# Riiid! Answer Correctness Prediction

## Introduction

Education is one of the most challenging topics, especially recently during the COVID-19 pandemic. I see around myself many teachers and students have a hard time to teach and learn different topics in online classes.

In the traditional education systems normally teachers or instructors monitor and assess student’s knowledge based on their skills and abilities. In case students need more help or practice, their teachers would assist them. Imagining the situation that each student can trace her/his knowledge. Each student can obtain requirement skills based on her/his knowledge and abilities before moving to the next complex topic. In this way, students just spend their time to improve their weakness and get more attendance, engagement and individualized attention. Therefore, in modifying what students need in their next steps for learning, it is necessary to track, measure, and predict student’s changing knowledge, state, thereby personalizing the design. For having the more effective automated tutoring systems the student’s knowledge state should be modeled which is called knowledge tracing and replace the traditional ways that instructors use to assess the students’ performance with sequence of formative and summative learning activities. In knowledge tracing, machine learning algorithms help us to model student performance which has a high educational impact on automated tutoring systems.

Riiid Labs, an AI solutions provider delivering creative disruption to the education market, empowers global education players to rethink traditional ways of learning leveraging AI. With a strong belief in equal opportunity in education, Riiid launched an AI tutor based on deep-learning algorithms in 2017 that attracted more than one million South Korean students. This year, the company released EdNet, the world’s largest open database for AI education containing more than 100 million student interactions.


## Problem Statement
n this project, I am going to create algorithms for "Knowledge Tracing," the modeling of student knowledge over time. The goal is to accurately predict how students will perform on future interactions.

## Results :
In this notebook, I investigated different features that are able to affect students’ performance. For this reason, I considered the relation among the different variables and students' performance. Below I bring them in briefly. 
* Time spent on answering each question isn't related to correctness of the answers.

<img src="/pic2.png">

* Most of the students watched the explanation of the question when their answers were incorrect.
* As much as students answered more questions the number of the correct and incorrect answers increased.
* Number of wrong answers doesn't have any relation with total time spent watching lectures. 
* The number of the Lectures were watched has a direct relation with incorrect answers, which needs more investigation for the reasons.

For Modeling part,among all the models I have CatBoosting and LightBoosting have the best results.

|Algorithm |Accuracy |AUC |Time |
|-----------|----------|-----|------|
| XGBoosting | 69.32% | 67% |	11:50 |
|------------|--------|-----|-------|
| CatBoosting |	72.34% | 75% |	7:51 |
|-------------|--------|-----|-------|
| LightBoosting |	72.33% |	75% |	0:55 |
|---------------|--------|------|------|
| Multi Neural Network |	65.37% |	50% |	20:00 |
|----------------------|---------|------|-------|
| Embedding Neural Network |	65.94% |	50% |	2:00:00 |
|--------------------------|---------|------|---------|


<img src="/pic1.png">

<img src="/pic3.png"> 

## Future Works

* Evaluate students’ performance baise on different types of questions.
* Evaluate Lecture effect on correctness of answers
* Evaluate the background of students to the correctness of answers.
* Improving the prediction model by increasing AUC and Accuracy
