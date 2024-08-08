---
layout: project
title: "Effect  of  Zidovudine  Regimens  on  CD4   Count  over  Time"
overview: "Examining how the daily treatment with medication Zidovudine affects CD4 Counts in patients with AIDS. Conducted EDA, choose appropriate model, and preformed residual analysis."
---
![Housing Prices](/assets/images/project/CD4Counts.png)
[View Project File](/assets/files/CD4Count_AIDS.pdf){: class="download-button"}

<div class="dashed"></div>
Joint Effort with Ian Hu, and Cristobal Sanhueza


## Overview
Measuring the impact of four different Zidovudine treatments on the CD4 Counts in AIDS patients. We seek to compare the effects of these treatments:

- Treatment  1:  zidovudine  alternating  monthly  with  400mg  didanosine   

- Treatment  2:  zidovudine  plus  2.25mg  of  zalcitabine   

- Treatment  3:  zidovudine  plus  400mg  of  didanosine   

- Treatment  4:  zidovudine  plus  400mg  of  didanosine  plus  400mg  of  nevirapine   


## Domain Expertise
The data used for this project is based in the biomedical domain. Although we are not specialized in this domain, our professor provided context for this problem.  

Some important information to note:

 For this paper, we have defined advanced immune suppression to have CD4  counts of less than or equal to  50  cells/mm^3.
 
 Additionally, we will measure the impact on the log of CD4 Counts rather than CD4 counts. There are several reasons for measuring it this way- the normalization of the distribution among individuals over time and making it easier to handle the wide range of CD4 Counts. The results will then be correctly interpreted for CD4 Counts.


## Data Provenance
This data was provided in a clean format by our professor to complete this project. The variables included are:

- `id`: Unique identifier for each study participant.
- `treatment`:  With values range from 1 to 4, representing the four different treatments.
- `age`: The age of participants which is recorded numerically to the ten-thousandth place.
- `gender`: Gender identified as either "female" or "male".
- ` week`: A decimal value to the ten-thousandth place, ranging from 0 to 52, representing the week of the study.
- `log_cd4`: The log of CD4 counts, calculated to the millionth place.

We then converted `treatment` and `gender` to factors before beginning.

## Technical Stack
Completed in R using the `tidyverse,` `pander,` and `GGally` packages.


## Methods

- **Exploratory Data Analysis**- Explored interactions between variables and vs. time. Produced histograms, boxplots, and spaghetti plots.

- **Model Building**- Modeled using the full model with all the variables provided and tested it against three reduced models. Compared with ANOVA tests. Addressed nonlinearity, added random effects, and selected the best model. 

- **Prediction and Residual Analysis**- Compared predicted model to actual results. Examined residuals using QQ-plot, Mahalanobis Distance, transformed residuals, and a semi-variogram. Provided a visual for the finished results on our chosen model.



## Results
AIDS patients with advanced immunosuppression hoping to increase their CD4 count can have
the assurance that the daily regimen of zidovudine plus 400mg of didanosine or a daily regimen if
zidovudine plus 400mg of nevirapine, namely treatments 3 and 4, is predicted to have a net positive effect
on their CD4 count.


## Conclusion
Our model suggest that treatments involving zidovudine combined with other drugs (particularly treatments 3 and 4, including didanosine and nevirapine) show statistically significant improvements in CD4 counts over time compared to the baseline treatment of zidovudine alone.