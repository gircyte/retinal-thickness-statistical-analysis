# Is Retinal Thickness Associated with Cognitive Impairment in Parkinson's and Alzheimer's Disease?

The .pdf file attached to this repository is my Bachelor's degree dissertation, completed April 2020.
The goal of this project is to:
 - Showcase my proficiency with statistical data analysis - choosing the correct statistical approach & seeing it through.
 - Demonstrate my ability to approach a a problem and measure it through a process of a thorough literature review, data management & statistical testing.

## About Dataset

Data that was used in this study is a part of a larger machine-learning project called OCTAHEDRON, which aims to detect early signs of neurodegenerative diseases like Parkinson's and Alzheimer's using optical coherence tomography (OCT) scans of the retina. For more information, see [here](https://research.ncl.ac.uk/octahedron/).

## About Project

**GOAL**: Reduced retinal thickness has recently been indicated as a feature of mild cognitive impairment (PD-MCI) and dementia associated with Parkinson’s disease (PDD), as well as Alzheimer’s disease (AD). The present study aimed to identify retinal thickness differences in people with PDD, PD-MCI and AD, as well as to explore relationships between total mean retinal thickness and global cognition.

**HYPOTHESES**:
 1. Patients with mild cognitive impairment or dementia in PD and AD differ in mean retinal thickness compared to healthy controls, which predicts that PDD, PD-MCI and AD patients will exhibit reduced retinal thickness in contrast to controls.
 2. The pattern of retinal thinning is different in patients with PD compared to patients with AD.
 3. Retinal thickness is associated with global cognition in PD and AD, which predicts that as global cognition decreases, retinal thickness decreases as well.

**PARTICIPANTS & DESIGN**: This was a cross-sectional, between-subjects design study, recruiting 81 participants across four clinical groups: PD (n = 25); PDD/PD-MCI (n = 17); early AD/amnestic cognitive impairment (AD-MCI; n = 14); healthy, age-matched controls (n = 25). Retinal images were taken from the macular areas of the retina. An 8x8 volumetric grid of the retina was produced, leading to an investigation of 64 individual retinal areas. Then, mean retinal thickness in each of these 64 retinal areas was compared between the four groups of participants.
 - **Measured metric**: mean retinal thickness across 64 different points in the retina.
 - **Other variables**: global cognition scores.

## Statistical Analysis

 - Analysis was performed using IBM SPSS (Version 24.0.0.1)
 - **Normality testing** included:
   - Histograms - to visually examine the distribution
   - Boxplots - to identify symmetry & detect outliers
   - Q-Q Plots - again, visual inspection of quantile distribution
   - Shapiro-Wilk test - suitable for a sample size of 81 participants.
 - **Significance level** was considered to be α ≤ 0.05.
 - Statistical tests for normally distributed data:
    - **Single-factor ANOVA** since the design is between-subjects (4 different participant treatment groups and 1 independend variable).
    - Post-hoc testing: **independent t-test** since the design is between-subjects (4 different participant treatment groups and 1 independend variable).
 - Statistical tests for non-normally distributed data:
    - **Kruskal-Wallis H test**
    - Post-hoc: **Mann-Whitney U test**
 - For post-hocs, **Bonferroni's correction** was applied to minimise the risk to get Type I errors (α = 0.05/number of comparisons).
 - **Chi-squared test** was used to investigate possible gender differences between groups (due to the categorical nature of the gender variable).
 - Associations between individual retinal thickness data points and global cognition were examined by employing **Spearman’s correlation** (because global cognition scores present themselves as ordinal data).
 - To construct predictive models of global cognition, **hierarchical regression models** were employed.
    - **Backwards stepwise multiple linear regression analysis** was performed to identify a basic model predicting the global cognition score (removing the least significant predictors one at a time, with the global cognition socre as the only dependent variable)
    - Gender, age, years in education and motor symptom severity score were all entered into the basic model as possible predictors & covariates.
    - **Hierarchical backwards multiple linear regression analysis** was used to establish whether retinal thickness was associated with ACE-R total score (which also removes the least significant predictors one at a time, however, variables are entered in a hierarchic structure - basic model from the backwards stepwise multiple linear regression + retinal thickness variables).

## Discussion

 - As predicted, PDD and PD-MCI participants were discovered to exhibit significantly more pronounced retinal thinning than healthy controls or PD participants. However, no significant retinal thickness differences were observed in AD or PD participants. Therefore, the hypothesis that patients with mild cognitive impairment or dementia associated with PD and AD exhibit reduced retinal thickness compared to controls was only partially supported.
 - As no evidence of retinal thinning in AD patients was found, the hypothesis that retinal thinning patterns differ between PD and AD subjects was not supported.
 - Global cognitive functioning was found to be positively associated with retinal thickness in several different parts of the retina, although more so for PD, PDD and PD-MCI patients than for AD participants. No significant correlations were found in the control group. The hypothesis that retinal thickness is associated with global cognition in PD and AD was fully supported.
