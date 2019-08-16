---
title: "Final Project"
output:
  html_document:
    keep_md: TRUE
    highlight: pygments
    theme: cerulean
  pdf_document: default
  word_document: default
---

The course final is an individual project for which you will submit a written project report due May 18th. Everyone will have access to the same data, and the report will consist of five main parts: Introduction, Exploratory Data Analysis, Model Building, Model Interpretation, and Conclusion. The grading breakdown for these parts is listed below. While the techniques you use will be up to you, we do maintain that you include a multilevel component. 

The project will also consist of two in-class parts. Prior to class on May 3rd everyone will submit a draft of their exploratory data analysis. Similarly, prior to class on May 8th everyone will submit a draft including how they plan to approach the model building process and some initial model building steps. These does not need to fully reflect your final model. Class time both days will then be devoted to peer-review (we will determine partners). By the end of each day, you will need to submit a short 2-3 paragraph review for your partner. We will also be available for questions during class time. The aim is for these two sessions to help you get a solid start to the project.

---

## Grading

  -  30% Initial Drafts and Peer Reviews (due May 3rd and May 8th)
      - 15% In-class Drafts
      - 15% Submitted Peer-Reviews
  - 70% Final Report (due May 18th)
      - 5% Introduction
      - 15% Exploratory Data Analysis
      - 25% Model Building
      - 10% Interpretation of Model
      - 5% Conclusion
      - 10% Overall Writing

---

## Data and Research Question
The data sets you will use for this project are available on Canvas. The first data set gives information about police killings in the U.S. in 2015. This data is from fivethirtyeight, and a description is available at
<https://github.com/fivethirtyeight/data/tree/master/police-killings>. 
The second data set is the census information for the U.S. from the American Community Survey in 2015 <https://www.census.gov/programs-surveys/acs/>. Note that **geo_id** in the police data set corresponds directly to **CensusTract** in the ACS data set. The census data can also be pooled by county or state. 

Your project should focus on understanding factors that affect racial bias in police shootings. As you do your exploratory data analysis, you should think about what response you might use in your models to answer this question. One potential idea is to use logistic regression for which the response is race, but we are open to other ideas. You should know that we do not expect you to map the data, but you should include relevant figures. You may also use additional data sets to complement the two above, but this is not required or expected.





