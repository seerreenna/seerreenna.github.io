---
layout: project
title: "Analyzing Regional and National House Price Trends Over Time: A Bayesian Hierarchical Modeling Approach"
overview: "Understanding the impact national housing prices have on regional housing prices by using a nested bayesian method as an economic indicator."
---
![Housing Prices](/assets/images/project/HousingOverlaid.png)
[View Project File](/assets/files/BayesHousingPrices.pdf){: class="download-button"}

<div class="dashed"></div>
Joint Effort with Saanvi Shanka


## Overview
Understand the general impact of the Bayesian Hierarchal Modeling approach on modeling economic phenomena and potential gains. 


## Domain Expertise
This project addresses a classical econometrics problem using a Bayesian approach. The aim of this paper is to understand and explain the economic phenomenon, as is common in econometrics, rather than using the data alone to reach a solution. Knowledge in economic theory, as well as econometrics, was essential for this project.


## Data Provenance
The data was sourced from the Federal Reserve Economic Data (FRED). It is publically avalible for non-commercial use and offers clean and reliable datasets. We downloaded several data series including the average sales prices and median sales prices of houses sold for the Midwest, Northeast, South, and West Census Regions, and the United States as a whole, as well as the Consumer Price Index (CPI) for the United States. 

The data was pulled from FRED starting from 1975, and it was adjusted for inflation using CPI.


## Technical Stack
This project was completed entirely in R using `rstanram` for bayesian modeling and `tidyverse` for data manipulation.


## Methods
We modeled this using a nested data structure (regional prices nested within national prices) and included both random and fixed effects to capture the regional differences and overall trends. We checked diagnostic criteria such as posterior predictive checks and Rhat values to ensure our model was satisfactory.


## Results
Our analysis showed that *Time* and *national housing prices* has a significant influence on house prices, confirming that both factors are strong predictors. Regional differences did exist however, with some regions like the Northeast region showing lower prices overall compared to the others.


## Conclusion
We have demonstrated that using an advanced techinique such as Bayesian hierarchical modeling can offer more information and contribute to a better economic indicator. Further application of these techniques should be considered in future modeling of economic phenomena.
