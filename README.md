## Best Time to Buy High Speed Train Ticket in Spain
### Author: Brian Jankowitz
[Medium](https://medium.com/@JankowitzB) | [LinkedIn](https://www.linkedin.com/in/brian-jankowitz/)

#### [Project Presentation](presentation.pptx)
#### [Jupyter Notebook](/code/project_notebook.ipynb)

<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Problem-Statement" data-toc-modified-id="Problem-Statement-2">Problem Statement</a></span></li><li><span><a href="#Executive-Summary" data-toc-modified-id="Executive-Summary-3">Executive Summary</a></span></li><li><span><a href="#Model-Selection" data-toc-modified-id="Model-Selection-9">Model Selection</a></span></li><li><span><a href="#Conclusion" data-toc-modified-id="Conclusion-10">Conclusion</a></span></li><li><span><a href="#Recomendations" data-toc-modified-id="Recomendations-11">Recomendations</a></span></li><li><span><a href="#References" data-toc-modified-id="References-12">References</a></span></li></ul></div>

## Problem Statement

Buying a high speed train rail ticket can be just as tricky as buying an airplane ticket as prices fluctuate all the time based on multiple facotrs. The factors that make a high speed train ticket fluctuatte can be because of the time, the supply, and the demand. Other factors that decide the cost of a ticket can be because of it's class and ticket type.

Having prices vary so much, we are tasked with predicitng the ticket prices of the high speed train this way the company an inform their customers when the best time to buy a train ticket is.


## Executive Summary

[High Speed Train Dataset](https://www.kaggle.com/thegurusteam/spanish-high-speed-rail-system-ticket-pricing)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|insert_date|date|renfe|date data was scrapped|
|origin|object|renfe|departure city|
|destination|object|renfe|arrival city|
|start_date|date|renfe|departure date|
|end_date|date|renfe|arrival date|
|train_type|object|renfe|type of train|
|price|float|renfe|ticket price|
|train_class|object|renfe|ticket class|
|fare|object|renfe|type of fair|


Our goal is to accuratly predict high speed train prices this way the travel company can inform their customers when they should buy their train tickets.

This data came from Kaggle. The data was scrapped by the Gurus, a team of data scientists, and the data was uploaded onto Kaggle.
The data that we obtained came from Kaggle.

The metrics we decided to use are r^2 , Adjusted r^2 , and aboluste mean error. r^2  was decided as the primary metric because we wanted all the prices to be on the same scale. If a price is €10 but we predict €20, we more than double the price. If we a price is €200 but we predict €210, we are more accurate. We wanted everything to be on the same scale. Adjusted r^2  was looked at after as we wanted to look at every indepdent value. This was another was to check our model. The third metric that we looked at was Absolute Mean Squared. This was looked at as we wanted to see how accurate we are to our mean price.

By making a model to predict the high speed train prices in Spain, we were able to discover that certain features affect the ticket price as well as the time when you buy tickets.

When looking at the data, we wanted to use this data to make it into a time series model. However, when the data was analyzed more closely, it did not make sense to use this data to make a time series model. Instead, we focused on regression models to predict ticket prices. If this had been discovered very early on, we would have seen if we can get different data for our ticket prices. With little time left for this to be submitted, we were to far ahead with little time left that we had no choice but to continue. An assumption was made that the pricing system is very similiar to airline prices. High speed train tickets in Spain are priced the same way that airlines price their tickets.

## Model Selection

We decided to go with Decision Trees as our metric. This metric performed relatively the same compared to Bagging and Random Forest. Linear Regression performed the poorest. This model performed the best compared to those two and it took the least amount of time to run.


## Conclusions

We are able to predict the correct prices of a high speed train ticket in Spain 95% of the time. For the travel company, we are able to provide them a model that shows them that we can predict the prices which the travel company will be able to use to inform their customers when the best time to buy a train ticket is.


## Recommendations

I would recommend that data should be analyzed that containts the prices if a person buy a ticket one week in advance versus one month in advance. By having this data, we are able to predict when the customers should buy a ticket.

## Sources
-Adjusted r^2
 - https://www.programcreek.com/python/example/89256/sklearn.metrics.r2_score
 
-Spain graph using folium
 - https://python-visualization.github.io/folium/quickstart.html
