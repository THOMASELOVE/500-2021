# 500 Class 01: 2021-02-04

[Main Website](https://thomaselove.github.io/500/) | [Calendar](https://thomaselove.github.io/500/calendar.html) | [Syllabus](https://thomaselove.github.io/500-2021-syllabus/) | [Canvas](https://canvas.case.edu) | [Data/Code](https://github.com/THOMASELOVE/500-data) | [Sources](https://github.com/THOMASELOVE/500-2021/tree/master/sources) | Need Help? Email Us!
:-----------: | :--------------: | :----------: | :---------: | :-------------: | :-----------: | :-----------: 
for everything | deadlines | expectations | zoom info, etc. | downloads | to read | `500-help` at `case dot edu`

## Welcome to 500!

- Instructor: Thomas E. Love, Ph.D., Professor of Medicine and of Population and Quantitative Health Sciences, CWRU.
- TA: We are fortunate to have [Wyatt P. Bensken](https://wyattbensken.com/) as our teaching assistant. 
- Learn more about us in the [Syllabus](https://thomaselove.github.io/500-2021-syllabus/). Contact us at **500-help** at **case dot edu** with any questions.
 

## Materials for Today's Class

- Today's Slides are [available in PDF](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class01/500_2021_slides01.pdf), as well as in [R Markdown](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class01/500_2021_slides01.Rmd).

## Logistics and Reminders

1. You should have received an email with the subject heading "**PQHS / CRSP 500: Start of the Semester - Welcome!**" 
    - If you have this email, please attend to what it asks you to do. If you don't have this email, please let us know that now.
2. Please read the [Syllabus](https://thomaselove.github.io/500-2021-syllabus/) and familiarize yourself with the [Course Website](https://thomaselove.github.io/500), the Shared Google Drive (which you can see from your CWRU Google account as *500 Spring 2021 Dr Love and Students*), and [Canvas](https://canvas.case.edu/) so that if you have any questions or problems getting started, we can settle them quickly.
    - Questions should be posted to **500-help** at **case dot edu**, where Wyatt and I will see them. Wyatt is also available for office hours by appointment.
3. There's a Contact List in our Shared Google Drive now, based on the Welcome to 500 survey you completed. Please fix anything that's not correct.
4. [Lab 01](https://github.com/THOMASELOVE/500-2021/blob/master/labs/README.md) is due next Thursday 2021-02-11 at 8 AM.
    - To do this Lab, you'll need to have [R and RStudio up and running for you](https://thomaselove.github.io/500/software_install.html), and [download the data from our Data site](https://thomaselove.github.io/500/data_index.html).
    - I encourage those of you less familiar with R to look at both [the R-basics materials](https://github.com/THOMASELOVE/500-2021/tree/master/r-basics) I've provided, as well as the ["Lab 0" example](https://github.com/THOMASELOVE/500-2021/blob/master/labs/lab0/README.md).
5. The final word on all deadlines is the [Course Calendar](https://thomaselove.github.io/500/calendar.html). All deliverables for the entire semester are listed.
6. We expect you to attend all classes live via Zoom, to facilitate our discussions (which will be a bigger part of the second half of the course.) All 500 classes are video-recorded, and the recordings will be archived in the Zoom section of [Canvas](https://canvas.case.edu).
7. I want to remind you of the University's resources to help you that are listed in [Section 8 of our syllabus](https://thomaselove.github.io/500-2021-syllabus/university-resources-for-student-support.html), especially the newly available [CWRU Care 24/7 Mental Telehealth for Students](https://timely.md/faq/cwrucare/) program.

![](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class01/figures/lancet-tw01.PNG)

![](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class01/figures/lancet-tw02.PNG)

![](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class01/figures/lancet-tw03.PNG)

## Questions (with Answers) from the "[Welcome to 500 Survey](http://bit.ly/500-2021-welcome-survey)"

Thanks for completing the survey.

1. How much overlap of course material is there between 432 and 500? 
    - There isn't much overlap, really. The 500 course is more about designing observational studies than it is about statistical methods. There's a lot of R coding to make that happen, of course, and we'll use a lot of the tools we'll be developing in 432, particularly logistic regression, but we'll use them in a simpler and more straightforward way in 500 than in 432.
2. Will there be an in-person portion of the class at the end of the semester?
    - I had hoped that perhaps we could have the project presentation sessions in person. That's not going to happen now, since not everyone will be vaccinated by the end of the class.

## References from Today's Class

Articles posted on our [Sources page](https://github.com/THOMASELOVE/500-2021/blob/master/sources/README.md)

- Concato John et al. 2000 [Randomized, Controlled Trials, Observational Studies and the Hierarchy of Research Designs](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Concato%20Shah%20and%20Horwitz%202000%20OS%20vs%20RCTs%20and%20Hierarchy%20of%20Research%20Design.pdf) *New England Journal of Medicine*
- Gum Patricia A Thamailarasan Maran Watanabe Junko et al. 2001 [Aspirin Use and All-Cause Mortality among Patients being Evaluated for Known or Suspected Coronary Artery Disease](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Gum%202001%20JAMA%20Aspirin%20Use%20Propensity%20Analysis.pdf) *JAMA* 2001 286(10): 1187-1194.
- Smith Gordon C S and Pell Jill P 2003 [Parachute use to prevent death and major trauma related to gravitational challenge: Systematic review of randomized controlled trials](https://github.com/THOMASELOVE/500-2021/blob/master/sources/articles/Smith%20and%20Pell%202003%20BMJ%20Parachutes.pdf) *The BMJ*

You might be interested as well in [The Book of Why](http://bayes.cs.ucla.edu/WHY/) by Judea Pearl and Dana Mackenzie in 2018.

Other articles I refer to in the slides, if you're interested in tracking down further details...

- Multiple risk factor intervention trial. Risk factor changes and mortality results. Multiple Risk Factor Intervention Trial Research Group. *JAMA* 1982 Sep 24;248(12):1465-77. [PubMed](https://pubmed.ncbi.nlm.nih.gov/7050440/)
- [USPSTF Grade Definitions](https://www.uspreventiveservicestaskforce.org/Page/Name/grade-definitions) including links to definitions prior to July 2012.
- Veterans Administration Coronary Artery Bypass Surgery Cooperative Study Group. Eleven-year survival in the Veterans Administration randomized trial of coronary bypass surgery for stable angina. *N Engl J Med* 1984 Nov 22;311(21):1333-9. doi: 10.1056/NEJM198411223112102. [PubMed](https://pubmed.ncbi.nlm.nih.gov/6333636/)

## One Last Thing

Need help? Contact us at **500-help** at **case dot edu** with any questions. We want to hear from you!

![](https://github.com/THOMASELOVE/500-2021/blob/master/classes/class01/figures/phd_staring.PNG)

