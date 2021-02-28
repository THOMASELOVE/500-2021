# 500 Class 05: 2021-03-04

[Main Website](https://thomaselove.github.io/500/) | [Course Calendar](https://thomaselove.github.io/500/calendar.html) | [Syllabus](https://thomaselove.github.io/500-2021-syllabus/) | [Canvas](https://canvas.case.edu) | [Data and Code](https://github.com/THOMASELOVE/500-data) | Need Help?
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: 
for everything | for deadlines | expectations | zoom information | for downloads | email `500-help` at `case dot edu`

## Materials for Today's Class

- Today's class will be held from **9:30 AM to 10:50 AM**. Dr. Love will open Zoom 10 minutes before and stay on until we run out of questions after the main session.
- Before class, please watch the pre-recorded lecture using the link on our shared Google Drive, when it becomes available.
- The Slides for Class 05 are [available in PDF](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class05/500_2021_slides05.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class05/500_2021_slides05.Rmd).
    - The pre-recorded lecture slides are the first 41 in this deck. 
    - The deck continues with additional material that we'll discuss in our class session.
- The [dm2200 example](https://github.com/THOMASELOVE/500-data/tree/master/dm2200) demonstrates the use of several R packages to develop causal effect estimates using various types of propensity score matching. This example is a part of today's pre-recorded material, but I'm hopeful you'll be able to dip into it on your own as you need code to accomplish various types of propensity matching.
    - Noah Greifer's [MatchIt: Getting Started](https://cran.r-project.org/web/packages/MatchIt/vignettes/MatchIt.html) vignette
    - Noah Greifer's [Covariate Balance Tables and Plots: A Guide to the cobalt Package](https://cran.r-project.org/web/packages/cobalt/vignettes/cobalt.html) vignette
    - Jasjeet Sekhon's [Multivariate and Propensity Score Matching Software for Causal Inference](http://sekhon.berkeley.edu/matching/) describes the Matching package.
- As always, Dr. Love will be available for the 10 minutes before and 15 minutes after this session for informal "office hours". If you need help with anything, please email us!

## Announcements

1. Remember that your [Project 1 Proposal](https://github.com/THOMASELOVE/500-2021/blob/master/project/01_proposal.md) is due on **Tuesday** 2021-03-09 at 9 PM.
2. On 2021-02-25, Wyatt and I updated [the toy example](https://github.com/THOMASELOVE/500-data/tree/master/toy2021) and [the lindner example](https://github.com/THOMASELOVE/500-data/tree/master/lindner) to deal with the changes caused by an update to the cobalt package, mostly. I assume you got my email - if not, please let us know.
3. On 2021-02-26, I posted to the Shared Google Drive my comments on Paul Rosenbaum's *Observation and Experiment* including comments on all chapters other than the ones where you'll be writing [essays](https://github.com/THOMASELOVE/500-2021/blob/master/essays/README.md), starting with the Chapter 7 essay due on 2021-03-18. 
4. On 2021-02-28, Dr. Love updated the [dm2200 example](https://github.com/THOMASELOVE/500-data/tree/master/dm2200) which is included in today's pre-recorded lecture.

## Next Week

For Class 06 on 2021-03-11, we will again start at 9:30 AM. 

- The Class 06 pre-recorded lecture will focus on what can be learned from Don Rubin's 2001 paper entitled [Using Propensity Scores to help Design Observational Studies: Application to the Tobacco Litigation](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rubin%202001%20Tobacco%20Litigation%20article.pdf).
    - Please skim or read [the Rubin 2001 paper](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rubin%202001%20Tobacco%20Litigation%20article.pdf) before you watch the Class 6 lecture.

## Making a Plan for OSIA

Details to come.

## Additional Sources related to today's discusssions or slides

- Austin Peter C and Mamdani Muhammad M 2006 [A comparison of propensity score methods: A case study estimating the effectiveness of post-AMI statin use](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%20and%20Mamdani%202006%20case%20study.pdf) *Statistics in Medicine* 2006; 25: 2084-2106.
- Austin Peter C 2009 [Balance diagnostics for comparing the distribution of baseline covariates between treatment groups in propensity-score matched samples](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202009%20Balance%20Diagnostics%20after%20PS%20matching.pdf) *Statistics in Medicine* 2009; 28: 3083-3107.
- Austin Peter C 2011 [Optimal caliper widths for propensity-score matching when estimating differences in means and differences in proportions in observational studies](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202011%20Optimal%20caliper%20widths%20for%20PS%20matching.pdf) *Pharmaceutical Statistics* 2011; 10, 150-161.
- Austin Peter C 2011 [A Tutorial and Case Study in Propensity Score Analysis: An Application to Estimating the Effect of In-Hospital Smoking Cessation Counseling on Mortality](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202011%20Tutorial%20on%20PS%20Analysis.pdf) *Multivariate Behavioral Research* 2011; 46: 119-151.
- Austin Peter C 2014 [A comparison of 12 algorithms for matching on the propensity score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202014%20Comparing%2012%20PS%20matching%20algorithms.pdf) *Statistics in Medicine* 2014; 33: 1057-1069.
- Austin Peter C 2017 [Double propensity-score adjustment: A solution to design bias or bias due to incomplete matching](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202014%20Double%20PS%20Adjustment.pdf) *Statistical Methods in Medical Research* 2017; 26(1): 201-222.
- Austin Peter C 2014 [The use of propensity score methods with survival or time-to-event outcomes: reporting measures of effect similar to those used in randomized experiments](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202014%20PS%20models%20with%20survival%20outcomes.pdf) *Statistics in Medicine* 2014; 33: 1242-1258.
- Austin Peter C and Stuart Elizabeth 2014 [Moving towards best practice when using inverse probability of treatment weighting (IPTW) using the propensity score to estimate causal treatment effects in observational studies](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202014%20PS%20weighting.pdf) *Statistics in Medicine* 2015; 34: 3661-3679.- Austin Peter C 2014 [A comparison of 12 algorithms for matching on the propensity score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Austin%202014%20Comparing%2012%20PS%20matching%20algorithms.pdf) *Statistics in Medicine* 2014; 33: 1057-1069.
- Ho Daniel E, Imai Kosuke, King Gary and Stuart Elizabeth A 2007 [Matching as Nonparametric Preprocessing for Reducing Model Dependence in Parametric Causal Inference](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Ho%20Imai%20King%20Stuart%202007%20Matching%20as%20Nonparametric%20Preprocessing.pdf) *Political Analysis* 2007; 15: 199-236.
- Rosenbaum Paul E Rubin Donald B 1983 [The Central Role of the Propensity Score in Observational Studies for Causal Effects](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20and%20Rubin%201983.pdf) *Biometrika* 1983: 70(1); 41-55.
- Rosenbaum Paul E Rubin Donald B 1984 [Reducing Bias in Observational Studies Using Subclassification on the Propensity Score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20and%20Rubin%201984%20JASA.pdf) *JASA* 1984: 79(387): 516-524.
- Rosenbaum Paul E Rubin Donald B 1985 [Constructing a Control Group Using Multivariate Matched Sampling Methods That Incorporate the Propensity Score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20and%20Rubin%201985.pdf) *The American Statistician* 1985: 39(1): 33-38.
- Rosenbaum Paul E 2010 [Design of Observational Studies](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20PR%202010%20Design%20of%20Observational%20Studies.pdf)
- Rubin Donald B 2001 [Using Propensity Scores to help Design Observational Studies: Application to the Tobacco Litigation](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rubin%202001%20Tobacco%20Litigation%20article.pdf) *Health Services & Outcomes Research Methodology*
- Stuart Elizabeth A. 2010 [Matching Methods for Causal Inference: A Review and a Look Forward](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Stuart%202010%20Stat%20Science%20Matching%20Methods%20for%20Causal%20Inference.pdf) *Statistical Science* 2010; 25(1): 1-21.
