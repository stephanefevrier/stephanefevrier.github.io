---
layout: post
title:  "COVID-19 interactive visualizations"
date:   2020-04-12 14:14:20 +0200
categories: Health
permalink: covid-19-visualizations
---

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>


This page contains several interactive visualizations about the COVID-19 propagation, with the goal to provide an easy way to access and explore the data, gathered from the <a href="https://github.com/CSSEGISandData/COVID-19" target="_blank">Johns Hopkins Github repository</a>.
<!--  and <a href="https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset" target="_blank">Kaggle</a>.  -->

All plots are automatically updated daily, and their interactivity encourages user exploration. The code written in Python on a Jupyter notebook is maintained on <a href="https://github.com/stephanefevrier/covid-19-analysis" target="_blank">this repository</a>.

# Disclaimer 

This page was made out of boredom for the sole purpose of producing embeddable interactive plots, the nature of the data itself is anecdotal.

# Notes on the data

- Data starts on January 22, 2020.
- Cases are separated in 3 categories: *confirmed, deaths and recovered*.
- Comparison between countries is subject to a number of caveats: each country has a different way of counting the number of cases.
- Spikes in the number of cases may appear, and are generally caused by the introduction of a new way of counting by the contry concerned.

*The visualizations are provided for informative purpose only, the numbers may differ from the official ones although differences should be minor.*

<!--All plots are interactive and should be played with. Change the scale / data with the dropdown menus, select the data to be displayed with the legend, and zoom-in by performing a left-click and drag, drawing a square or a vertical / horizontal line. Explore the upper-right corner of each plot to go through other possibilities such as toogling spikes lines. -->


# World

<!-- World indicators -->
<iframe width="100%" height="300" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/16.embed?showlink=false"></iframe>

The evolution of the **total number of cases in the world** is presented below, along with the **repartition between cases**. The legend is interactive, and the y-axis can be set to a logarithmic scale.

<!-- World scatter (total) --->
<iframe width="100%" height="600" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/164.embed?showlink=false"></iframe>

The number of **daily new cases in the world** is given below, along with the **repartition between daily new cases**. Use the **button** to switch between numbers and percentages (calculated as a comparison with the previous day). The legend is interactive, and the y-axis can be set to a logarithmic scale.

<!-- World scatter (delta) --->
<iframe width="100%" height="600" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/166.embed?showlink=false"></iframe>

# Per country

The **map** below shows the **total number of cases** for each country. Use the **button** to switch between cases. See also the <a href="/map_animated.html" target="_blank">animated evolution of daily deaths through time</a> (opening in a new tab).

<!-- map -->
<iframe width="100%" height="600" frameborder="0" scrolling="yes" src="//plotly.com/~stephanefevrier/41.embed?showlink=false"></iframe>

The following **heatmap** shows the **daily or total number of deaths through time**, expressed **as a number or as a proportion of the population** (use the **buttons** to choose data). Hovering the mouse provides additional informations.

On the y-axis, **169 countries** are presented by alphabetical order. The **color** shows the data like a **height** seen from top-view. This 3rd dimension represented by the color can be seen explicitly by clicking on the **"3D Surface" button** (some seconds to load).

<!-- heatmap / surface -->
<iframe width="100%" height="800" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/577.embed?showlink=false"></iframe>

The **scatter plots** below, more conventional, show for 10 countries the number of confirmed / deaths / recovered cases (use the **button** to switch). On the above, the **total number of cases**, on the bottom, the **number of new cases each day**. The legend is interactive, and the y-axes can be set to a logarithmic scale.

<!-- scatterplot per country -->
<iframe width="100%" height="700" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/18.embed?showlink=false"></iframe>

To allow better comparison between countries, the same graph is given with the **number of cases per 100,000 inhabitants**. The legend is interactive, and the y-axes can be set to a logarithmic scale.

<!-- scatterplot per country with percentages -->
<iframe width="100%" height="700" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/568.embed?showlink=false"></iframe>


<!--
For a lot of countries.

<iframe width="100%" height="800" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/586.embed?showlink=false"></iframe>


 
Exploratory data analysis


To explore the data differently, the *violin plot* below shows the effect of age and gender on the possibility of dying of the disease. It is to be noted that the dataset contains only 825 examples. More details on the dataset used and its biases are given below the plot. 
Gender is slightly correlated to the possibility of dying of the disease (roughly $$0.1$$), but the age correlation to the possibility of dying is higher (almost $$0.3$$). Pearson correlation coefficient is used, measuring a linear correlation.

<!-- violin plot death -->
<!--
<iframe width="100%" height="500" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/208.embed?showlink=false"></iframe>

To understand the distribution of the **data used for the previous plot** and its possible biases, the *Sankey diagram* below shows the country, relationship to Wuhan, and gender of the population sample studied. It is useful to directly see any over-/under-representation of a category. 

<iframe width="100%" height="800" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/277.embed?showlink=false"></iframe>

What can be drawn from this diagram about the dataset used:
- a majority of the population presented is coming from Asia. 
- 32% of the population  is related to Wuhan, whether by travelling or living there. 
- 17% of genders are unknown (thus removed from the dataset). In known genders, 58% are male and 42% female. 

These 3 biases need to be remembered when drawing conclusions from the violin plot, which therefore does not represent the world population. 

-->