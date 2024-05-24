# STOR 320 Final Paper - Modeling FEMA Aid Distribution and COVID-19 Impact

## Introduction

This repository contains the final paper and analysis for the STOR 320 course, focusing on modeling and optimizing disaster response and aid distribution by the Federal Emergency Management Agency (FEMA). The paper explores two primary research questions:

1. **Predicting Aid Received**: Developing a model to predict the inflation-adjusted amount of aid received for disaster claims based on various factors.
2. **COVID-19 Impact**: Investigating the effects of the COVID-19 pandemic on the frequency and nature of FEMA biological disaster claims across different cities, and the relationship between aid received and the presence of elderly occupants in affected households.

## Data

The analysis utilizes a comprehensive dataset from FEMA's National Emergency Management Information System (NEMIS), containing applicant-level data for the Individuals and Households Program (IHP). The dataset spans from 2002 to April 27th, 2024, and includes various disaster types and geographic regions across the United States.

Key variables used in the analysis include:

- `ihpAmount`: Total financial IHP award for Housing Assistance and Other Needs Assistance.
- `fipAmount`: Applicant's Flood Insurance Premium amount.
- `declarationDate`: Date on which the disaster was officially declared.
- `incidentType`: Type of disaster (e.g., fire, flood).
- `damagedStateAbbreviation` and `county`: Geographic identifiers.
- `householdComposition`: Number of individuals affected in each household.
- `grossIncome`: Economic status of the applicants.

## Results

1. **Predicting Aid Received**:
  - A model with 19 predictor variables was developed to predict inflation-adjusted aid received.
  - The model achieved an R-squared value of 78.77% after variable selection, interaction terms, and transformations.
  - Cross-validation revealed a mean absolute error (MAE) of around $2,000, indicating accurate predictions for most zip codes.
  - Geographic Information System (GIS) analysis identified extreme data points (e.g., Hurricane Katrina) and provided insights into potential reasons for high aid received in certain areas.

2. **COVID-19 Impact**:
  - Analysis of biological claims showed spikes in COVID-19 claims coinciding with actual case spikes in different cities.
  - GIS analysis revealed that rural areas along the coast and in the mountains of North Carolina received a higher percentage of COVID-19 aid compared to urban and suburban areas.
  - A Poisson regression model was developed to predict the presence of elderly occupants based on COVID-19 aid received, but the model's performance was moderate, suggesting the need for additional predictors.

## Conclusion

The paper provides valuable insights into the patterns and effectiveness of FEMA aid allocation, highlighting distinct trends and potential factors influencing aid distribution. The developed models and analyses can inform future disaster response policies and strategies, allowing for more effective and equitable aid distribution.

Future work could involve incorporating additional variables, real-time data, and continuous optimization to enhance the predictive capabilities of the models, as well as further investigating the relationship between aid received and specific demographic factors across different geographic regions.

## Usage

The repository contains the final paper, data processing scripts, and modeling code used in the analysis. For detailed information on running the code and reproducing the results, please refer to the respective files and documentation within the repository.
