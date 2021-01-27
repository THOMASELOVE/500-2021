Lab 5 Instructions
================

Last Update: 2021-01-26

## Submission Details

Submit your work via [Canvas](https://canvas.case.edu/) by the deadline
specified in the [Course
Calendar](https://thomaselove.github.io/500/calendar.html).

## Data

Lab 5 returns to the `dig1.csv` data file we used in Labs 1 and 2. The
data remain available on the [500-data web
page](https://github.com/THOMASELOVE/500-data) as well as in the [data
folder](https://github.com/THOMASELOVE/500-2021/tree/master/labs/lab5/data)
above.

The idea here is to develop an analysis of the data in the DIG teaching
data set. Choose a population (based on the available DIG data or an
appropriate subset), outcome, a binary indicator of treatment/exposure
group and a set of between 10 and 30 covariates, then produce a R
Markdown and HTML file combination which addresses Tasks 1-5 below.

## Task 1.

Build and display an appropriate Table 1 comparing the treatment groups
on the covariates of interest.

## Task 2.

Build and describe an unadjusted analysis of the impact of the treatment
on the outcome. This should yield both a point estimate and uncertainty
interval.

## Task 3.

Build a complete analysis using propensity matching, including a balance
assessment pre- and post-matching, and an appropriate matched-set
estimate and uncertainty interval for the causal effect of treatment on
outcome, in the population you have defined, accompanied by a
sensitivity analysis if the results appear significant, and a smart
stability analysis if the results do not appear to be significant.

## Task 4.

Build a complete analysis using propensity weighting (and regression
adjustment, if you like), including a balance assessment pre- and
post-matching, and an appropriate propensity-weighted estimate and
uncertainty interval for the causal effect of treatment on outcome, in
the population you have defined.

## Task 5.

Build and describe (in complete English sentences) a comparison of the
results obtained from Tasks 2, 3 and 4. Describe any concerns you have
about the relative merits of your various causal effect estimates.
