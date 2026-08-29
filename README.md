# **Business Statistics Course: Generalized Linear Models (GLMs)** 📈



This repository contains detailed reports and analyses (in Italian- original folder, than translated in English) developed for the **Business Statistics** course at **Sapienza University of Rome**. The focus is on mastering **Generalized Linear Models (GLMs)** to address complex statistical challenges in business contexts. 

Each report is crafted with the utmost attention to detail, combining **technical rigor** with **clarity of communication**. Special emphasis is placed on producing **insightful visualizations** that enhance the interpretation and presentation of results. The work reflects a commitment to excellence, balancing advanced statistical methods with a polished narrative style.

## Project 1 : LOGISTIC

  This project studies what predicts a right-leaning political self-placement among US voters, using data from the 2020 ANES election survey. The analysis asks whether ethnicity is a determining factor in voting     
   preferences, and whether it remains so once income, gender, religiosity, education, marital status, generation, employment status, and social class are controlled for, through a logistic regression model.
   
   Key findings: white and African American respondents are the most conservative ethnic groups overall, but the relationship between income and conservatism is not uniform across ethnicities — the "richer means more
   conservative" pattern only holds for Caucasian voters, while among Asian, Hispanic, and African American voters it is the poorer respondents who lean more to the right. Religiosity is the single strongest predictor in
   the model.
   
   ### Technical challenges
   - **Rescaling continuous predictors** (income, religious importance) so that coefficients are comparable across variables with very different original scales.
   
  - 📄 [`vote-logistic.md`](./vote-logistic.md) — full write-up with all figures and the regression formula
  - 🖼️ [`images/`](./images) — figures from the original analysis
