# Project Background
  
Diabetes is a prevalent chronic disease in the United States, affecting millions each year and posing serious health challenges. To better understand its risk factors, the Centers for Disease Control and Prevention (CDC) surveyed over 400,000 U.S. citizens about their lifestyles.

Early diagnosis is crucial, as it enables timely lifestyle changes and effective treatment. This report highlights key findings from the data analysis, aiming to identify indicators that can help predict diabetes risk and guide prevention efforts for individuals and public health officials alike.

This dataset pulls from the 2015 Behavioral Risk Factor Surveillance System (BRFSS) survey and consist of 253,680 response that were previously managed to have no null data point.

Some of the goals for this report includes:

- **Goal 1**: Can survey questions from the provide accurate predictions of whether an individual has diabetes?

- **Goal 2**: What risk factors are most predictive of diabetes risk?

- **Goal 3**: Can we use a subset of the risk factors to accurately predict whether an individual has diabetes?
  
An interactive PowerBI dashboard can be downloaded [here](https://github.com/QuinnNgo97/Project-CDC-Diabetes-Health-Indicators/blob/5d7eba803040f64734cf796473d06d038abdc3ea/CDC%20diabetes.pbix).

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

Among the 254,000 survey responses collected in 2015, 15.8% of participants were diagnosed with either diabetes or prediabetes. The data reveal that the likelihood of developing diabetes increases significantly from the age of 57, surpassing the risk observed in the overall population. Additionally, factors such as gender, income, and education show strong correlations with diabetes risk. High-income males are 50% more likely to develop a diabetic condition compared to their female counterparts, while individuals with lower educational attainment face even greater risks—those who have not completed high school are twice as likely to develop diabetes compared to those with higher levels of education.

Below is the overview page from the PowerBI dashboard and more examples are included throughout the report. The more interactive dashboard can be downloaded [here](https://github.com/QuinnNgo97/Project-CDC-Diabetes-Health-Indicators/blob/5d7eba803040f64734cf796473d06d038abdc3ea/CDC%20diabetes.pbix).

<div align="center">
  <img src="https://github.com/QuinnNgo97/githubtest/blob/0a66c0c66e304c97df169a5fb10b34992dff70f0/Dia02.png">
</div>

# 
Individuals with heart disease or related conditions are twice as likely to be diagnosed with diabetes compared to the general population. While scheduling a blood test can often be costly and challenging, the Body Mass Index (BMI), calculated using height and weight, serves as a valuable marker for diabetes risk. This is particularly useful in situations where professional medical examinations are not readily accessible.

An individual with a BMI of 25 and above will have gradually higher likelihood of developing diabetes.

<div align="center">
  <img src="https://github.com/QuinnNgo97/githubtest/blob/5b9477e4f7480ca44763e74ead03e95bf7ec4efc/Dia06.png" width="600" >
</div>

Additionally, self-perception of poor health or experiencing difficulty walking can also serve as effective indicators of a higher risk for diabetic conditions. These factors provide practical alternatives for assessing diabetes risk, particularly in situations where access to healthcare is limited.

<div align="center">
  <img src="https://github.com/QuinnNgo97/githubtest/blob/a116885ab01dd604c3444f6074819997138b24b8/Dia07.png" width="600">
</div>

### Goal 1:

Machine learning models were used to evaluate whether the survey data and questions could accurately predict an individual’s likelihood of having diabetes. Across five independent models, the predictions achieved an overall accuracy of approximately 72%. However, further analysis revealed that the models missed diabetic or prediabetic cases at a rate of 12%.

In medical contexts, the Total Allowable Error (TAE) is typically set at 6%, meaning the current models do not meet the regulatory standards required for a medical diagnostic tool.

<div align="center">
<p float="left">
  <img src="https://github.com/QuinnNgo97/githubtest/blob/9ebf8aad9a9219d7ae8aece1390ff2975488e1ca/Dia03.png" width="450" />
  <img src="https://github.com/QuinnNgo97/githubtest/blob/9ebf8aad9a9219d7ae8aece1390ff2975488e1ca/Dia08.png" width="200" /> 
</p>
</div>

### Goal 2:

The analysis process identified several risk factors with the strongest correlations to diabetic and prediabetic conditions, including sex, age, education, income, stroke, high blood pressure, high cholesterol, BMI, heart disease or heart attack, general health status, difficulty walking, and physical activity. These factors were found to be significant indicators in predicting the likelihood of developing diabetes.

### Goal 3:

To assess whether a smaller subset of the questionnaire could effectively predict whether an individual has diabetes, we divided the features into three logical subsets:

- **Group 1**: These features consist of demographic data or objective observations made by medical professionals.
- **Group 2**: These features are based on participants' self-reported data, reflecting their subjective experiences and perceptions.
- **Group 3**: Following data analysis, we identified the features with the strongest correlations to diabetic and prediabetic conditions. These features were selected for further model development.

The results show that the features from Group 3 outperformed the other groups, including the full feature set, by a small margin. This confirms that a subset of risk factors has been identified, which can effectively predict whether an individual has diabetes.

<div align="center">
  <img src="https://github.com/QuinnNgo97/githubtest/blob/9ebf8aad9a9219d7ae8aece1390ff2975488e1ca/Dia04.png" width="600">
</div>

### Recommendations:

- **Refine Model with Group 3 Features**: Focus on further optimizing the model using the subset of features identified in Group 3. This will enhance predictive accuracy and efficiency by reducing the feature set while maintaining performance.
- **Incorporate Additional Data Sources**: Explore the possibility of incorporating additional objective health data (such as medical records) or more granular self-reported data to further improve model accuracy and account for potential missing risk factors.
- **Validate with Larger, Diverse Datasets**: Test the model on a larger and more diverse dataset to ensure its robustness and generalizability across different demographics, regions, and medical backgrounds. This will help ensure the model's reliability in real-world applications.
