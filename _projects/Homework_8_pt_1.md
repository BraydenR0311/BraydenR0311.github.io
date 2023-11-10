---
name: Homework 8 pt. 1
tools: [Python, Altair, vega-lite]
image: assets/pngs/chart.png
description: Chart 1 for Homework 8
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Example with Altair

Just look at this. Look at this art. It's enough to make an envious man of Michelangelo. So, I decided to use the buildings dataset, and I linked the two graphs I made for the last homework. They are essentially the same graphs, but I redid the code in altair, when it was formerly javascript. I like altair better since I'm so used to Python. Too many dictionaries and lists overwhelm me.

These charts represent square footage of the different usage descriptions. The bar chart represents the average square footage among the usage descriptions, whereas the point represents the square footage by year.

"For homework seven, the point chart was just the 'education' usage description". But, with the interactivity, I linked the two so you can click on the bar of the usage description you want and it shows up on the point graph. Killing two birds with one stone, created by two graphs and added interactivity by linking them. I had the idea to link them by selecting the category, and somehow I figured out the code to do so. There were too many points clumped together, so I had to just choose one category for homework seven. But, being able to choose from all of them is pretty cool. It's awesome because you can use this in so many other instances. I think it'd also be cool to add tooltips on mouse hover. It could include things like the city, county, etc.

I think the bar chart works well because it shows categorical variables. It also aggregates the square footage by the mean. For the point graph, it's best represented by a point because it shows individual buildings with their respective square footage, and the year is on the x-axis, of course. There's no specific color scheme. They're just represented by different colors for visual appeal and comprehensibility. I'm really proud of this work.

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart.json" style="width: 100%"></vegachart>

## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>
