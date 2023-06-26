---
layout: page-fullwidth
title: Single Occupant Results
description: "3 Days of Racing on the Track For the Most Laps"
nav-menu: true
header: no
permalink: "fsgp_sov"
---

The Electrek Formula Sun Grand Prix 2023 is 3 days of racing on the 2.5 mile road course at [Heartland Motorsports Park](http://heartlandmotorsports.us/) in Topeka, Kansas. Solar Cars drive for 8 hours per day and have additonal solar charging time available in the morning and evening. FSGP is open to the public and free to attend! [Full Event Info →](https://www.americansolarchallenge.org/the-competition/2023-formula-sun-grand-prix/)

-----

Vehicles competing in the [Single Occupant Vehicle Class](https://www.americansolarchallenge.org/the-competition/vehicle-classes/) are ranked solely on laps completed. The most laps over 3 days wins!

{% include fsgp-final-results class="sov" %}

-----
{% if site.fsgp-days-tabs %}
{% tabs day %}
{% tab day Overall %}
{% include fsgp-lap class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table class="sov" %}
{% endtab %}

{% tab day Day 1 %}
{% include fsgp-lap-day day="day1" class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table-day day="day1" class="sov" %}
{% endtab %}

{% tab day Day 2 %}
{% include fsgp-lap-day day="day2" class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table-day day="day2" class="sov" %}
{% endtab %}

{% tab day Day 3 %}
{% include fsgp-lap-day day="day3" class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table-day day="day3" class="sov" %}
{% endtab %}
{% endtabs %}{% else %}
{% tabs dayonly %}
{% tab dayonly Overall %}
{% include fsgp-lap class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table class="sov" %}
{% endtab %}
{% endtabs %}
{% endif %}

{% assign url = site.baseurl | prepend: site.url %}
<link rel="stylesheet" href="{{ url }}/assets/css/tabs.css">
<script src="{{ url }}/assets/js/tabs.js"></script>