---
layout: post
title:  "COVID-19 interactive visualizations"
date:   2020-04-12 14:14:20 +0200
categories: Health
permalink: /covid-19-visualizations/
---
This page contains several interactive visualizations about the COVID-19, with the goal to provide an easy way to access and explore the data your own way. Data is gathered from [Kaggle](https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset), coming from the [Johns Hopkins Github repository](https://github.com/CSSEGISandData/COVID-19). 

All plots are interactive and should be played with. Change the scale / data with the dropdown menus, select the data to be displayed with the legend, and zoom-in by performing a left-click and drag, drawing a square or a vertical / horizontal line. Explore the upper-right corner of each plot to go through other possibilities such as toogling spikes lines. 

The code is maintained on [this repository](https://github.com/stephanefevrier/covid-19-analysis) in Python, on a Jupyter notebook.

# Disease propagation summary



Summary of the disease propagation since 22/01/20. Cases are compartmented into 3 categories: confirmed, deaths and recovered.

Before making conclusions from the data, two things need to be considered:
- Numbers are provided for informative purpose only and may differ from the official ones, although differences should be limited.
- Each country has a different way of counting the number of cases, making comparisons less relevant. The number of deaths should be the closest to reality, but is still an estimate.

## World

Overview of the COVID-19, world-wise. 

<!-- World indicators -->
<iframe width="100%" height="300" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/16.embed?showlink=false"></iframe>

Evolution of the number of total cases in the world. The bottom subplot gives the repartition between cases.

<!-- World scatter (total) --->
<iframe width="100%" height="600" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/164.embed?showlink=false"></iframe>

New cases each day. The percentage is calculated as the difference with the previous day. The bottom subplot gives the repartition between cases.

<!-- World scatter (delta) --->
<iframe width="100%" height="600" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/166.embed?showlink=false"></iframe>

## Per country

Overview of the COVID-19, country-wise. Switching the projection back to natural projection from orthographic may lead to some bugs on the plotly side.

See also the [evolution of COVID-19 deaths cases through time](/map_animated.html) (opening in a new window).

<!-- map -->
<iframe width="100%" height="600" frameborder="0" scrolling="yes" src="//plotly.com/~stephanefevrier/41.embed?showlink=false"></iframe>

Country-wise scatter plot. On the above, the total number of cases, on the bottom, the number of new cases each day. The interactive legend allows to isolate a specific country or a group of countries. 

<!-- scatterplot per country -->
<iframe width="100%" height="700" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/18.embed?showlink=false"></iframe>

# Exploratory data analysis

To explore the data in another way, the *violin plot* below gives shows the effect of age and gender on the possibility of dying of the disease. It is to be noted that the dataset used contains less that 1000 people. More details on the dataset used are given below the plot. 

A small correlation of the gender is seen (0.1), but the age seens to be a more influent factor (almost 0.3). Person correlation is used, meaning that the coefficient quantifies a linear relationship. 

<!-- violin plot death -->
<iframe width="100%" height="500" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/208.embed?showlink=false"></iframe>

To understand the data used for the violin plot, the 15 most represented countries in the dataset are presented through a Sankey diagram, where the relationship to Wuhan and the gender of each person are given. This diagram is not here to draw conclusions, but to understand the possible underlying biases present in the data, along with its distribution. 


What can be drawn from this diagram about the dataset used:
- the majority of the population presented is coming from Asia. 
- a huge proportion of the population is related to Wuhan, whether by travelling or living there. 
- a significant proportion of genders are unknown. 

These 3 biases need to be remembered when drawing conclusions from the violin plot, which therefore does not represent the world population. 

<iframe width="100%" height="800" frameborder="0" scrolling="no" src="//plotly.com/~stephanefevrier/277.embed?showlink=false"></iframe>
