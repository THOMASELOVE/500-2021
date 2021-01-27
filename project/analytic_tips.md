# Tips for Building Your Project Analysis

## The Main Propensity Score Analyses

I expect you to do (and present) two analyses using propensity scores. You will eventually be submitting a single R Markdown file that takes your original (perhaps after cleaning) data, and produces all of the analyses you will do. You will perform a first analysis that uses matching and a second analysis that uses weighting. 

For the matched analysis, you can use any form of propensity score matching: in most cases this will probably be 1:1 greedy matching, either without or with replacement. You are welcome to consider alternative matching strategies. 

For the weighted analysis, my preference is the use of an ATT approach with the linear propensity score included as an adjustor in the final outcome model after weighting – we'll call this a "double robust" analysis. Should that not be feasible for some reason, you may instead consider ATT weighting on the propensity score without the additional adjustment. I wouldn't use ATE weighting without checking with me first.

## On Coding Your Variables

I have some variables which I could code in several ways - for instance, I could code as "yes/no" for meeting a standard or I could code as "low/middle/high" in terms of severity or I could code as the continuous measured value? Which should I do?

- Always code everything in the least collapsed way possible at the start of building a data set. 
- You definitely want to build your data set using the data in the least aggregated (most granular) manner possible. It is always easy to collapse categories (taking low/middle/high to low vs not low, for instance) but it is always hard to expand them (taking low vs. not low to low/middle/high). 
- If any of your categorical variables are based on a continuous variable that you have also measured, then you should definitely include the continuous variable in your data set either instead of or along with the categorized version. Again, you can always get the categories again if you need them from the continuous results, but you can't go the other way. 

## What to do about missing data?

1. If you have missing data in an outcome, drop those cases.
2. If you have missing data in your exposure/treatment, drop those cases.
3. If you have missing data in a covariate or several but it affects less than 20 observations total, and also less than 10% of the sample size, then just drop them or impute them with single imputation. The simputation package is one good option.
4. If you have more substantial missingness in a covariate or covariates, so that more observations are affected than you are willing to drop, then:
    - Create an indicator (1 = value was imputed, 0 = value was observed) for each variable with substantial missingness. If age, for example, is missing, call this indicator age_im
    -  Then use simple imputation to impute the missing value for the missing cases for that variable. Call that age_full to indicate that you've imputed the data.
    - Include both age_full and age_im in your propensity score model, and balance on both. That way, you've balanced on whether a value was missing or not, and on the observed values, too.
    - To do the simple imputation, it's ok to impute with the simputation package (do something simple, like a robust linear model on a few predictors for a continuous variable or select an observed value at random, or impute according to the existing probabilities in observed data for a categorical variable.) Be sure to set a seed before imputing, so you can change that choice later, as part of a stability analysis.

I don't see any reason for you to do multiple imputation in your 500 project, and would not recommend it.

## Checking Balance

Don't use Rubin's Rule 3 in the project. That is all. Use a Love Plot and Rubin's Rules 1 and 2, in your matching and weighting analyses.

## Checking to See if Your Propensity Scores are Too Close to Zero or One

We will worry if a propensity score value is below 0.01 or above 0.99. If that happens to you, contact me, quickly. If just one or two subjects fall in that range, we may wind up just dropping them from the study. If more fall in that range, we will have to look for variables included in your covariate list that either alone or in combination with other covariates, determine the treatment group perfectly. The simplest check is to get a summary of the bottom few and top few propensity score values within each treatment group, perhaps with the `describe` function in the `Hmisc` package. 

Check also that each covariate has a non-explosive and non-missing point estimate and confidence interval. If any of this is not the case, you likely have a covariate that completely separates the treatment group from the control group. Such a variable should not be in your propensity model. Or it may be that you have two extremely collinear covariates in the PS model, in which case you can see that via VIF. The best way I have to fix this problem (if it's not obvious what to drop using other means) is to build the propensity model one predictor at a time until you find the covariate (or covariates) that causes the PS model to blow up. So that would be the first thing I suggest you try.

## Squared Terms or Product Terms in a Propensity or Outcome Model

Suppose you decide you want to include Age as a covariate in your propensity or outcome model, and also account for the notion that Age might have a non-linear relationship with what you're trying to predict, or just for the notion that Age is an especially important continuous covariate to balance well. So you decide, as a result to include Age and Age squared in your model. Try this...

1. Find the average `age` for all subjects. If some subjects don't have an `age`, impute first.
2. Subtract that average `age` from each subject's `age` to create a new variable, called centered age. If the overall average age was 50, and the first subject's age was 53, then that subject's centered age would be 3. If the second subject was 44, then centered age would be -6.
3. Create a new variable containing the square of the centered age for each subject.
4. Include the centered age (I usually call this `age.c`) and its square (`age.c2`) in your outcome model or propensity model, in place of the original ages.

If you're including an interaction between a binary indicator and a continuous variable in a model for the purposes of the project, I would simply create a product term and include that. Include a product term if you have reason to believe there is a meaningful interaction between the variables.

## What if 1:1 greedy matching without replacement doesn't work well?

If your 1:1 match without replacement doesn't produce enough of an improvement in covariate balance (by Rubin's Rules or by a Love plot) to make you happy, then consider 1:1 matching with a caliper, or 1:1 matching with replacement. In most cases, one (or both) of those strategies should help.

As mentioned previously, if you have roughly equal numbers of subjects in your "intervention" and "control" groups, then 1:1 matching won't work very well (unless, perhaps, you do it with replacement) so you may wind up needing to consider other matching approaches that we will demonstrate over the course of the semester.


