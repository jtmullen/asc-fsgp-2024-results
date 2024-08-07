---
title: Official Electrek FSGP Results
layout: page-fullwidth
nav-menu: true
permalink: /fsgp/results/
header: no
social_title: Electrek Formula Sun Grand Prix 2024 Results
social_description: See the Official Results from Bowling Green, KY
social_image: "{% link assets/images/florida_fsgp_front.jpg %}"
breadcrumb: true
---

The Electrek Forumla Sun Grand Prix is a 3-day track event. For 8 hours each day, solar cars will drive on the 3.15 mile course at the [National Corvette Museum Motorsports Park](https://www.motorsportspark.org/) in Bowling Green, Kentucky. FSGP is open to the public and free to attend! 

-----
_Running lap counts from the track will be updated periodically throughout the day. MOV Scores will be calculated at the end of each race day._

{% tabs class %}
{% tab class SOV Class%}

__First Place:__ #92 Éclipse (215 laps / 677.25 miles)<br>
__Second Place:__ #32 Principia (189 laps / 539.35 miles)<br>
__Third Place:__ #17 Illinois State (149 laps / 469.35 miles)

__Fastest Lap:__ Jae Won Hwang from #6 Berkeley. 4:21.414 time / 43.4 mph average

{% include fsgp-lap-chart-js class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens. </i>
{% include fsgp-table class="sov" %}
</div>
### Provisional Qualification

The following SOV teams have been granted provisional qualification for the American Solar Challenge:
- #26 British Columbia
- #22 Ilinois
- #12 Texas A&M
- #2 Michigan
- #786 Western Michigan


{% endtab %}
{% tab class MOV Class%}


Vehicles competing in the [Multi Occupant Vehicle Class](https://www.americansolarchallenge.org/the-competition/vehicle-classes/) at FSGP are scored based on a formula that includes: the number of miles (laps) driven, the number of passengers in the vehicle during those laps, amount of external charging (non-solar charging), and average speed. The full formula is as follows: \$$ S = \frac{1}{E} \times D \times C \times T $$
Variable Definitions: 
- __S__: Score
- __D__: Person Mile Distance - the number of miles driven (3.15 miles per lap) times the average number of passengers in the vehicle 
- __E__: External Energy Usage - the vehicles battery capacity (assumed to start FSGP full) plus any external charging during the event in kWh
- __C__: Completion Factor - the number of miles driven less penalty miles divided by the highest number of miles driven by any team 
- __T__: Target Speed Derating - 1.0 if the vehicle averages at least <b>30 mph</b> for the duration of the event. If average speed is less than 30 mph, the team will have their score derated based on the following formula: \$$ T = (0.6)^{(30-[Average Speed])^{0.4}} $$


MOV teams must also complete a minimum number of official laps over the 3 days, teams that do not will be ranked below all teams who do. For 2024 at NCM Motorsports Park this is 153 official laps (482 miles).

-----
## MOV Score

__First Place:__ #55 Poly Montreal (88.57 score / 165 laps)<br>
__Second Place:__ #828 App State (36.53 score / 201 laps)<br>
__Third Place:__ #35 Minnesota (20.16 score / 158 laps)

__Fastest Lap:__ Logan Staubus from #9 Iowa State. 4:38.223 time / 40.8 mph average

{% include fsgp-score-chart-js %}

<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens. </i>
{% include fsgp-score-table %}
</div>

-----

## MOV Laps
{% include fsgp-lap-chart-js class="mov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens. </i>
{% include fsgp-table class="mov" %}
</div>

### Provisional Qualification

The following MOV teams have been granted provisional qualification for the American Solar Challenge:
- #4 MIT

{% endtab %}
{% endtabs %}


{% assign url = site.baseurl | prepend: site.url %}
<link rel="stylesheet" href="{{ url }}/assets/css/tabs.css">
<script src="{{ url }}/assets/js/tabs.js"></script>
<script> jekyllTabs.init({
    activateTabFromUrl: true,
    activateTabFromUrl: true,
});
</script>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>




