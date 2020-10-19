# DATA 512 Assignment A2: Bias in Data
Author: Aboli Moroney
Date Created: 15-Oct-2020

## Purpose
The goal of this assignment is to identify potential sources of bias in a corpus of human-annotated data and describe some implications of those biases.
The analysis is performed the using the Jupyter notebook and all data, documentation, code and outputs are published in this GitHub repository for reference.

## Directory Structure
```
data-512-a2
│   README.md    
└───1-Data
│   │   data_aggression_annotated_comments.tsv
│   │   data_aggression_annotations.tsv
│   │	data_aggression_worker_demographics.tsv
|   |	data_toxicity_annotated_comments.tsv
|   |	data_toxicity_annotations.tsv
|   |	data_toxicity_worker_demographics.tsv
└───2-Analysis
|   │   hcds-a2-data-bias.ipynb
└───3-Outputs
|   │   Analysis1_CommentsReviewedbyGender.png
|   │   Analysis1_WorkersbyGender.png
|   │   Analysis2_PercentCommentsbyAge.png
|   │   Analysis2_WorkersbyAge.png
    
```

## Data Sources

Source data for Aggression and Toxicity in Wikipedia Talk project can be found on [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731) and the schema and descriptions can be found [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release).

The source data used for this analysis includes:
1. Aggression: 100k labeled comments from English Wikipedia by approximately 10 annotators via Crowdflower on how aggressive the comment was perceived to be along with some demographic data for each crowd-worker.
2. Toxicity: 160k labeled comments from English Wikipedia by approximately 10 annotators via Crowdflower on a spectrum of how toxic the comment is (perceived as likely to 	make people want to leave the discussion) to how healthy to conversation the contribution is.

Please visit the [Perspective API repository on GitHub](https://conversationai.github.io/) and [Wikimedia Research:Detox](https://meta.wikimedia.org/wiki/Research:Detox) to learn more about this project and its current applications.

## Analysis Research Questions
**Analysis 1: Analyze the demographic information about the Crowdflower workers that is available in the dataset** <br>

**Research Questions**
1. Is there fair representation of the different genders (male, female, other) in demographic profile of the crowdworkers who are labelling the comments as aggressive or toxic? 2. Do they fairly to represent the the general population?
Are the comments are being distributed evenly across different genders (male, female and other) for a fair labelling exercise?

**Exploratory Analysis**
1. The distribution of workers by gender who are labelling the comments datasets
2. The distribution of comments annotated by gender of the annotators

**Analysis 2: Explore relationships between worker age groups and labeling behavior** <br>

**Research Questions**
1. Is there fair representation of the annotators across all age groups?
2. Are younger labelers more or less likely to label comments as aggressive or toxic than older labelers?

**Exploratory Analysis**
1. The distribution of workers by age groups who are labelling the comments datasets
2. The percentage of comments by workers across different age groups that have been labelled as aggressive/toxic

The jupyter notebook containing the analysis code and outputs can be found [here](https://github.com/abolim/data-512/blob/master/data-512-a2/2-Analysis/hcds-a2-data-bias.ipynb)

## Outputs
The outputs for the exploratory analysis 1 and analysis 2 can be found in the [3-Outputs directory](https://github.com/abolim/data-512/tree/master/data-512-a2/3-Outputs)

## Licenses
Please refer the LICENSE file with [MIT LICENSE](https://github.com/abolim/data-512/blob/master/LICENSE) for understanding the code of conduct

