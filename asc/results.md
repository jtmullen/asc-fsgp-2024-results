---
title: Official Electrek ASC Results
layout: page-fullwidth
permalink: /asc/results/
social_title: Electrek American Solar Challenge 2024 Results
social_description: 'Official Results from the Road as the solar cars See America By National Historic Trail'
social_image: "{% link assets/images/ets_scottsbluff.jpg %}"
nav-menu: true
header: no
breadcrumb: true
---

The Electrek American Solar Challenge 2024 is an 8 day 1550+ mile competition split into 4 stages. Teams will take the road following 7 [National Historic Trails](https://www.nps.gov/subjects/nationaltrailssystem/national-historic-trails.htm) as they _See America By National Historic Trail!_


## Scoring 

The 2024 Event is once again a distance-based competition. The primary goal is to compelete the 1560 mile base route; however, teams will have numerous opportuntities to complete additional optional loop segments to gain addition miles (or person miles for Multi-Occupant Vehicles) which will help increase their ranking. See our [vehicle classes](https://www.americansolarchallenge.org/the-competition/vehicle-classes/) page for more info on the classes.


### Single Occupant Vehicle (SOV) Class
The Single Occupant class is scored solely on miles driven. The team that completes the most miles, while completing the base route, will win the event. Stage winners are also determined by miles driven on that stage. Teams who do not finish the base route will be ranked below all teams who do. In the event of a tie, elapsed time is the tie-breaker. 

### Multi-Occupant Vehicle (MOV) Class
Multi-Occupant vehicles are scored on a variety of factors including person-miles driven, their practicality score, amount of external energy used, and whether they maintain the 35mph target average speed. MOV teams must also complete the base route, any team that does not will be ranked below all teams who do. The scoring formula is as follows: \$$ S = \frac{1}{E} \times D \times C \times T \times P$$

Variable Definitions: 
- __S__: MOV Score
- __D__: Person-Mile Distance - the number of miles driven (2.5 miles per lap) times the average number of passengers in the vehicle. 
- __E__: External Energy Usage - the vehicles battery capacity (assumed to start FSGP full) plus any external charging during the event. 
- __C__: Completion Factor - the number of miles driven less penalty miles divided by the highest number of miles driven by any team. 
- __P__: Practicality Score - during display day a panel of judges will evalute the practical features of each vehicle and award a score from 0-100.
- __T__: Target Speed Derating - vehicles must average at least <b>35 mph</b> for the event, in which case this factor will be 1.0. Otherwise they have their score derated based on the following formula: \$$ T = (0.6)^{(35-[Average Speed])^{0.4}} $$

_Note: For individual stage winners, the pracitcality and external energy factors are not considered, only the "D x C x T" factors_

<ul class="actions">
<a href="https://www.americansolarchallenge.org/ASC/wp-content/uploads/2024/07/MOV-Team-Window-Stickers.pdf" class="button special" style="margin:5px">MOV Window Stickers</a>
<a href="https://www.americansolarchallenge.org/ASC/wp-content/uploads/2024/07/ASC-2024-MOV-Practicality-Rubric-Template.pdf" class="button special" style="margin:5px">MOV Practicality Judging Rubric</a>


# Results

_Distance Completed, Times, Average Speeds, and Passenger Information will be updated occasionally. Penalties, MOV Charging Information, and MOV Scores will be updated at the end of each stage._


{% tabs stage %}
{% tab stage Overall%}

__July 20th-27th:__ Nashville, TN to Casper, WY
- 1561.4 Total Base Route Miles
- 7 Optional Loops
    - 213.4 unique loop miles (teams may complete loops multiple times)

{% endtab %}
{% tab stage Stage 1%}
__July 20th & 21st:__ Nashville, TN to Edwardsville, IL via Paducah, KY
- Route Segments:
  - Nashville to Paducah: <i>159.7 miles</i>
  - Paducah to Edwardsville: <i>217.1 miles</i>
- Optional Loops:
  - Paducah Loop: <i>48.8 miles</i>
  - Edwardsville Loop: <i>29.2 miles</i>
{% endtab %}
{% tab stage Stage 2%}
__July 22nd & 23rd:__ Edwardsville, IL to St. Joseph, MO via Jefferson City, MO and Independence, MO
- Route Segments:s
  - Edwardsville to Jefferson City: <i>165.6 miles</i>
  - Jefferson City to Independence: <i>156.6 miles</i>
  - Independence to St. Joseph: <i>74.0 miles</i>
- Optional Loops:
  - Jefferson City Loop: <i>28.2 miles</i>
  - St. Joseph Loop: <i>32.8 miles</i>
  - _There is no loop at the Indpendence Checkpoint_
{% endtab %}
{% tab stage Stage 3%}
__July 24th-26th:__ St. Joseph, MO to Gering, NE via Beatrice, NE and Kearney, NE
- Route Segments:
  - St. Joseph to Beatrice: <i>138.2 miles</i>
  - Beatrice to Kearney: <i>178.4 miles</i>
  - Kearney to Gering: <i>273.6 miles</i>
- Optional Loops:
  - Beatrice Loop: <i>25.4 miles</i>
  - Kearney Loop: <i>22.0 miles</i>
  - Gering Loop: <i>26.0 miles</i>
{% endtab %}
{% tab stage Stage 4%}
__July 27th:__ Gering, NE to Casper, WY
- Route Segments:
  - Gering to Casper: <i>198.3 miles</i>
{% endtab %}
{% endtabs %}
## SOV Results
{% tabs stagesov %}
{% tab stagesov Overall%}
{% include asc-final-chart stage="overall" class="sov" %}
<br>&nbsp;
<br>&nbsp;
{% include asc-stage-table stage="overall" class="sov" %}
{% endtab %}
{% tab stagesov Stage 1%}
{% include asc-stage-chart stage="stage1" class="sov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage1" class="sov" %}
{% endtab %}
{% tab stagesov Stage 2%}
{% include asc-stage-chart stage="stage2" class="sov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage2" class="sov" %}
{% endtab %}
{% tab stagesov Stage 3%}
{% include asc-stage-chart stage="stage3" class="sov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage3" class="sov" %}
{% endtab %}
{% tab stagesov Stage 4%}
{% include asc-stage-chart stage="stage4" class="sov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage4" class="sov" %}
{% endtab %}
{% endtabs %}
<br>
## MOV Scores
{% tabs stagescore %}
{% tab stagescore Overall%}
{% include asc-score-chart-final-js %}
{% include asc-final-score %}
{% endtab %}
{% tab stagescore Stage 1%}
_For stage ranking MOV teams are scored solely on Distance, Completion Factor, and Target Speed. Other factors are not considered_
{% include asc-score-chart-js stage="stage1" %}
{% include asc-score-table stage="stage1" %}

</ul>

{% endtab %}
{% tab stagescore Stage 2%}
## MOV Scores
_For stage ranking MOV teams are scored solely on Distance, Completion Factor, and Target Speed. Other factors are not considered_
{% include asc-score-chart-js stage="stage2" %}
{% include asc-score-table stage="stage2" %}
{% endtab %}
{% tab stagescore Stage 3%}
_For stage ranking MOV teams are scored solely on Distance, Completion Factor, and Target Speed. Other factors are not considered_
{% include asc-score-chart-js stage="stage3" %}
{% include asc-score-table stage="stage3" %}
{% endtab %}
{% tab stagescore Stage 4%}
_For stage ranking MOV teams are scored solely on Distance, Completion Factor, and Target Speed. Other factors are not considered_
{% include asc-score-chart-js stage="stage4" %}
{% include asc-score-table stage="stage4" %}
{% endtab %}
{% endtabs %}
<br>
### MOV Distance Completed
{% tabs stagemov %}
{% tab stagemov Overall%}
{% include asc-final-chart stage="overall" class="mov" %}
<br>&nbsp;
<br>&nbsp;
{% include asc-stage-table stage="overall" class="mov" %}
{% endtab %}
{% tab stagemov Stage 1%}
{% include asc-stage-chart stage="stage1" class="mov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage1" class="mov" %}
{% endtab %}
{% tab stagemov Stage 2%}
{% include asc-stage-chart stage="stage2" class="mov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage2" class="mov" %}
{% endtab %}
{% tab stagemov Stage 3%}
{% include asc-stage-chart stage="stage3" class="mov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage3" class="mov" %}
{% endtab %}
{% tab stagemov Stage 4%}
{% include asc-stage-chart stage="stage4" class="mov" %}
<br>&nbsp;<br>
{% include asc-stage-table stage="stage4" class="mov" %}
{% endtab %}
{% endtabs %}

{% assign url = site.baseurl | prepend: site.url %}
<link rel="stylesheet" href="{{ url }}/assets/css/tabs.css">
<script src="{{ url }}/assets/js/tabs.js"></script>
<script> jekyllTabs.init({
    syncTabsWithSameLabels: true,
});
</script>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML">
</script>



