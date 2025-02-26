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

# Task 2.4: Biochemistry and Oncology

## Description
This project involves analyzing protein mutation datasets using SIFT and FoldX scores to determine deleterious mutations. The analysis includes data merging, filtering, visualization, and interpretation of the impact of mutations on protein structure and function.

## Data Sources
The datasets used in this analysis are:
- **SIFT Dataset**: [sift.tsv](https://raw.githubusercontent.com/HackBio-Internship/public_datasets/main/R/datasets/sift.tsv)
- **FoldX Dataset**: [foldX.tsv](https://raw.githubusercontent.com/HackBio-Internship/public_datasets/main/R/datasets/foldX.tsv)

## Methodology
1. **Data Loading**
   - The datasets are loaded using `pandas`, ensuring correct tab separation.
   
2. **Data Processing**
   - A new column `specific_Protein_aa` is created by combining the protein and amino acid columns.
   - The datasets are merged on `specific_Protein_aa` to analyze mutations present in both datasets.

3. **Filtering Deleterious Mutations**
   - Mutations with `sift_score < 0.05` (high probability of being deleterious) and `foldX_score > 2` (destabilizing mutations) are extracted.

4. **Frequency Analysis**
   - The frequency of the first character of amino acids involved in deleterious mutations is calculated.

5. **Data Visualization**
   - Bar charts and pie charts visualize the frequency distribution of the affected amino acids.

## Visualization
- **Bar Charts**: Show frequency of amino acids involved in deleterious mutations for SIFT and FoldX datasets.
- **Pie Charts**: Represent proportional distribution of affected amino acids.

## Structural and Functional Analysis
### Glycine's Role:
- **Structural Role**: Glycine, being the smallest amino acid, provides flexibility in protein structures. It is commonly found in loops and turns.
- **Functional Role**: Essential for enzyme function and protein folding.
- **Impact of Mutations**: Mutations replacing glycine with bulkier amino acids can hinder flexibility, leading to diseases such as osteogenesis imperfecta.

## Key Findings
- Glycine (G), Leucine (L), Alanine (A), and Proline (P) are among the most affected amino acids.
- Hydrophobic amino acids (L, A, V, I, F, W) are crucial for protein core stability.
- Polar/charged amino acids (R, D, Y, S, T) influence enzymatic activity and protein interactions.
- Mutations in these amino acids can lead to protein misfolding, loss of function, or destabilization.

## Conclusion
- Amino acids involved in stability, flexibility, or enzymatic functions are functionally critical.
- Mutations in these residues are key targets in protein mutation studies due to their potential role in diseases.

## Dependencies
Ensure the following Python libraries are installed before running the script:
```bash
pip install pandas seaborn matplotlib
```

## Usage
Run the script using Python:
```bash
python script.py
```
This will generate the necessary visualizations and outputs for analysis.

## Authors
This project is part of the HackBio Internship program.

## License
This project is licensed under the MIT License.

