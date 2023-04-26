# NAPLAN_Survey_Analysis
How did Year 9 students feel about the 2022 NAPLAN Numeracy test? I asked and have completed text analysis on their responses!

[![Made With](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com/images/badges/made-with-python.svg)

Author: Denneya Muscat

## Background 🖼️

NAPLAN. The annual assessment students in Years 3, 5, 7 and 9 sit nationwide. There are mixed feelings about NAPLAN, especially amongst parents and teachers. But how do the students feel? We've noticed results have been steadily declining, even after providing students with practice tests and regular NAPLAN style quizzes. After a discussion in the Mathematics faculty meeting, we decided since we would be seeing the Year 9 students straight after they finished their Numeracy NAPLAN test, it would be the perfect opportunity to survey them and see if there are other factors impacting their performance.

## The Survey 📋
Below is a data dictionary, providing a brief description of the types of questions we asked the students. 

# Data Dictionary

| Column | Description|
| :- | :- |
| feeling_rating | How the student was feeling on the day. 5 stars = Great, 4 stars = Pretty good, 3 stars = OK, 2 stars = Not good, 1 star = Terrible |
| low_star_reason | Reason for a 1 or 2 star rating |
| feeling_day_NAPLAN | How the student was feeling on the day about NAPLAN |
| difficulty | How the student found the numeracy exam |
| preparation | How the student prepared for the exam |
| easier_harder | Was the exam easier or harder than expected |
| impact | Was there anything that impacted student performance during the test |

## Data Cleaning 🧼

The following processes were necessary prior to beginning the analysis.
1. Deidentifying students.
2. Searching for null values
3. Fixing incorrect spelling in order for words to be counted as the same word.

## Data Exploration 🔍

1. Preview and shape of the data

### Preview

![Data Preview](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/data_preview.png)

### Shape
The dataset contained 149 rows and 8 columns.

2. Null values

31 students didn't answer the question asking why they gave a low star rating. This could be interpreted as only 31 students chose an average to high rating for how they were feeling on the day of the NAPLAN Numeracy test. It could also ben students ignoring/choosing not to answer the question.

3. Distribution of ratings
* 47% of students selected a rating of 3, meaning they felt "OK".
* 3% of students felt "Great" (5 stars).
* 6.7% of students felt "Terrible" (1 star).
* The ratings follow the shape of a Normal Distribution.

![Rating Distribution](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/dist_ratings.png)

## Text Preprocessing



