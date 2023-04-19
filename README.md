# Home Features Analysis
**Author:** Elimelech Berlin  
**Date:** March 2023

## Overview
This report analyzes available data to identify home features that have a correlation with home sale prices. Included in this data is both information about fixed aspects of houses such as location, year built etc., & features that can be modified e.g. living space, utilities. As this report aims to provide insight to professionals looking to modify properties to maximize home resale value, it focuses on features included in the latter category.  
From this report, several takeaways emerge regarding the following home features:
* Heating System
* Square-footage of space available for renovation
* Qualty of construction & design

## Business Understanding
Investors interested in buying homes, renovating them & reselling them at a profit, are presented with the following dilemma: of the modifications possible to apply to a given property, what sort of changes will increase the sale price of that property thus maximizing the return on their investment?  
This report analyzes the given dataset to identify where such investors would be advised to allocate their resources in an effort to boost home resale values.

## Data
The data examined in this report describes properties located in King County, Washington and comes from the King County Assessor Data Download available from the [King County Department of Assesments webpage](https://info.kingcounty.gov/assessor/DataDownload/default.aspx). _(Some of the properties are located outside of the county proper.)_
This dataset contains information about a variety of home/property features of about 30,000 properties. Features described include general details (location, view from the home etc.) as well as details about the actual structure and layout (square-footage, utilities etc.) of the properties.  
In creating this report the following two files were used:
* [kc house data.csv](https://github.com/terminalcoder/dsc-phase-2-project-v2-5/blob/main/data/kc_house_data.csv) contains the dataset 
* [column names.md](https://github.com/terminalcoder/dsc-phase-2-project-v2-5/blob/main/data/column_names.md) contains descriptive information about each column in the dataset

## Modeling
The `'price'` column of the dataset is set as the target variable & all other home features are the predictor variables.  
This model originally included about 30 predictor features (including some non-numerical ones that were converted via one-hot encoding), but was eventually reduced to less than half that amount because the coefficients for many of the features were found to be non-statistically significant & unreliable.  
In an effort to reduce some of the issues of this model failing to meet some of the assumptions of linear regression modeling, the target variable of the final model was log transformed.

## Regression Results
Several insights emerge from this model:
* Home price increases by .4% for every square-foot of living space
* Price of a home with a gas/solar heating source is typically 15% greater than a home with an electric heating source (reference category)
* A home with an Excellent grade construction & design is typically worth 30% more than a home with Substandard grade

## Conclusion
Based on the above insights, investors looking to turn a profit from flipping homes, are advised the following:
* Maximize the area dedicated as living space
* Install a gas/solar powered heating system
* Invest in Excellent grade construction & design in all home remodeling & renovation

## Limitations
The following points should be taken into consideration before applying any of the recomendations given in this report:
* The data used has been shown to fail to meet some of the assumptions for linear regression modeling; a different model may better explain the data.
* Regarding the grade of construction & design, a somewhat surprising pattern was revealed: homes with an excellent grade were shown to sell for more money than those with higher grades (luxury, mansion). Although not impossible, it should be the subject of further investigation to understand if there are other factors, unaccounted for in this report, that justify this fact.
* Although certain modifications/features have been shown to have a stronger affect on home price than others, this report doesn't consider the costs involved in making those changes. Any proposed changes must be subject to a cost-benefit analysis to determine what type of modifications are truly most lucrative.

## For More Information
Please review the full analysis in the Jupyter Notebook or the presentation.  
For any additional questions, please contact Elimelech Berlin, melech.berlin@gmail.com

## Repository Structure
```
├── README.md                                 <- The top-level README for reviewers of this project
├── Home Features Analysis.ipynb              <- Narrative documentation of analysis in Jupyter notebook
├── Home Features Analysis Presentation.pdf   <- PDF version of project presentation
├── data                                      <- Sourced externally
├── .gitignore                                <- files to ignore
└── images                                    <- Sourced from code
```




Overview
Business and Data Understanding
Explain your stakeholder audience here
Modeling
Regression Results
Conclusion
