---
title: Multi Occupant Results
layout: page-fullwidth
description: '3 Days of Highly Efficient Driving Competing for the Highest Score'
nav-menu: true
header: no
---


The Electrek Formula Sun Grand Prix 2023 is 3 days of racing on the 2.5 mile road course at [Heartland Motorsports Park](http://heartlandmotorsports.us/) in Topeka, Kansas. Solar Cars drive for 8 hours per day and have additonal solar charging time available in the morning and evening. FSGP is open to the public and free to attend! [Full Event Info →](https://www.americansolarchallenge.org/the-competition/2023-formula-sun-grand-prix/)

-----

Vehicles competing in the [Multi Occupant Vehicle Class](https://www.americansolarchallenge.org/the-competition/vehicle-classes/) at FSGP are scored based on a formula that includes the number of miles (laps) driven, the number of passengers in the vehicle during those laps, external energy used, and average speed. The full formula is detailed at the bottom of this page. 

{% include fsgp-final-results class="mov" %}
-----
## MOV Score
{% tabs day %}
{% tab day Overall %}
{% include fsgp-score-chart %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-score-table %}
{% endtab %}
{% tab day Day 1 %}
{% include fsgp-score-chart-day day="day1" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-score-table-day day="day1" %}
{% endtab %}

{% tab day Day 2 %}
{% include fsgp-score-chart-day day="day2" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-score-table-day day="day2" %}
{% endtab %}

{% tab day Day 3 %}
{% include fsgp-score-chart-day day="day3" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-score-table-day day="day3" %}
{% endtab %}
{% endtabs %}

-----
## MOV Laps
{% tabs day %}
{% tab day Overall %}
{% include fsgp-lap class="mov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table class="mov" %}
{% endtab %}

{% tab day Day 1 %}
{% include fsgp-lap-day day="day1" class="mov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table-day day="day1" class="mov" %}
{% endtab %}

{% tab day Day 2 %}
{% include fsgp-lap-day day="day2" class="mov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table-day day="day2" class="mov" %}
{% endtab %}

{% tab day Day 3 %}
{% include fsgp-lap-day day="day3" class="mov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table-day day="day3" class="mov" %}
{% endtab %}
{% endtabs %}

-----

# MOV Scoring Formula

At FSGP, Multi Occupant Vehicles are scored based on the number of laps they complete, the number of passengers carried, the amount of external energy used, and their average speed. The scoring formula is as follows: \$$ S = \frac{D}{E} \times C \times T $$

Variable Definitions: 
- __S__: Score
- __D__: Person  Mile Distance. This is the number of miles driven (2.5 miles per laps) times the average number of passengers in the vehicle. 
- __E__: External Energy Usage. This is the vehicles battery capacity (assumed to start FSGP full) plus any external charging during the event. 
- __C__: Completion Factor. This is the number of miles driven less penalty miles divided by the highest number of miles driven by any team. 
- __T__: Target Speed Derating. Multi Occupant Vehicles must average at least 30mph for the event, in which case this factor will be 1.0. Otherwise they have their score derated based on the following formula: \$$ T = (0.6)^{(30-[Average Speed])^{0.4}} $$

-----

{% assign url = site.baseurl | prepend: site.url %}
<link rel="stylesheet" href="{{ url }}/assets/css/tabs.css">
<script src="{{ url }}/assets/js/tabs.js"></script>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>




