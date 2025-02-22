Josephine and Guille - Bioinformatics collaboration

## Project 1 ##
Two-Sample Mendelian Randomisation 🧬

25(OH)D -> Carotid artery plaque risk

R / Python / UNIX


# Steps #

- Mine GWAS-derived VCFs (exposure and outcome) - Bash script
- Python script -> VCFs -> TSV format
- R Script -> manhattan or scatter plots (X = chr, Y = -log10(P)
- Set SNP selection cutt-offs at P < 5e-08 
- Check for valid SNPs in exposure GWAS (i.e no overlap with outcome GWAS)
- Store SNPs on a CSV file

- Quality Control
- R Script
- Compure LD - r2 (r2 < 0.01) - LDLink package
- Check MAF < 0.01 (~1%)
- Scan for secondary phenotypes (PhenoScanner)
- Accumulate the remaining SNPs in CSV

- TWoSample MR
- R Script
- Run summary statistics for each SNP on exposure and outcomr
- Beta (causal effect), 95% CI, Pval
- IVW - OR - 95% CI - Pval
- WME - OR - 95% CI - Pval
- Check for Horizontal Pleiotropy
- MR-Egger regression + Stats
- Check for IVW and Egged heterogeneity
- Cochran Q coefficient and I2 statistic

- Data Visualisation
- R or Python
- Box plots
- Funnel Plot
- Regression plots (IVW, WM, and Egger)

- Pipeline automatisation
- Bash Script
