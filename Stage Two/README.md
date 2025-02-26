# Task Code 2.1

## Description
This script analyzes bacterial growth data by processing, visualizing, and statistically comparing the growth of wild-type (WT) and mutant (MUT) strains across three different strain types. The analysis includes data processing, growth curve visualization, statistical computations, and hypothesis testing.

## Repository Links
Below are the GitHub repositories containing implementations of this task:

- **Karimat**: [GitHub Link](https://github.com/hardae/hackbio-biocoding-internship/blob/main/stage%202/stage%202%20karimah)
- **Yustina**: [GitHub Link](https://github.com/Yustina-Mayunga/HackBio_coding_Internship/tree/main/Stage-two-task)
- **Chaimae**: *(Link not provided)*
- **Favour**: [GitHub Link](https://github.com/Fabs247/hackbio_biocoding_intern/blob/main/stage_2_task)
- **Joshua**: [GitHub Link](https://github.com/RagingThunder99/Hackbio-biocoding-internship/tree/main/Stage%20Two)

## Data Processing
- The script imports a dataset containing bacterial growth measurements.
- Metadata is created to map strain replicates to their respective conditions (WT or MUT).
- Data is restructured for analysis and visualization.

## Visualization
- Growth curves are plotted to compare WT and MUT strains across different conditions.
- Scatter plots and boxplots illustrate the time required to reach 80% of the carrying capacity.

## Statistical Analysis
- The time required for each strain to reach 80% of its maximum optical density (OD) is calculated.
- Normality tests (Shapiro-Wilk) determine whether the data follows a normal distribution.
- A T-test or Mann-Whitney U test is performed to assess statistical significance between WT and MUT strains.
- Results suggest no significant difference in growth between WT and MUT strains (p-value > 0.05).

## Interpretation
- Both WT and MUT strains exhibit similar growth trends.
- Time to reach 80% of carrying capacity remains comparable across most strains.
- Statistical analysis confirms that the mutations do not significantly affect bacterial growth.

This project provides valuable insights into bacterial growth patterns and statistical comparison methodologies in bioinformatics.

