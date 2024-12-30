# Project Background
  
Diabetes is a prevalent chronic disease in the United States, affecting millions each year and posing serious health challenges. To better understand its risk factors, the Centers for Disease Control and Prevention (CDC) surveyed over 400,000 U.S. citizens about their lifestyles.

Early diagnosis is crucial, as it enables timely lifestyle changes and effective treatment. This report highlights key findings from the data analysis, aiming to identify indicators that can help predict diabetes risk and guide prevention efforts for individuals and public health officials alike.

This dataset pulls from the 2015 Behavioral Risk Factor Surveillance System (BRFSS) survey and consist of 253,680 response that were previously managed to have no null data point.

Some of the goals for this report includes:

- **GOAL 1**: Can survey questions from the provide accurate predictions of whether an individual has diabetes?

- **GOAL 2**: What risk factors are most predictive of diabetes risk?

- **GOAL 3**: Can we use a subset of the risk factors to accurately predict whether an individual has diabetes?
  
An interactive PowerBI dashboard can be downloaded [here]().

The Python code utilized to clean, organize and prepare data for the dashboard can be found [here](https://github.com/QuinnNgo97/Project-CDC-Diabetes-Health-Indicators/blob/73fd15dc9a8ff576926571ce21ee3db836652fe2/cdc_diabetes_report.py).

The original Kaggle dataset for perfoming this analysis can be found [here](https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset?resource=download).

# Data Structure & Initial Checks

The dataset contains 253,680 instances with no missing values, spanning 22 features related to lifestyle and health.
<div align="center">
  <img src="https://github.com/QuinnNgo97/githubtest/blob/56cbfcdf4d77bb9be078b58e522c7e29b2a31731/Dia01.png">
</div>

Prior to beginning the analysis, a variety of checks were conducted for quality control and familiarization with the datasets. The Python code utilized to inspect and perform quality checks can be found [here](https://github.com/QuinnNgo97/Project-CDC-Diabetes-Health-Indicators/blob/73fd15dc9a8ff576926571ce21ee3db836652fe2/cdc_diabetes_report.py).

# Excecutive summary

### Overview of Findings

The features in the dataset can be categorized into two subsets: Measured and Lifestyle. Preliminary observations suggest that the Measured data subset demonstrates greater accuracy in identifying diabetes among the survey respondents compared to the Lifestyle data.

Below is the overview page from the PowerBI dashboard and more examples are included throughout the report. The more interactive dashboard can be downloaded [here]().

<div align="center">
  <img src="">
</div>

