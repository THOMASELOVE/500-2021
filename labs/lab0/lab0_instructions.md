500 Lab 0 (An Example) with Instructions
================

Last Updated: 2021-01-26

## What Is This?

This is an example, which I’m calling Lab 0.

In earlier versions of this course, this was an actual assignment, as
described below. For the Spring 2021 course, I’ve decided to simply
provide it as a worked example. Looking it over should be helpful in
doing your work this semester, especially for those of you who aren’t
simultaneously taking another course with me.

I am making the following items available to you, in addition to these
instructions:

-   The `lab0` data set called `lab0.csv` (which is a comma-separated
    .csv file suitable for reading into R.) You’ll find this at [our
    500-data web site](https://github.com/THOMASELOVE/500-data).
-   An Answer Sketch for Lab 0, including both the [R Markdown
    file](https://github.com/THOMASELOVE/500-2021/blob/master/labs/lab0/lab0_sketch.Rmd)
    I used to create the sketch and the resulting [PDF
    file](https://github.com/THOMASELOVE/500-2021/blob/master/labs/lab0/lab0_sketch.pdf)
    it generates.

Your task for Lab 0 is to read over these materials, and see if they
help you answer the questions that arise in generating your responses to
your actual Lab assignments (Lab 1 - Lab 5) this semester.

## Load R Packages

To start, I’ll request that R sets its responses to be rendered without
the default pair of hashtags, as follows.

``` r
knitr::opts_chunk$set(comment = NA)
```

Next, I’ll load three R packages that will help me with these
instructions.

``` r
library(here)
library(Hmisc)
library(tidyverse)
```

# Original Instructions for this work

Here are the instructions I gave to students for whom this was a
required assignment.

This assignment requires students to analyze some data, and prepare a
report. That report should be in the form of a Word, PDF or HTML file,
along with an R Markdown file which allows me to completely replicate
the analysis.

1.  The files you develop should be named `YOURNAME-500lab0.Rmd` and
    `YOURNAME-500lab0.html`, please.
2.  Do professional work with this little problem. What do I mean by
    this?
    -   Properly labeled graphs/figures are a minimal expectation for
        graduate school.
    -   Use complete English sentences to describe your findings.
    -   Make sure that the answers include enough of the question that
        your text responses (in addition to the graphs) stand on their
        own. Be sure to address all three tasks.
    -   Present edited code, making an effort to delete false starts,
        and comment liberally. Don’t present R code without explaining
        what you’re doing in English. R Markdown makes it easy to
        intersperse code with explanations, so make that happen.
    -   Use words I know, without simply repeating my explanations
        verbatim, please.
3.  You are welcome to discuss Lab 0 with anyone, including myself, or
    your colleagues, but your answer must be prepared by you alone.
4.  If you are confused by the assignment, or stuck in the development
    of your response, please ask questions!

## The Data

The **lab0.csv** data file is available on [the 500-data web
site](https://github.com/THOMASELOVE/500-data).

The file includes 135 subjects, the first 40 of whom have received a
particular **treatment** and the remaining 95 of whom have not received
it.

-   Also provided are five meaningful predictors of treatment status,
    labeled (imaginatively) **cov1**, **cov2**, **cov3**, **cov4** and
    **cov5**.  
-   Covariates 1-4 are continuous covariates, gathered at varying levels
    of precision. The **cov5** variable is an indicator of whether the
    subject has a particular characteristic (1 = yes, 0 = no.)
-   Happily, there are no missing values in the data.

``` r
lab0 <- read_csv(here("data", "lab0.csv")) %>%
    mutate(subject = as.character(subject))
```


    -- Column specification --------------------------------------------------------
    cols(
      subject = col_double(),
      treatment = col_character(),
      cov1 = col_double(),
      cov2 = col_double(),
      cov3 = col_double(),
      cov4 = col_double(),
      cov5 = col_double()
    )

``` r
describe(lab0) # from Hmisc package
```

    lab0 

     7  Variables      135  Observations
    --------------------------------------------------------------------------------
    subject 
           n  missing distinct 
         135        0      135 

    lowest : 101 102 103 104 105, highest: 291 292 293 294 295
    --------------------------------------------------------------------------------
    treatment 
           n  missing distinct 
         135        0        2 
                                      
    Value      Not Treated     Treated
    Frequency           95          40
    Proportion       0.704       0.296
    --------------------------------------------------------------------------------
    cov1 
           n  missing distinct     Info     Mean      Gmd      .05      .10 
         135        0      133        1    48.36    11.83    30.70    34.36 
         .25      .50      .75      .90      .95 
       41.75    47.70    56.62    61.84    64.94 

    lowest : 27.03 28.30 28.39 28.73 29.60, highest: 66.37 67.30 67.89 68.39 73.28
    --------------------------------------------------------------------------------
    cov2 
           n  missing distinct     Info     Mean      Gmd      .05      .10 
         135        0      133        1    52.68    11.08    36.81    39.15 
         .25      .50      .75      .90      .95 
       46.48    53.48    59.99    65.39    67.05 

    lowest : 29.49 31.93 32.24 34.24 34.25, highest: 68.90 69.55 70.10 72.03 73.25
    --------------------------------------------------------------------------------
    cov3 
           n  missing distinct     Info     Mean      Gmd      .05      .10 
         135        0       24    0.995    20.28     5.87       12       14 
         .25      .50      .75      .90      .95 
          17       20       24       27       29 

    lowest :  8  9 11 12 13, highest: 28 29 30 32 33
    --------------------------------------------------------------------------------
    cov4 
           n  missing distinct     Info     Mean      Gmd      .05      .10 
         135        0       23    0.994    20.06    4.929       13       15 
         .25      .50      .75      .90      .95 
          17       20       23       26       28 

    lowest :  9 11 12 13 14, highest: 28 29 31 32 33
    --------------------------------------------------------------------------------
    cov5 
           n  missing distinct     Info      Sum     Mean      Gmd 
         135        0        2    0.735       58   0.4296   0.4938 

    --------------------------------------------------------------------------------

## Tasks

1.  Build a logistic regression model using the main effects of the five
    predictors to predict **treatment** status.
    -   Use R to add two columns to the data set, specifically the
        fitted probability (according to your logistic regression model)
        of being treated, and the linear component of the logistic
        regression model (i.e. the logit of the probability of being
        treated.)
2.  Next, summarize the resulting probabilities across the untreated and
    treated patients in an appropriate and attractive manner.
    -   Raw R code is rarely attractive on its face - build something
        brief, effective and appropriate for a presentation.  
    -   Of course, we’d expect that the average probability of being
        treated will be higher in the patients who are actually treated.
        Verify that this is the case, in a short **numerical and
        graphical** summary of your findings.
3.  How much overlap is there between the fitted probabilities of the
    treated patients and the fitted probabilities of the untreated
    patients?
    -   A **graph** of this overlap (perhaps a boxplot, but a better
        option would be a dot chart or density plot of some sort;
        creativity is welcome here) is crucial, supplemented by a short
        written description of your findings.

## A Hint for Task 1

Partial R code you might use to do this work follows…

``` r
m1 <- glm(treatment=="Treated" ~ 
              cov1 + cov2 + cov3 + cov4 + cov5,
          family=binomial(), data=lab0)

lab0$linpred <- m1$linear.predictors
lab0$prob <- m1$fitted.values

lab0 # note new columns
```
