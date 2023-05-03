# NAPLAN_Survey_Analysis
How did Year 9 students feel about the 2022 NAPLAN Numeracy test? I asked and have completed text analysis on their responses!

[![Made With](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com/images/badges/made-with-python.svg)

Author: Denneya Muscat

## Background 🖼️

NAPLAN. The annual assessment students in Years 3, 5, 7 and 9 sit nationwide. There are mixed feelings about NAPLAN, especially amongst parents and teachers. But how do the students feel? We've noticed results have been steadily declining, even after providing students with practice tests and regular NAPLAN style quizzes. After a discussion in the Mathematics faculty meeting, we decided since we would be seeing the Year 9 students straight after they finished their Numeracy NAPLAN test, it would be the perfect opportunity to survey them and see if there are other factors impacting their performance.

## The Survey 📋
Below is a data dictionary, providing a brief description of the types of questions we asked the students. 

### Data Dictionary

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

## Text Preprocessing ✏️

### 1. Visualisations 

Firstly, it was important to explore whether or not students were providing legitimate answers to the questions asked, rather than writing single word responses or gibberish. The insights provided summarise the findings from the average word count of how students were feeling on the day, their preparation for the NAPLAN test and what impacted them during the exam. Below are some visuals after exploring the average word count of how students were feeling on the day of NAPLAN, dependent on the feeling rating they first chose.

![Feeling Great](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/Wrdcnt_Great.png)
![Feeling Average](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/Wrdcnt_notgood.png)
![Feeling Bad](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/Wrdcnt_bad.png)

The following wordclouds were created showing the most common words used to desribe how students were feeling on the day and what impacted their performance in the exam.

![Feeling_wordcloud](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/feeling_wordcloud.png)
![Impact_wordclous](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/impact_wordcloud.png)

The bar charts show the frequency of the top 20 most used words in the feeling and impact responses.

![feeling_bar](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/feeling_bar.png)
![impact_bar](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/impact_bar.png)

**Insights**

Overall:
- the students who were feeling "Pretty Good" wrote the most for how they were feeling on the day of NAPLAN.
- the students who were feeling "Great" wrote the most for the difficulty of the exam.
- the students who were feeling "Not Great" wrote the most for preparation.
- the students who were feeling "Terrible" wrote the most for what impacted them during the exam.

### 2. Collocations

In order to identify any collocations in the data, the following preprocessing methods were performed:
1. New variable created
2. Removed capital letters and punctuation
3. Tokenized words
4. Defined stopwords
5. Added custom stopwords
6. Stored the good tokens in a new variable
7. Collocations: Bigrams, Trigrams, Quadgrams

Previews of this process are provided below, as well as the overall insights. The full process can be seen in the code file <a href= "https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/naplan_survey_2022.py">here</a>.

**Preview of the beginning process**
![Process_Feeling](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/preview_feeling.png)

**Bigrams of how students were feeling and what impacted them during the test**
![Feeling_Bigram](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/feeling_bigram.png)
![Impact_Bigram](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/impact_bigram.png)

**Trigrams of how students were feeling and what impacted them during the test**
![Feeling_Trigram](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/feeling_trigram.png)
![Impact_trigram](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/impact_trigram.png)

**Quadgrams of how students were feeling**
![Feeling_Quadgram](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/feeling_quadgram.png)
![Impact_Quadgram](https://github.com/Denneya/NAPLAN_Survey_Analysis/blob/main/impact_quadgram.png)

**Insights**

Overall:
- Students felt aggravated, annoyed, tired, anxious, stressed and bored on the day of the exam.
- A lot of students commented that this test doesn't go towards anything. This stood out as we're looking for reasons why results are decling. Are more and more students answering questions carelessly because they think this test is meaningless?
- When students were asked what impacted their performance during the exam, a lot of students said the lagging app, not remembering basic formulas, a negative mindset, clicking of other students' mouse, creaking floor and the student next to them. 
- In the quadgrams, the most common word associations regarded students with runny noses and that their laptops impacted their performance.
- Students also said the halfway time announcement really impacted their performance.








