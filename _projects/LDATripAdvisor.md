---
layout: project
title: "Measuring the Impact of Text Summarization Before Topic Modeling on Travel Reviews"
overview: "Understanding the impact of text summarization for the improvement of Topic Modeling using LDA; applied to Travel Reviews"
---
![Housing Prices](/assets/images/project/Topic_diff.png)
[View Project File](/assets/files/LDATripAdvisor.pdf){: class="download-button"}
Joint Effort with Atharva Deodhar, Nilabjya Ghosh, and Joshua Michael Tucker

## Overview
We aimed to test whether the the summarization of text before preforming Latent Dirichlet Allocation,LDA, would have a significant impact on the results of the generated topic models.

## Domain Expertise
Before beginning, we conducted a small-scale literature review on our topic of LDA, focusing on its mathematical foundation and application to communication research. Additionally, we reviewed some of the applications others have attempted on our dataset. 

## Data Provenance
We sourced this data from kaggle, and was provided preprocessed with the special characters and stop words already removed. This dataset contains over 20,000 reviews and ratings for various hotel from the trip advisor website. The variables included are:

- `Review`: The review text for each hotel. The average size for a review is about 700 characters.

- `Rating`: The 1 to 5 rating (often denoted as stars) given for the given hotel by the reviewer. 

## Technical Stack
We used **Python** to build this project using the packages `gensim`, `spacy`, `WordCloud`, and `pyLDAvis`. 

## Methods
We summarized the text reviews using adapted code from  user Sandy M. on Medium to conduct our text summarizations. The result is a summarized review that keeps the main concept and crucial details but is not represented in plain english. 

We then modeled both the summarized reviews and full reviews using `gensim`. We then compared similarities within, and between the models using a heatmap. Finally, we visualized the model structure and learning objective measured with log likelihood and perplexity, and word cloud and word count respectively. 

## Results
We ultimately found that summarization did significantly impact the topic models generated. The summarized dataset produced vastly different topics from the full reviews, with them only one topic in common.

## Conclusion
Summarizing reviews may significantly impact the topics produced by LDA. Our research has showed that summarizing reviews to non-english words may skew the perceived topics of the same review. Further research is needed to dive deeper into the overall cost-benefit of using this method for the purpose of topic modeling on reviews. 
