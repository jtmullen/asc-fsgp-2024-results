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

__The Live Timing Board will be updated during Event Hours__

*Note: The Live Online Timing Board is not the official timing board. Teams should cross reference with HQ on-site. Every effort is made to keep this up to data and accurate, in the case of descrepencies the on-site HQ specified times are official.*

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
<th>Data Loading</th>
</table>
<span id="livenote" style="display: none;">
__The Timing Board is currently live!__ _Information on this page automatically updates, next updating in <b><span id="countdowntime">-</span></b> seconds._</span>
<span id="notlivenote" style="display: none;">__The Timing Board is not current live, live updates will begin at: <span id="livestarttime">-</span>__. Please Refresh at that time.</span>


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

var time_to_update = update_interval_seconds;
function next_update_time(){
	document.getElementById("countdowntime").innerHTML = time_to_update;
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

function createTable(timingData){
	liveTable = document.getElementById("liveTable");
	switch(Number(timingData.stage)) {
	  case 1:
		liveTable.innerHTML = document.getElementById("stage1template").innerHTML;
		break;
	  case 2:
		liveTable.innerHTML = document.getElementById("stage2template").innerHTML;
		break;
	  case 3: 
		liveTable.innerHTML = document.getElementById("stage3template").innerHTML;
		break;
	  case 4:
		liveTable.innerHTML = document.getElementById("stage4template").innerHTML;
		break;
	  default:
		liveTable.innerHTML = "<th>Data Not Available</th>"
		throw new Error("Unknown Stage")
		break;
	} 
	
	if(!timingData.live){
		document.getElementById("livestarttime").innerHTML = timingData.livestart;
		document.getElementById("notlivenote").style.display = "";
		return;
	};
	timingData.results.forEach((result, rowIndex) => {
		const newRow = liveTable.getElementsByTagName('tbody')[0].insertRow();
		newRow.id = `row${rowIndex}`
		const cells = result.split(',');
		cells.forEach((cell, cellIndex) => {
			const newCell = newRow.insertCell();
			newCell.innerHTML = cell;
			newCell.id = `row${rowIndex}cell${cellIndex}`
		});
	});
	document.getElementById("livenote").style.display = "";
	setInterval(next_update_time, 1000);
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

</script>


<div id="templateheaders" style="display:none">

</div>

## Completed Timing Boards
{% tabs stage-timing %}
{% tab stage-timing Stage 1 %}
{% include asc-timing-board stage="1" %}
{% endtab %}
{% tab stage-timing Stage 2 %}
{% include asc-timing-board stage="2" %}
{% endtab %}
{% tab stage-timing Stage 3 %}
{% include asc-timing-board stage="3" %}
{% endtab %}
{% tab stage-timing Stage 4 %}
{% include asc-timing-board stage="4" %}
{% endtab %}
{% endtabs %}

<link rel="stylesheet" href="{{ url }}/assets/css/tabs.css">
<script src="{{ url }}/assets/js/tabs.js"></script>
<script> jekyllTabs.init({
});</script>


<div id="templateheaders" style="display:none">
<div id="stage1template">
{% include asc-timing-board stage="1" %}
</div>
<div id="stage2template">
{% include asc-timing-board stage="2" %}
</div>
<div id="stage3template">
{% include asc-timing-board stage="3" %}
</div>
<div id="stage4template">
{% include asc-timing-board stage="4" %}
</div>
</div>