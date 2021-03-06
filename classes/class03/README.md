# 500 Class 03: 2021-02-18

[Main Website](https://thomaselove.github.io/500/) | [Course Calendar](https://thomaselove.github.io/500/calendar.html) | [Syllabus](https://thomaselove.github.io/500-2021-syllabus/) | [Canvas](https://canvas.case.edu) | [Data and Code](https://github.com/THOMASELOVE/500-data) | Need Help?
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: 
for everything | for deadlines | expectations | zoom information | for downloads | email `500-help` at `case dot edu`

## Materials for Today's Class

- Today's class will be held from **9:30 AM to 10:50 AM**. Dr. Love will open Zoom 10 minutes before and stay on until we run out of questions after the main session.
- Before class, please watch the pre-recorded lecture using the link on our shared Google Drive, when it becomes available.
- The Slides for Class 03 are [available in PDF](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class03/500_2021_slides03.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class03/500_2021_slides03.Rmd).
    - The pre-recorded lecture slides are the first 70 in this deck. 
    - The deck continues with additional material that we'll discuss in our class session.
- As always, Dr. Love will be available for the 10 minutes before and 15 minutes after this session for informal "office hours". If you need help with anything, please email us!

## Announcements

1. If you want to learn more about difference-in-differences analysis, I recommend https://diff.healthpolicydatascience.org/.
2. Class 4 next week will also be held from 9:30 to 10:50 AM.
    - The Class 4 pre-recording will be available soon, and will present (most of) an R example I've built called the [toy example](https://github.com/THOMASELOVE/500-data/tree/master/toy2021). You can review the code and results now.
    - The toy example uses simulated data, but Wyatt has prepared [the lindner example](https://github.com/THOMASELOVE/500-data/tree/master/lindner) which addresses many of the same issues using a real, albeit unrealistically clean, data set.
    - Wyatt will lead the Class 4 session. At that session, you'll be discussing Chapter 4 of Rosenbaum and Wyatt will also introduce the lindner example briefly, along with discussing any questions you have related to the pre-recorded lecture. You will be in excellent hands.
    - Dr. Love will be at AHRQ study section during Class 4, and will return for Class 5.

## References from Today's Class

References posted on our [Sources page](https://github.com/THOMASELOVE/500-2021/blob/master/sources/README.md)

- D'Agostino Ralph B Jr. 1998 [Tutorial in Biostatistics: Propensity Score Methods for Bias Reduction in the Comparison of a Treatment to a Non-Randomized Control Group](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/D'Agostino%201998%20SIM%20Tutorial%20on%20Propensity%20Scores.pdf) *Statistics in Medicine*
- Connors Alfred F et al. 1996 [The Effectiveness of Right Heart Catheterization in the Initial Care of Critically Ill Patients](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Connors%20et%20al%201996%20JAMA%20The%20Right%20Heart%20Catheterization%20Study.pdf) *Journal of the American 
- Gum Patricia A Thamailarasan Maran Watanabe Junko et al. 2001 [Aspirin Use and All-Cause Mortality among Patients being Evaluated for Known or Suspected Coronary Artery Disease](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Gum%202001%20JAMA%20Aspirin%20Use%20Propensity%20Analysis.pdf) *JAMA* 2001 286(10): 1187-1194.
- Hirano Keisuke and Imbens Guido W 2001 [Estimation of Causal Effects using Propensity Score Weighting: An Application to Data on Right Heart Catheterization](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Hirano%20and%20Imbens%202001%20Weighting%20in%20RHC.pdf) *Health Services & Outcomes Research Methodology*
- Hirano Keisuke, Imbens Guido W. and Ridder Geert 2003 [Efficient Estimation of Average Treatment Effects Using the Estimated Propensity Score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Hirano%20Imbens%20Ridder%20Efficient%20Estimation%20of%20ATE.pdf) *Econometrica* 2003, 71(4): 1161-1189. https://doi.org/10.1111/1468-0262.00442.
- Rosenbaum Paul E 2010 [Design of Observational Studies](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20PR%202010%20Design%20of%20Observational%20Studies.pdf)
- Rosenbaum Paul E Rubin Donald B 1983 [The Central Role of the Propensity Score in Observational Studies for Causal Effects](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20and%20Rubin%201983.pdf) *Biometrika* 1983: 70(1); 41-55.
- Rosenbaum Paul E Rubin Donald B 1984 [Reducing Bias in Observational Studies Using Subclassification on the Propensity Score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20and%20Rubin%201984%20JASA.pdf) *JASA* 1984: 79(387): 516-524.
- Rosenbaum Paul E Rubin Donald B 1985 [Constructing a Control Group Using Multivariate Matched Sampling Methods That Incorporate the Propensity Score](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rosenbaum%20and%20Rubin%201985.pdf) *The American Statistician* 1985: 39(1): 33-38.
- Rubin Donald B 2001 [Using Propensity Scores to help Design Observational Studies: Application to the Tobacco Litigation](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rubin%202001%20Tobacco%20Litigation%20article.pdf) *Health Services & Outcomes Research Methodology*
- Rubin Donald B 2004 [On principles for modeling propensity scores in medical research](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Rubin%202004%20editorial%20Pharmacoepidemiology%20and%20Drug%20Safety%20on%20Propensity%20Score%20Principles.pdf) *Pharmacoepidemiology and Drug Safety*
- Weitzen Sherry et al. 2004 [Principles for modeling propensity scores in medical research: A systematic literature review](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Weitzen%20et%20al%202004%20Systematic%20Literature%20Review%20of%20Propensity%20Score%20Usage.pdf) *Pharmacoepidemiology and Drug Safety*
- Weitzen Sherry et al. 2005 [Weaknesses of goodness-of-fit tests for evaluating propensity score models: the case of the omitted confounder](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Weitzen%20et%20al%202005%20Why%20goodness%20of%20fit%20tests%20aren't%20appropriate%20for%20evaluating%20propensity%20score%20models.pdf) *Pharmacoepidemiology and Drug Safety*

Other references in the slides, if you're interested in tracking down further details...

- Brookhart MA Schneeweiss S Rothman KJ Glynn RJ Avorn J Stürmer T Variable selection for propensity score models. *Am J Epidemiol* 2006 Jun 15;163(12):1149-56. doi: 10.1093/aje/kwj149. Epub 2006 Apr 19 [PubMed](https://pubmed.ncbi.nlm.nih.gov/16624967/)
- D'Agostino Jr. RB and Rubin DB Estimating and Using Propensity Scores with Partially Missing Data *JASA* 2000, 95(451): 749-759.
- McCaffrey DF Ridgeway G Morral AR Propensity score estimation with boosted regression for evaluating causal effects in observational studies. *Psychol Methods* 2004 Dec;9(4):403-25. doi: 10.1037/1082-989X.9.4.403. [PubMed](https://pubmed.ncbi.nlm.nih.gov/15598095/)
- Harrell FE *[Biostatistics for Biomedical Research](http://hbiostat.org/bbr/)*, specifically the [BBR Notes (pdf)](http://hbiostat.org/doc/bbr.pdf). 
- Lunceford JK and Davidian M 2004 Stratification and weighting via the propensity score in estimation of causal treatment effects: a comparative study. *Stat Med* 2004 Oct 15;23(19):2937-60. doi: 10.1002/sim.1903. [PubMed](https://pubmed.ncbi.nlm.nih.gov/15351954/).
