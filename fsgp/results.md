---
title: Official Electrek FSGP Results
layout: page-fullwidth
nav-menu: true
header: no
social_title: Electrek Formula Sun Grand Prix 2024 Results
social_description: See the Official Results from Bowling Green, KY
social_image: "{% link assets/images/florida_fsgp_front.jpg %}"
breadcrumb: true
---


The Electrek Formula Sun Grand Prix 2024 is 3 days of racing on the 3.15 mile full course at the [National Corvette Museum Motorsports Park](https://www.motorsportspark.org/) in Bowling Green, Kentucky. Solar Cars drive for 8 hours per day and have additonal solar charging time available in the morning and evening. FSGP is open to the public and free to attend! 

-----
_Running lap counts from the track will be updated periodically throughout the day. MOV Scores will be calculated at the end of each race day._

{% tabs class %}
{% tab class SOV Class%}

{% include fsgp-lap-chart-js-grey class="sov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table class="sov" %}



{% endtab %}
{% tab class MOV Class%}


Vehicles competing in the [Multi Occupant Vehicle Class](https://www.americansolarchallenge.org/the-competition/vehicle-classes/) at FSGP are scored based on a formula that includes the number of miles (laps) driven, the number of passengers in the vehicle during those laps, amount of external charging (non-solar charging), and average speed. The full formula is detailed at the [bottom of this page](#mov-scoring-formula). 


-----
## MOV Score

{% include fsgp-score-chart-js %}

<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-score-table %}
</div>

-----

## MOV Laps
{% include fsgp-lap-chart-js class="mov" %}
<br>
<div style="margin:auto; text-align:center;"> <i> Scroll right to see all data on small screens </i>
{% include fsgp-table class="mov" %}
</div>

-----

# MOV Scoring Formula

At FSGP, Multi Occupant Vehicles are scored based on the number of laps they complete, the number of passengers carried, the amount of external energy used, and their average speed. The scoring formula is as follows: \$$ S = \frac{1}{E} \times D \times C \times T $$

Variable Definitions: 
- __S__: Score
- __D__: Person  Mile Distance - the number of miles driven (2.5 miles per lap) times the average number of passengers in the vehicle. 
- __E__: External Energy Usage - the vehicles battery capacity (assumed to start FSGP full) plus any external charging during the event. 
- __C__: Completion Factor - the number of miles driven less penalty miles divided by the highest number of miles driven by any team. 
- __T__: Target Speed Derating - vehicles must average at least <b>35 mph</b> for the event, in which case this factor will be 1.0. Otherwise they have their score derated based on the following formula: \$$ T = (0.6)^{(35-[Average Speed])^{0.4}} $$



{% endtab %}
{% endtabs %}

-----

{% assign url = site.baseurl | prepend: site.url %}
<link rel="stylesheet" href="{{ url }}/assets/css/tabs.css">
<script src="{{ url }}/assets/js/tabs.js"></script>
<script> jekyllTabs.init({
    activateTabFromUrl: true,
});
</script>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>




