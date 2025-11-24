# Summary: South Asian Cancer Cohort - Clinical and Genomic Analysis

This resource provides a notebook for downstream analysis of clinical and genomic data from South Asian cancer patients. The workflow integrates patient demographics, comorbidities, genomic variants, and association studies to provide insights into cancer prevalence, morbidity patterns, and genetic risk factors. The notebook combines data preprocessing, statistical analysis, and high-quality visualizations for publication-ready figures.

## Key Sections:

1. **Library Imports & Helper Functions**
   - Imports standard Python libraries for data manipulation, visualization, and file handling.
   - Defines utility functions for reading large CSV files in chunks, parsing dates, binning numeric values, and calculating quartiles.

2. **Cancer Dictionaries & Incidence Data**
   - Defines mappings for aggregated and individual cancer types.
   - Loads baseline cancer incidence and prevalence data.
   - Normalizes cancer type names and prepares datasets for analysis.

3. **Patient Demographics & Prevalence Visualization**
   - Analyzes gender distribution across cancer types.
   - Creates population prevalence barplots for male and female patients.
   - Generates ethnicity-genetic ancestry concordance visualizations.

4. **Comorbidity Analysis**
   - Loads and maps morbidity data.
   - Visualizes comorbidities by cancer type with lifetime vs. pre-diagnosis prevalence.
   - Performs significance testing for morbidity-cancer associations and generates Manhattan-style plots.
   - Summarizes top comorbidities and counts of significant associations.

5. **Genomic Variant Analysis**
   - Loads exome sequencing variant data, annotates consequences, and maps genes.
   - Processes GWAS summary statistics for multiple cancers.
   - Generates Manhattan plots for exome-wide significant variants.
   - Identifies clinically actionable variants (CGI hits) and evaluates gene panel efficacy.
   - Visualizes the proportion of impacted patients by variant consequence type.

6. **Gene-Based Association Studies (GEL Data)**
   - Aggregates logistic regression results across comparisons and cancer types.
   - Computes minor allele counts and filters low-frequency variants.
   - Identifies significant gene-level associations using case/control counts and p-values.
   - Produces filtered tables of significant gene associations for downstream analysis.

7. **PheWAS Analysis**
   - Processes multi-genotype PheWAS summary statistics.
   - Visualizes significant associations across phenotypes using Manhattan-style plots.
   - Highlights significant phenotype associations with text annotations.

8. **Output & Publication-Ready Figures**
   - Saves processed datasets and figures to designated `plot_path` and `text_path`.
   - Figures include barplots, stacked charts, Manhattan plots, and PheWAS visualizations with high-resolution formatting suitable for publication.

**Overall**, this notebook integrates clinical data, comorbidity profiles, and genomic association studies to characterize cancer risk and morbidity in South Asian populations, providing a foundation for downstream functional analysis and translational research.

## Prerequisites
- Python 3.9+

## Directory structure

## Input Folder Paths in Notebook

**result_path**: Directory containing input CSV/TSV files for comorbidities, prevalence, XWAS, PheWAS, and GEL results.

**plot_path**: Directory to save generated figures (publication-ready PNGs).

**text_path**: Directory to save processed tables and filtered gene/variant association files.

**manhattan_path**: Subdirectory for Manhattan plot-related ExWAS and PheWAS summary stastics files (only one provided for demonstration reason)


## Output Folder Paths in Notebook

**Figures**: Saved in plots/publication/ and subfolders.

**Processed Tables**: Saved in text/ for downstream interpretation.

## Usage

Create input and output directories and subdirectories as the respoitory.

Open and run the notebook SouthAsian_Cancer_Analysis.ipynb.

Figures and tables will be automatically saved to the designated paths.

## License
This project is provided for research purposes. Please cite appropriately when using data or figures derived from this analysis.


## Author

Abu ZM Dayem Ullah

Barts Cancer Institute

Contact: d.ullah@qmul.ac.uk

----



