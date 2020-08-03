# univariate-multivariate-model-in-biomarker-discovery

1. linear regression vs logistic regression vs Cox regression model:
linear regression for continuous outcomes, logistic regression for binary outcomes, and Cox regression for time-to-event outcomes.
a. a linear regression model is used to evaluate whether specific covariates are associated with continuous outcome. For such model, the effect size
   of each covariate is simply the estimated coefficient, i.e. the b terms;
b. a logistic regression model is used to evaluate whether specific covariates are associated wtih a binary outcome (0 or 1) that has no longitudinal aspect.
   The effect size of each covariate is typically provided as an odds ratio (OR) with 95% confidence intervals (CIs). OR will tell you the size of effect, and the
   p value will tell you the probability that your result is due to chance.
c. In cases where we are interested in the time to an event, particularly an event that may not be oberved within the follow-up perios (known as censoring),
   then a Cox proportional hazards regression model is commonly utilized. For example, a model to evaluate the association of baseline covariates on survival
   over 10-year follow-up in a cohort of patients undergoing CABG. The effect size is provided as a hazard ratio (HR) with 95% CIs.
d. Above 3 models are the most commonly utilized models, but there are other models available, such as ordinal regression models, accelarated failure time 
   models for time-to-even data, non-linear modelling for continuous outcomes, spatial modelling, and machine learning methods (e.g. random forests)
   
2. Univariable/multivariable univariate/multivariate regression model:
variate means outcome, variable indicates exploratory factor;
a. Univariate univariable regression model: a model with one outcome and one explanatory variable;
b. Univariate multivariable regression model: a model with one outcome and several explanatory variables;
c. Multivariate univariable regression model: a model with multiple outcomes and single explanatory variable;
d. Multivariate multivariable regression model: a model with multiple outcomes and multiple explanatory variables;

3. Prognostic factor: a situation or condition, or a characteristic of a patient, that can be used to estimate the chance of recovery from a disease or the chance of the disease recurring (coming back).

4.R package for implementing advanced multivariable regression modelling techniques.
  a. Linear regression: lm() function;
  b. logistic regression: glm() function with binomial family;
  c. Cox PH regression: coxph() function in 'survival' package;
  d. stepwise regression: step() function;
  e. Fractional polynomials: mfp() function in 'mfp' package;
  f. Splines: rcspline.eval() function in 'Hmisc';
  
5. Cofounding factor: a variable, other than the independent variable that you're interested in, that may affect the dependent variable. This can lead to   
   erroneous conclusions about the relationship between the independent and dependent variables. How to adjust cofounding factor (e.g. age and gender)?----
    fit <- lm (concentration ~ healthy + age + gender, data=mydf)
    
    
6. Usful website: http://www.sthda.com/english/wiki/cox-proportional-hazards-model


