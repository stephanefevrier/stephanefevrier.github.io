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


This page contains several interactive visualizations about the COVID-19, with the goal to provide an easy way to access and explore the data, gathered from the <a href="https://github.com/CSSEGISandData/COVID-19" target="_blank">Johns Hopkins Github repository</a> and <a href="https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset" target="_blank">Kaggle</a>. 

All plots are interactive and should be played with. Change the scale / data with the dropdown menus, select the data to be displayed with the legend, and zoom-in by performing a left-click and drag, drawing a square or a vertical / horizontal line. Explore the upper-right corner of each plot to go through other possibilities such as toogling spikes lines. 

The code is maintained on <a href="https://github.com/stephanefevrier/covid-19-analysis" target="_blank">this repository</a>, made with Python on a Jupyter notebook.

# Disease propagation summary

Summary of the disease propagation since 22/01/20. Cases are compartmented into 3 categories: confirmed, deaths and recovered.

About the data:
- Numbers are provided for informative purpose only and may differ from the official ones, although differences should be minor.
- Each country has a different way of counting the number of cases, making comparisons less relevant. The number of deaths is supposed to be the closest to reality, but is still an estimate.

## World

Overview of the COVID-19, world-wise. 

<!-- World indicators -->
<iframe width="100%" height="300" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/16.embed?showlink=false"></iframe>

The evolution of the number of total cases in the world is presented below, with the bottom subplot giving the repartition between cases.

<!-- World scatter (total) --->
<iframe width="100%" height="600" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/164.embed?showlink=false"></iframe>

The number of new cases each day is given below. The percentage is calculated as the difference with the previous day. The bottom subplot gives the repartition between cases.

<!-- World scatter (delta) --->
<iframe width="100%" height="600" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/166.embed?showlink=false"></iframe>

## Per country

Overview of the COVID-19, country-wise. Use the upper-left menu to zoom. Switching back the projection from orthographic to Natural earth or Equirectangular may lead to projection problems. 

See also the <a href="/map_animated.html" target="_blank">geographical evolution of COVID-19 deaths cases through time</a> (opening in a new tab).


<!-- map -->
<iframe width="100%" height="600" frameborder="0" scrolling="yes" src="//plotly.com/~stephanefevrier/41.embed?showlink=false"></iframe>

Country-wise scatter plot. On the above, the total number of cases, on the bottom, the number of new cases each day. The interactive legend allows to isolate a specific country or a group of countries. 

Choose the type of cases (*confirmed* / *deaths* / *recovered*) and the y-axes scale with the dropdown menus.

<!-- scatterplot per country -->
<iframe width="100%" height="700" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/18.embed?showlink=false"></iframe>

# Exploratory data analysis

To explore the data differently, the *violin plot* below shows the effect of age and gender on the possibility of dying of the disease. It is to be noted that the dataset contains only 825 examples. More details on the dataset used and its biases are given below the plot. 

Gender is slightly correlated to the possibility of dying of the disease (roughly $$0.1$$), but the age correlation to the possibility of dying is higher (almost $$0.3$$). Pearson correlation coefficient is used, measuring a linear correlation.

<!-- violin plot death -->
<iframe width="100%" height="500" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/208.embed?showlink=false"></iframe>

To understand the distribution of the **data used for the previous plot** and its possible biases, the *Sankey diagram* below shows the country, relationship to Wuhan, and gender of the population sample studied. It is useful to directly see any over-/under-representation of a category. 

<iframe width="100%" height="800" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/277.embed?showlink=false"></iframe>

What can be drawn from this diagram about the dataset used:
- a majority of the population presented is coming from Asia. 
- 32% of the population  is related to Wuhan, whether by travelling or living there. 
- 17% of genders are unknown (thus removed from the dataset). In known genders, 58% are male and 42% female. 

These 3 biases need to be remembered when drawing conclusions from the violin plot, which therefore does not represent the world population. 
