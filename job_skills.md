# I am you and you are me: An educational, reproducible, parallel randomized controlled trial comparing a stakeholder enactment learning framework applied to job finding skill vs. control and its effect on knowledge, practice and learning experience

<!-- out of my shoes methodology -->


Andrea Scalco  
Morteza Charkhabi  
Bruno Melo  
Joao Ricardo Vissoci  
Ricardo Pietrobon  


## Abstract
<!-- write at the end -->

## Introduction

With the current economic crisis in Europe, and particularly in Italy, job finding skills are more important than ever. And yet, quality learning resources that adequately train students are scarce within academic environments. While the definition of quality learning in the context of job finding skills is mostly in the eyes of the beholder, most would agree that in order for a training to be satisfactory the learner should demonstrate skills that employers would judge of quality during the interview process. In other words, quality is mostly defined by the stakeholder judging the outcome of the job finding skills in the real world. Unfortunately, most learning frameworks do not attempt to have learners enact the stakeholders who are in charge of judging them.

* lit review on job skills online learning (test)
* lit review on role play and merrienboer

The objective of this educational, reproducible, parallel randomized trial is therefore to compare a stakeholder enactment learning framework intervention versus a control group in relation to knowledge, learning experience and impact in practice. We hypothesized that, compared to the control arm, the stakeholder enactment framework would significantly increase knowledge and experience.


## Methods

