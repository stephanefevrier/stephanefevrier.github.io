---
layout: post
title:  "COVID-19 interactive visualizations"
date:   2020-04-12 14:14:20 +0200
categories: Health
permalink: /covid-19-visualizations/
---
This page contains several interactive visualizations about the COVID-19, with the goal to provide an easy way to access and explore the data. Gathered from <a href="https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset" target="_blank">Kaggle</a>, the data is coming from the <a href="https://github.com/CSSEGISandData/COVID-19" target="_blank">Johns Hopkins Github repository</a>. 

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

To explore the data differently, the *violin plot* below shows the effect of age and gender on the possibility of dying of the disease. It is to be noted that the dataset used contains less that 1000 people. More details on the dataset used and its biases are given below the plot. 

A small correlation of the gender is seen (0.1), but the age seems to be a more influent factor (almost 0.3). Pearson correlation is used, meaning that the coefficient quantifies a linear relationship. 

<!-- violin plot death -->
<iframe width="100%" height="500" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/208.embed?showlink=false"></iframe>

To understand the data used for the violin plot, the 15 most represented countries in the dataset are shown through a Sankey diagram, where the relationship to Wuhan and the gender of each person are given. This diagram is not here to draw conclusions, but to understand the possible underlying biases present in the data, along with its distribution. 


What can be drawn from this diagram about the dataset used:
- the majority of the population presented is coming from Asia. 
- a huge proportion of the population is related to Wuhan, whether by travelling or living there. 
- a significant proportion of genders are unknown. 

These 3 biases need to be remembered when drawing conclusions from the violin plot, which therefore does not represent the world population. For example, the gender correlation on the patient outcome (dying or not) is already low, but also heavily 

<iframe width="100%" height="800" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/277.embed?showlink=false"></iframe>
