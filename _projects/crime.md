---
name: Crime Unveiled. Chicago's Underbelly Exposed 
tools: [Python, Vega-Altair]
image: assets/pngs/crime.png
description: Crime Football Charts
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Names
Brayden Riesberg - bjr3
Anna Ochoa - aochoa29
Justin Lam - hungkl2
Kyle Cruz - kcruz27
# Chicago Crime, Interactive Charts
Below, we see two graphs that are linked interactively. On the very right is a legend that you can hover over, which filters data in the charts. For example, if you hover over "ARSON", you get results only for Arson. In the bar chart, the orange represents the crimes that resulted in arrests. So, have fun seeing which types of crimes result in the mosts arrests.

<vegachart schema-url="{{ site.baseurl }}/assets/json/crime_chart.json" style="width: 100%"></vegachart>

# Chicago Crime Cloropleth

![image](/assets/pngs/crimemap.png)

This image is taken from a dataset about crime in Chicago neighborhoods. The visualization shows every neighborhood in Chicago and has a color associated with it signifying the safeness of the neighborhood where the darker the color the more “dangerous” the neighborhood is. If you hover over a certain section it highlights it and tells the user the name of the neighborhood so the visualization is very easy to use and understand.  It also shows you the 10 safest neighborhoods in Chicago.

Source:
{% include elements/button.html link="https://www.neighborhoodscout.com/il/chicago/crime" text="Crime Cloropleth" %}

# Chicago Police Stations

![image](/assets/pngs/police.png)

This image is taken from a city of chicago dataset. The dots represent police stations in Chicago and if you click on one of them you are given more information such as the station's location in coordinates, as well as what number station it is. This information is placed over an actual map of Chicago so you are able to zoom in and see the address of the station and change the view of the map between roadmap, satellite and terrain.

Source:
{% include elements/button.html link="https://data.cityofchicago.org/Public-Safety/Police-Stations-Map/gkur-vufi" text="Police Map" %}

## Explore the dataset and the Python Notebook:

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://data.cityofchicago.org/stories/s/Crimes-2001-to-present-Dashboard/5cd6-ry5g" text="Crime Dataset" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/BraydenR0311/sync/blob/master/is445/final/finalv2.ipynb" text="Python Notebook" %}
</div>


