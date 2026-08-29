# 📈 Business Statistics — Generalized Linear Models (GLMs)

Reports and analyses developed for the **Business Statistics** course at **Sapienza University of Rome**, focused on Generalized Linear Models (GLMs) applied to real-world business and social-science data.

Each report combines technical rigor with clear communication, with particular attention to visualizations that support the interpretation of results. Originally written in Italian (`italian/` folder) and translated into English for this repository.

## Contents

- [Project 1 — Logistic Regression: Political Self-Placement](#project-1--logistic-regression-political-self-placement)
- [Project 2 — Linear Regression: Income, Politics & Happiness](#project-2--linear-regression-income-politics--happiness)

---

## Project 1 — Logistic Regression: Political Self-Placement

**Data:** 2020 ANES election survey (US voters)

This project studies what predicts a right-leaning political self-placement among US voters. It asks whether ethnicity is a determining factor in voting preferences, and whether it remains so once income, gender, religiosity, education, marital status, generation, employment status, and social class are controlled for, through a logistic regression model.

**Key findings**
- White and African American respondents are the most conservative ethnic groups overall, but the relationship between income and conservatism is not uniform across ethnicities: the "richer means more conservative" pattern only holds for Caucasian voters, while among Asian, Hispanic, and African American voters it is the *poorer* respondents who lean more to the right.
- Religiosity is the single strongest predictor in the model.

**Technical challenges**
- Rescaling continuous predictors (income, religious importance) so that coefficients are comparable across variables with very different original scales.

📄 [`vote-logistic.md`](./vote-logistic.md) — full write-up with all figures and the regression formula

---

## Project 2 — Linear Regression: Income, Politics & Happiness

**Data:** European Social Survey (ESS) — France, Czech Republic, Hungary, Bulgaria

This project asks whether income drives differences in happiness levels across four European countries, and how that relationship changes with a respondent's political orientation. Since the ESS is observational rather than experimental, the analysis is framed in terms of association rather than causation.

**Key findings**
- Income has a positive effect on happiness everywhere, but the effect is strongest among far-left respondents and weakest among far-right ones.
- Among the wealthy, political orientation barely affects happiness; among the poor, conservatives report noticeably higher happiness than progressives.
- A second model finds a U-shaped relationship between age and happiness, with a minimum (peak unhappiness) around age 46.

**Technical challenges**
- Standardizing income and political orientation so that main effects and their interaction term are on comparable scales and can be meaningfully combined.
- Modeling age with a quadratic term (age and age²) to capture the U-shaped, non-linear relationship between age and happiness reported in the literature, rather than assuming a constant linear effect.

📄 [`poor-always-fare-worse.md`](./poor-always-fare-worse.md) — full write-up with figures and regression formulas

---
## Project 3 — Multiple Regression: The Gender Pay Gap

**Data:** 1985 Current Population Survey (US)

*"Женись стариком, никуда не годным... А то пропадет все, что в тебе есть хорошего и высокого"* — Leo Tolstoy, *War and Peace*

This project investigates the gender pay gap and its relationship with marital status, using a sample of US workers. It builds up from simple regressions (on sex alone, then on marital status alone) to a fully controlled multiple regression model with an experience–education–ethnicity–occupation set of predictors, to see how much of the raw wage gap survives once other conditions are held equal.

**Key findings**
- The raw gender pay gap is 21% (men $10/hour vs. women $7.90/hour on average), but the gap looks very different by marital status: only 1% among the unmarried, versus 29% among the married.
- All else equal, the "true" gender pay gap is 10% among unmarried individuals and rises to 24% among married ones — married men are the best-paid group overall, while married women are the worst-paid.
- Wages follow an inverted-U shape with experience, peaking around 29 years, and are also associated with education, ethnicity, region (South vs. North), and union membership.

**Technical challenges**
- Modeling experience with a quadratic term to capture the rise-then-plateau pattern of wages over a career.
- Interpreting a gender × marital-status interaction term, which requires computing the "effect" of one variable while holding a level of the other fixed, rather than reading the coefficients in isolation.
- Converting log-wage regression coefficients into interpretable "growth rates" (e^β − 1) for a model estimated on log(wage).

📄 [`gender-pay-gap.md`](./gender-pay-gap.md) — full write-up with all figures and regression formulas

---

## Repository structure

```
.
├── original/                    # original reports (Italian)
├── images/                     # figures used across all reports
├── vote-logistic.md            # Project 1 (English)
└── poor-always-fare-worse.md   # Project 2 (English)
```
