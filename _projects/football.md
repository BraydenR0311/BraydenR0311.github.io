---
name: Illini Football
tools: [Python, Vega-Altair]
image: assets/pngs/football.png
description: Chart 1 for Homework 8
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Interactive, Linked Illini Football Charts
As an Illini fan and a member of the Marching Illini, I'm deeply invested in our football team. It's also cool to learn about the history of the team and how we've done over the years. As a result of this passion, I decided to make an interactive dashboard to display the performance of our team from 1892 to 2020.
<vegachart schema-url="{{ site.baseurl }}/assets/json/football_chart.json" style="width: 100%"></vegachart>

The charts are linked, the top chart being almost the entire existence of Illinois Football, displaying the wins and losses grouped by season. When you hover over the chart, you will see a tooltip with essential information. Click on the chart on a given year and it will filter the data for the chart below. What you will see in the bottom chart is the scores from each game of the selected season. Neat, right?

Some tips: The chart and tooltip just look better when the website is in "light mode", which can be changed by clicking on the sun/moon emoji in the site's toolbar. Also, don't double click and don't click on the point markers. Evil things will happen.

## Search The Data & Methods

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/BraydenR0311/BraydenR0311.github.io/blob/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/BraydenR0311/BraydenR0311.github.io/blob/main/python_notebooks/hw%208.ipynb" text="The Analysis" %}
</div>


