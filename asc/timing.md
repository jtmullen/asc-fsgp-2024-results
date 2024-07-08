---
title: Timing Board
layout: page-fullwidth
nav-menu: true
permalink: /asc/timing/
header: no
social_title: Electrek ASC 2024 Timing Board
social_description: Up to Date Timing Information from ASC 2024
social_image: "{% link assets/images/prin_drone.jpg %}"
breadcrumb: true
---

__Coming Soon__

<style>


thead {
	font-weight: bold;
	border-bottom: 2px solid;
}

td, th {
	border: 1px solid;
}

td {
	white-space: nowrap;
	display: block;
	overflow: auto; 
	max-width: 100%;
}

td.transition, tr.transition {
	transition: background-color 4s ease-in;
}

td.changed, tr.changed {
	background-color: #84bc41;
}

td:last-child {
	font-style: italic;
}
</style>
<table id="liveTable" style="margin:auto; border: 2px solid;overflow:auto;">
<colgroup>
<col>
<col>
<col>
<col>
<col>
<col>
<col>
<col style="border-left: 2px solid">
<col style="font-style: italic">
</colgroup>
<thead>
  <tr>
    <th rowspan="2">Team</th>
    <th rowspan="2">Stage Start Time</th>
	<th colspan="3" style="text-align: center; border-bottom: 0;">Paducah Checkpoint</th>
	<th colspan="2" style="text-align: center; border-bottom: 0;">Edwardsville Stage</th>
	<th rowspan="2">Next Release Time</th>
	<th rowspan="2">Last Known Status</th>
  </tr>
  <tr style="border-bottom: 1px solid">
	<th rowspan="1" style="border-top: 0">Arrival</th>
	<th rowspan="1" style="border-top: 0">Departure</th>
	<th rowspan="1" style="border-top: 0">Loops</th>
	<th rowspan="1" style="border-top: 0">Arrival</th>
	<th rowspan="1" style="border-top: 0">Loops</th>
  </tr>
</thead>
<tbody>
<tr id="row0"><td id="row0cell0">#1 - Team Name</td><td id="row0cell1">9:01am</td><td id="row0cell2">2:12pm</td><td id="row0cell3"></td><td id="row0cell4"></td><td id="row0cell5"></td><td id="row0cell6"></td><td id="row0cell7">4:15pm</td><td id="row0cell8">Holding in Paducah</td></tr>
</tbody>
</table>
_The information on this page automatically updates, next updating in <b><span id="time"></span></b> seconds._


<script>

update_interval_seconds = 5;

function fadeoutHighlight(changeList){
	changeList.forEach((id) => {
		document.getElementById(id).classList.add("transition");
		document.getElementById(id).classList.remove("changed");
	});
}

function highlightChanges(changeList){
	changeList.forEach((id) => {
		document.getElementById(id).classList.remove("transition");
		document.getElementById(id).classList.add("changed");
		setTimeout(fadeoutHighlight, 500, changeList);
	});
}

function updateTable(timingData){
	liveTable = document.getElementById("liveTable");
	changedIds = [];
	timingData.results.forEach((result, rowIndex) => {
		existingRow = document.getElementById(`row${rowIndex}`)
		const cells = result.split(',');
		if (existingRow){
			cells.forEach((cell, cellIndex) => {
				existingCell = document.getElementById(`row${rowIndex}cell${cellIndex}`)
				existingContent = existingCell.innerHTML;
				existingCell.innerHTML = cell;
				if(existingContent != cell){
					changedIds.push(`row${rowIndex}cell${cellIndex}`);
				}
		});
		}
		else{
			const newRow = liveTable.insertRow();
			newRow.id = `row${rowIndex}`;
			changedIds.push(`row${rowIndex}`)
			cells.forEach((cell, cellIndex) => {
				const newCell = newRow.insertCell();
				newCell.innerHTML = cell;
				newCell.id = `row${rowIndex}cell${cellIndex}`
			});
		}
	});
	highlightChanges(changedIds);
}

function createTable(timingData){
	liveTable = document.getElementById("liveTable");
	timingData.results.forEach((result, rowIndex) => {
		const newRow = liveTable.insertRow();
		newRow.id = `row${rowIndex}`
		const cells = result.split(',');
		cells.forEach((cell, cellIndex) => {
			const newCell = newRow.insertCell();
			newCell.innerHTML = cell;
			newCell.id = `row${rowIndex}cell${cellIndex}`
		});
	});
}

function getTimingDataUpdateTable(){
	console.log("Running Update");
	fetch("../../assets/timing.json")
		.then(res => res.json())
		.then(function(res) {updateTable(res)})
		.catch(function(error){console.log(error)})
}

fetch("../../assets/timing.json")
  .then(res => res.json())
  .then(function(res) {createTable(res)})
  .catch(function(error){console.log(error)})

var time_to_update = update_interval_seconds;
function next_update_time(){
	document.getElementById("time").innerHTML = time_to_update;
	if(time_to_update == 1 && document.hidden == true){
		console.log("Wait");
		return;
	}
	if (time_to_update == 0){
			getTimingDataUpdateTable()
			time_to_update = update_interval_seconds;
	}else{
		time_to_update--;
	}
}
setInterval(next_update_time, 1000);

// document.getElementById("test").classList.remove("transition");
// document.getElementById("test").classList.add("changed");
// document.getElementById("test").classList.add("transition");
// setTimeout(function (){
// document.getElementById("test").classList.remove("changed");}, 1000);

</script>

*Note: The Live Timing Board is not official and is for reference only. Every effort is made to ensure this page is up to date and correct; however, official times are those specified by HQ on site and Official Results as published at the end of the stage*

