---
name: Illini Football
tools: [Python, Vega-Altair]
image: assets/pngs/football.png
description: Interactive Football Charts
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Interactive, Linked Illini Football Charts
As a die-hard Illinois fan and a saxophone in the Marching Illini, I'm deeply invested in our football team. It's also cool to learn about the history of the team and how we've done over the years. Motivated by this passion, I decided to make an interactive dashboard to display the performance of our team from 1892 to 2020.
<vegachart schema-url="{{ site.baseurl }}/assets/json/football_chart.json" style="width: 100%"></vegachart>


The charts are linked, the top chart covering almost the entire existence of Illinois Football, displaying the wins and losses grouped by season. When you hover over the chart, you will see a tooltip with essential information. Click on the chart on a given year and it will filter the data for the chart below. What you see in the bottom chart are the scores from each game of the selected season. Neat, right?

## Some Tips:
The chart and tooltip just look better when the website is in "light mode", which can be changed by clicking on the sun/moon emoji in the site's navigation menu. Also, don't double click and don't click on the point markers. Evil things will happen.

## Explore the dataset and the Python Notebook:

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://discovery.cs.illinois.edu/dataset/football/" text="Football Dataset" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/BraydenR0311/BraydenR0311.github.io/blob/main/python_notebooks/football.ipynb" text="Python Notebook" %}
</div>