This trial was designed and reported in accordance with the recommendations provided by the [CONSORT statement](http://www.consort-statement.org/)

### Ethics
This study was approved by the Ethics Committe at the University of Verona ([Università degli Studi di Verona](http://www.univr.it)), informed consent having been waived since this was considered a research with minimal risk within an educational context. All participants were ensured that their participation was absolutely unrelated to their performance in their current disciplines and that they could drop out at any point if they so wanted.

### Trial Design

This is a parallel controlled randomized trial comparing a control group versus a stakeholder enactment educational framework comprehending a combination of two main components: (1) use of whole tasks according to the Complex Learning Instructional Design ([Merrienboer,]()) and (2) role play specifically focused on having job seekers playing the role of the stakeholders who would later evaluate their skills during a job interview. 

The trial involved 106 participants completing the trial <!-- replace by the actual number and describe dropout rate -->, randomized on a 1:1 ratio to the intervention and control arms, with the intervention and respective follow-up lasting a total of four weeks. No changes to the initially methods design were implemented while the trial was in course. <!-- need to check at the end whether this is true -->

### Participants
Our study involved 106 participants. Participants were students at the University of Verona and <!-- add -->, located in the Northeast part of Italy. For each participant we have collected information on gender, age, profession and previous educational background.

### Interventions


The "stakeholder enactment arm" arm was constituted by a short course with weekly video lectures, exercises and additional readings focused on a skills required for finding jobs. These areas included <!-- Andrea please add -->

The two main principles behind the intervention where Merrienboer's Complex Learning Theory <!-- ref --> and the Role Play educational theory <!-- ref -->. Briefly, Merrienboer's  Complex Learning Theory has among its principles the use of so called "whole tasks" <!-- add -->

Role play <!-- add -->

The way these two theories were combined in our stakeholder enactment intervention is described in detail in a separate publication (see [Pietrobon et cols, 2014]()), but below we provide the main workflow:

1. Provide a video and readings with supportive information on a specific aspect of job finding skills, such as <!-- add -->
1. Announcement that participants will take the role of job interviewers rather than of interviewees
2. A video demonstrates an actor playing the role of an interviewee providing answers to a number of standard interview questions
3. Subsequent items then asked the participant what in the interviewee's answers were errors, missing aspects and correct responses

Participants in the control arm were provided with readings on each of the topics.

All educational material for this course is made available within our Reproducible Research repositories, and delivered through the original [Open edX platform](http://code.edx.org/). Videos were provided in Italian. All remaining material is made available in Italian, although both Italian and English versions are provided within our Reproducible Research repositories (see subsequent section on Reproducible Research).

<!-- add CONSORT for Non-Pharmacological Treatment Interventions -->



### Outcome variables

Our study three main outcome variable categories: knowledge, learning experience and impact in daily practice, all described under the subsequent sections. Per CONSORT Statement guidelines, any eventual changes to outcome measures deviating from the initial plan and occurring throughout the trial were recorded in our versioning system ([Github](https://github.com/)), thus ensuring full reproducibility. However, changes were avoided unless strictly necessary.


<!-- get below from Gustavo's -->

#### Knowledge

#### Learning experience

#### Impact in daily practice


####  Sample size

Given the absence of preliminary efficacy data, we calculated our sample size based on an assumption of a two-sample t-test for an index representing the worst case scenario for each of the three outcomes, with an effect size of 55%, a significance level and statistical power set at the traditional levels of 0.05 and 80%, respectively. Under these assumptions the estimated required sample size is of 52.9 per group, which we have rounded to 53, ultimately leading to a total sample size of 106 participants in total. Taking into account a worst case scenario dropout rate of approximately 20%, we therefore planned to enroll 140 participants.


####  Interim analyses and stopping guidelines

Given the relatively short duration of our trial, we did not perform an interim analyses. In addition, given the low risk associated with the intervention, our guidelines did recommend that the trial be stopped only in case of an unlikely loss of confidentiality that might have compromised participants privacy, which has not occurred.

####  Randomization: sequence generation

All randomization schedules were delivered through [Planout](http://facebook.github.io/planout/) within the [edx Code](http://code.edx.org/) platform. Briefly, Planout makes use of a pseudorandom number generator from the [Python language](https://www.python.org/), which has been extensively tested. <!-- need ref --> Randomization was blocked at 10 participants, thus decreasing the likelihood of a possible imbalance.  Additional details are provided in a publication by our group <!-- ref -->

All randomization was delivered through the Open edX platform, thus ensuring that participants and investigators are blind to the allocation. Data analysts (RP and JRV) received a dataset from the computer scientist (BM) where the two randomization arms were designated by unspecific letters, thus ensuring that the analysis is also conducted in a blind fashion.


#### Statistical methods 

All analyses were conducted by the members in our team (RP, JRV). The data analysis started with an overall evaluation of individual variables to assess distributions for continuous variables (e.g., participant's age) in terms of their distributions, as well as the frequency/percentage for categorical variables (e.g., gender). 

Missing values were handled differently if they happened for individual variables or full encounters, e.g., an entire evaluation for a week. Individual variables were imputed starting by an exploratory visual analysis to better understand the potential underlying pattern behind missing values for each variable. This analysis was conducted using the [VIM package](http://cran.r-project.org/web/packages/VIMGUI/vignettes/VIM-Imputation.pdf) within the [R language](http://www.r-project.org/). Depending on the pattern of missing data, we then chose one of several alternatives, ranging from not imputing when the percent missing might be negligible, imputing using predictive models from variables that are hypothesized to be associated with the missing values (e.g., age predicting residency year), or multiple imputation in cases where missing patterns might be happening at random (MAR or missing at random) (@rubin1976inference). <!-- see 3d grant -->

We evaluated for potential confounding of the intervention effect by assessing balance across baseline variables between the 3D and control arms. This evaluation occurred for the overall study. While imbalances were unlikely given that we are using a series of preventive measures (blinding, concealed allocation, blocking and stratification), eventual imbalances were evaluated on an individual basis and required adjusting in our modeling strategy (see below for details).

The psychometric analysis for parallel validation of our scales started with an Exploratory Factor Analysis to evaluate the underlying dimensional structure of our item pool. We then conducted a Confirmatory Factor Analysis using the hypothesized domains (see Outcome Variable section for extensive details). Once domains are established we used Cronbach's alpha to measure internal reliability within each construct. Validity was measured by triangulation across different domains. 

Given that all of our outcomes have multiple endpoints over time, we used a combination of mixed models and survival analysis to measure the efficacy associated with the "better half toolkit" in comparison with the control arm. To formally test trends in each of our outcome variables over time we developed mixed models that account for multiple measures as random a effect. For each time period we also assessed differences in scores. These bivariate analyses incorporated robust standard errors to account for the clustering effect.


### Reproducible research
In order to follow a reproducible research protocol, we have written our manuscript while the project was ongoing, using the [Git]() versioning system and the [Github]() application. Specifically we used [Rmarkdown](), which combines the R statistical language with the [Markdown markup](http://daringfireball.net/projects/markdown/), ultimately allowing us to leave all calculations and data manipulation within the article text. All data sets and respective analytical scripts were provided in JSON (JavaScript Object Notation) in open public repositories including [Figshare](http://figshare.com/) and [Github](https://github.com/). In addition, we have also stored the version of the software used in this analysis and deposited it within our Github and Figshare repositories, ultimately decreasing the probability of problems during subsequent attempts to reproduce our analyses. <!-- add paper that recommends this procedure -->

## Results

<!-- add this section in alignment with CENT -->

## Discussion


<!-- http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0084118

http://kenexa.com/Portals/0/Downloads/KHPI%20Papers/Developing%20and%20Validating%20a%20Global%20Model%20of%20Employee%20Engagement.pdf

http://www.wilmarschaufeli.nl/publications/Schaufeli/290.pdf
 -->

<!-- 
http://www.psychologytoday.com/blog/career-transitions/201207/job-crafting
http://justinmberg.com/berg-dutton--wrzesniewski_j.pdf
http://www.compasspoint.org/sites/default/files/docs/Positive%20Organizational%20Scholarship%20Concepts%20and%20Resources.pdf
http://positiveorgs.bus.umich.edu/cpo-tools/job-crafting-exercise/
 -->
