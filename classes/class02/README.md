# 500 Class 02: 2021-02-11

[Main Website](https://thomaselove.github.io/500/) | [Calendar](https://thomaselove.github.io/500/calendar.html) | [Syllabus](https://thomaselove.github.io/500-2021-syllabus/) | [Canvas](https://canvas.case.edu) | [Data/Code](https://github.com/THOMASELOVE/500-data) | [Sources](https://github.com/THOMASELOVE/500-2021/tree/master/sources) | Need Help? Email Us!
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :-----------: 
for everything | deadlines | expectations | zoom info, etc. | downloads | to read | `500-help` at `case dot edu`

## Materials for Today's Class

- Today's class will be held from **9:30 AM to 10:45 AM**. Dr. Love will open Zoom 10 minutes before and stay on until we run out of questions after the main session.
- Before class, please watch the pre-recorded lecture using the link on our shared Google Drive. This link is available now.
- The Slides for Class 02 are [available in PDF](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class02/500_2021_slides02.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class02/500_2021_slides02.Rmd).
    - The pre-recorded lecture slides are the first 72 in this deck. 
    - The deck continues with additional material that we'll discuss in our class session.
- As always, Dr. Love will be available for the 10 minutes before and 15 minutes after this session for informal "office hours". If you need help with anything, please email us!

## Announcements

1. All of [the talks from rstudio::global(2021)](https://rstudio.com/resources/rstudioglobal-2021/) are now available to watch.
2. A new monthly Zoom lecture series on social determinants of health, led by my colleague Dr. Ash Sehgal at [MetroHealth](https://www.metrohealth.org/) and the [Institute for H.O.P.E.](https://www.metrohealth.org/institute-for-hope) starts soon. [This two-page flyer](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class02/SDOH_Seminar_Series_2021_March_and_April.pdf) describes the sessions and speakers for 2021-03-01 (Laura Gottlieb) and 2021-04-05 (Rishi Manchanda).
3. The answer sketch for Lab 1 is now posted to our shared Google Drive.
4. A reminder that [Lab 2](https://github.com/THOMASELOVE/500-2021/tree/master/labs/lab2) is due next Thursday 2021-02-18 at 8 AM.
    - You'll be selecting a sample which should include some missing data, building a Table 1, building a logistic regression model, and then **repeating the process** with a revised sample after dealing with missing data. Then you'll add fitted probabilities from your logistic regression model to the data (probably using `augment` from the `broom` package, but not necessarily) and then visualize the results in an interesting way.
    - [Lab 0](https://github.com/THOMASELOVE/500-2021/blob/master/labs/lab0/README.md) and [the R-basics materials](https://github.com/THOMASELOVE/500-2021/blob/master/r-basics/README.md) can help here, in addition to [the Lab 1 sketch](https://github.com/THOMASELOVE/500-2021/blob/master/labs/lab1/README.md) when it becomes available.
    - Contact Wyatt and I if you need help at **500-help at case dot edu**.
5. It's not too early to start thinking about:
    - claiming an [Observational Studies In Action](https://github.com/THOMASELOVE/500-2021/tree/master/osia) article (due 2021-03-02)
    - developing a [project proposal](https://github.com/THOMASELOVE/500-2021/tree/master/project) (and identifying an available data set) (initial draft due 2021-03-09)
6. I recently purchased a copy of [Causal Inference: The Mixtape](https://www.scunning.com/mixtape.html) by Scott Cunningham. It looks really interesting, although I won't get into it seriously for at least another month. [The online version is available here](https://mixtape.scunning.com/).
7. Today we'll discuss Lucy D'Agostino McGowan's [February 2017 blog post](https://www.kdnuggets.com/2017/02/hill-data-scientist-xkcd-story.html) "[Causation or Correlation: Explaining HIll Criteria using `xkcd`](https://www.kdnuggets.com/2017/02/hill-data-scientist-xkcd-story.html)."
    - It was inspired by Roger Peng and Hilary Parker's [Not So Standard Deviations podcast, Episode 28](http://nssdeviations.com/episode-28-writing-is-a-lot-harder-than-just-talking).
8. The American Statistical Association has a new monthly podcast called [Practical Significance](https://magazine.amstat.org/podcast-2), meant to inspire listeners with compelling stories from statistics and data science and to propel data-driven careers forward with learning opportunities for all. The latest episode ([Episode 2](https://magazine.amstat.org/podcast-2/), entitled How to Become a JEDI) is about the ASA's Anti-Racism Task Force, and its outreach group to address justice, equity, diversity and inclusion (JEDI).
    - ASA's complete [roster of sponsored podcasts can be found here](https://magazine.amstat.org/blog/2021/02/01/asa-sponsored-podcasts/).
9. A new monthly Zoom lecture series on social determinants of health, led by my colleague Dr. Ash Sehgal at [MetroHealth](https://www.metrohealth.org/) and the [Institute for H.O.P.E.](https://www.metrohealth.org/institute-for-hope) starts soon. [This two-page flyer](https://github.com/THOMASELOVE/432-2021/blob/master/classes/class04/figures/SDOH_Seminar_Series_2021_March_and_April.pdf) describes the sessions and speakers for 2021-03-01 (Laura Gottlieb) and 2021-04-05 (Rishi Manchanda).
10. Boston University and the Society for Epidemiologic Research are hosting a 3 part webinar series called  "[Epidemiology and Race: Why and How We Study Racial Health Disparities](https://www.bu.edu/sph/conversations/uncategorized/part-1-epidemiology-and-race-why-and-how-we-study-racial-health-disparities/)". The sessions are on 2021-02-25 and 2021-02-26 and registration is required.
11. The [tidymodels ecosystem](https://www.tidymodels.org/) provides an excellent schematic for lots of statistical learning engines besides `lm`, even though I don't plan to use it (other than the `broom` package) in this year's 500 class. The [tidymodels book](https://www.tmwr.org/) by Max Kuhn and Julia Silge is great, and I just learned that Max Kuhn will be presenting at [a Cleveland R Meetup session on TidyModels from 6 to 7:30 PM on 2021-02-24](https://www.meetup.com/Cleveland-UseR-Group/events/273725112/). If you're interested, [go here to register (for free) and attend](https://www.meetup.com/Cleveland-UseR-Group/events/273725112/). The talk will also be recorded and archived on the [Cleveland R Users Group YouTube channel](https://www.youtube.com/channel/UC7C4YZ-9itQW7Nl4RVKDflg).


## References from Today's Class

Articles posted on our [Sources page](https://github.com/THOMASELOVE/500-2021/blob/master/sources/README.md)

- Cochran WG 1968 [The Effectiveness of Adjustment by Subclassification in Removing Bias in Observational Studies](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Cochran%201968.pdf) *Biometrics* 24, 205-213.
- Gum Patricia A Thamailarasan Maran Watanabe Junko et al. 2001 [Aspirin Use and All-Cause Mortality among Patients being Evaluated for Known or Suspected Coronary Artery Disease](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Gum%202001%20JAMA%20Aspirin%20Use%20Propensity%20Analysis.pdf) *JAMA* 2001 286(10): 1187-1194.
- Riederer Emily 2021 [Causal design patterns for data analysts](https://emilyriederer.netlify.app/post/causal-design-patterns/) blog published 2021-01-31.
- Women's Health Initiative Writing Group 2002 [Risks and Benefits of Estrogen Plus Progestin in Healthy Postmenopausal Women: Principal Results From the Women's Health Initiative Randomized Controlled Trial](https://jamanetwork.com/journals/jama/fullarticle/195120) *JAMA* 2002; 288(3):321-333. doi:10.1001/jama.288.3.321

Other articles I refer to in the slides, if you're interested in tracking down further details...

- Barrett-Connor E Estrogen and estrogen-progestogen replacement: therapy and cardiovascular diseases. *Am J Med* 1993 Nov 30;95(5A):40S-43S. doi: 10.1016/0002-9343(93)90381-x. [PubMed](https://pubmed.ncbi.nlm.nih.gov/8256794/)
- Burkman RT Collins JA Greene RA Current perspectives on benefits and risks of hormone replacement therapy. *Amer J of Obstetrics and Gynecology* 2001 185 (2): S13-S23. [PubMed](https://pubmed.ncbi.nlm.nih.gov/11521117/)
- Col Nananda F Eckman MH Karas RH et al. Patient-specific decisions about hormone replacement therapy in postmenopausal women. *JAMA* 1997 Apr 9;277(14):1140-7. [PubMed](https://pubmed.ncbi.nlm.nih.gov/9087469/)
- Craig Michael C Maki Pauline M Murphy Declan G M The Women's Health Initiative Memory Study: findings and implications for treatment. *Lancet Neurol* 2005 Mar; 4(3): 190-4. doi: 10.1016/S1474-4422(05)01016-1 [PubMed](https://pubmed.ncbi.nlm.nih.gov/15721829/)
- Espeland Mark A Rapp Stephen R Shumaker Sally A et al. Conjugated equine estrogens and global cognitive function in postmenopausal women: Women's Health Initiative Memory Study. *JAMA* 2004 Jun 23;291(24):2959-68. doi: 10.1001/jama.291.24.2959. [PubMed](https://pubmed.ncbi.nlm.nih.gov/15213207/)
- Shumaker Sally A Legault Claudine Rapp Stephen R et al. Estrogen plus progestin and the incidence of dementia and mild cognitive impairment in postmenopausal women: the Women's Health Initiative Memory Study: a randomized controlled trial. *JAMA* 2003 May 28;289(20):2651-62. doi: 10.1001/jama.289.20.2651. [PubMed](https://pubmed.ncbi.nlm.nih.gov/12771112/)
- Shumaker Sally A Legault Claudine Kuller Lewis et al. Conjugated equine estrogens and incidence of probable dementia and mild cognitive impairment in postmenopausal women: Women's Health Initiative Memory Study. *JAMA* 2004 Jun 23;291(24):2947-58. doi: 10.1001/jama.291.24.2947. [PubMed](https://pubmed.ncbi.nlm.nih.gov/15213206/)
- Stampfer MJ Willett WC Colditz GA et al. A prospective study of postmenopausal estrogen therapy and coronary heart disease. *N Engl J Med* 1985 Oct 24;313(17):1044-9. doi: 10.1056/NEJM198510243131703. [PubMed](https://pubmed.ncbi.nlm.nih.gov/4047106/)
- Stampfer MJ Colditz GA Willett WC et al. Postmenopausal estrogen therapy and cardiovascular disease. Ten-year follow-up from the nurses' health study. *N Engl J Med* 1991 Sep 12;325(11):756-62. doi: 10.1056/NEJM199109123251102. [PubMed](https://pubmed.ncbi.nlm.nih.gov/1870648/)
- Yaffe K Sawaya G Lieberburg I Grady D Estrogen therapy in postmenopausal women: effects on cognitive function and dementia. *JAMA* 1998 Mar 4;279(9):688-95. doi: 10.1001/jama.279.9.688. [PubMed](https://pubmed.ncbi.nlm.nih.gov/9496988/)
- Zandi Peter P Anthony James M Hayden Kathleen M et al. 2002 Reduced incidence of AD with NSAID but not H2 receptor antagonists: the Cache County Study. *Neurology* 2002 Sep 24;59(6):880-6. doi: 10.1212/wnl.59.6.880. [PubMed](https://pubmed.ncbi.nlm.nih.gov/12297571/)

