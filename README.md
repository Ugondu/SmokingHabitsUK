# Exploring Demographics of Smoking Population in United Kingdom.
![image](https://github.com/Ugondu/SmokingHabitsUK/assets/113315492/da0b793b-5d11-4568-961a-8bf73ed8203e)
## Table of Contents.
- [Problem Overview](#problem-overview)
- [Project Objective](#project-objective)
- [Data Source](#data-source)
- [Data Exploration](#data-exploration)
- [Insights and Findings](#insights-and-findings)
- [Conclusion and Recommendation](#conclusion-and-recommendation)
## Problem Overview.
Understanding the rampancy of smoking on public health remains a matter of concern to the public in the UK. This comes with significant implications for the individuals’ health and well-being as well as the NHS. To address these issues effectively, it is important to understand the factors that contribute to smoking behavior.
This project will focus on analysing smoke habits from a survey carried out in the UK to uncover patterns and relationships between demographics and smoking. Variables such as gender, age group, academic qualifications, region, ethnicity, nationality, marital status, and income level will help understand the demographic groups at higher risk of smoking. The findings will inform targeted interventions and initiatives aimed at reducing smoking and improving health outcomes in the UK.
## Project Objective. 
The aim of the project is to use Excel as analytic tool to perform a thorough exploratory data analysis on the available dataset, This project will focus on analysing smoke habits from a survey carried out in the United Kingdom to uncover patterns and relationships between demographics and smoking.
To achieve the objectives.
1.	What is the distribution of smokers across different age groups, genders, income levels, regions, nationality, average income, and ethnicity?
2.	What types of tobacco are most consumed by smokers from each demographic group in our survey?
## Data Source.
The datasets were made available by 10alytics data consulting team. 
### Data Dictionary
* Gender– Male or Female
* Age- Participant age.
* Marital Status – Whether participant is married, single, divorced, widowed.
* Highest Qualification – Educational qualification of Participants.
* Nationality– Participants home country.
* Ethnicity– Participants ethnic group.
* Gross Income– The amount each participant earns annually.
* Region– Geographical location of each participant.
* Smoke – If a participant smokes (Yes or No).
* Amount Weekday– Number of cigarettes a participant smokes in a weekday
* Amount Weekend – Number of cigarettes a participant smokes on a weekend.
* Type – Type of Cigarette each participant smoke.
## Data Exploration
To ensure that the dataset is ready for analysis, I carried out a process of data cleaning, removing errors, inconsistencies, inaccurate information, and text conversion. The following steps were taken to ensure the readiness of the dataset.
* A copy of the data set was created for manipulation, cleaning, data preprocessing and analysis.
* Duplicate rows were removed from the dataset using the “check duplicates” function.
* The dataset was checked for blank cells, and none was present.
After data cleaning, feature engineering was carried out to create new features/columns for ease of analysis.
* An age group column was created using the IFS formula.
=IFS([@age] <= 43, "Youth (<=43)", [@age ]<= 71, "Old (<=71)", [@age]>71, "Elderly (>71)")
* On the marital status column, all individuals without a partner were replaced as “Single” using the “Find and Replace” formula.
* The “Find and Replace” function was used to streamline all individuals with different degrees to “Degree” and those without to “No Qualification”.
* The “Find and Replace” was used to replace all “Refused”, and “Unknown” with “Other” on the Nationality, Ethnicity, Gross Income, and Region columns.
* A new column “Amt_weekly”, was created using =[@[amt_weekends]] +[`@[amt_weekdays]] to find the total number of tobaccos used in a week by each smoker.
## Insights and Findings.
* Of the participants who are smokers, female smokers made up 56% while Male smokers counted for 44% of the survey participants.
* With over 45% more than the next nationality, English participants accounted for most active smokers in the survey, while the least active smokers were the Irish with less than 1% of the survey participants. The bias seen could be because the survey was carried out in United Kingdom.
* The white ethnic group leads with over 99.9% of active smokers, significantly higher than other ethnicities. This can be attributed to the fact the survey was carried out in a predominantly White country. The Other, Mixed and Chinese ranks lowest among the ethnicities with less than 0.01% smokers from the survey.
* Single participants as expected had 66% of numbers who are active smokers over married participants. Individuals that are classed as low- income earners appeared to be most active smokers in the data available. 
* Active smokers are predominant (57%) in individuals who are between 16 and 43 years of age (Youth). As expected, the elderly (>71 years) are less likely to smoke. This could be due to underlying illnesses associated with old age.
## Conclusion and Recommendations
Public health campaigns and awareness should be targeted towards low-income earners, British nationals, and individuals of White ethnicity as they make up the highest population of smokers in the United Kingdom. Offering financial incentives or subsidies may be useful to individuals who are low-income earners,
