HBB Variant Pathogenicity Prediction in Sickle Cell Disease

Project Proposal – Milestone 1

Student Names: Kantemir Tkhamokov, Zeynep Aykol

Course: ENS210 – Computational Biology

Date: 28.10.2026

Project Option: Option 1 – Rare Genetic Diseases

Topic: Sickle Cell Disease (SCD) – HBB gene

1. Project Objective

The objective of this project is to develop and evaluate a reproducible computational workflow for distinguishing likely pathogenic from likely benign variants in the HBB gene, which is associated with sickle cell disease (SCD). We will use clinically classified variants from ClinVar, population allele frequencies from gnomAD, and biological annotations to construct a labelled dataset. We will compare a simple rule-based baseline with selected existing prediction tools or a basic machine-learning classifier, depending on dataset size and quality. The final output will be a documented dataset, an analysis workflow, and an evaluation of prediction performance.

2. Background

Sickle cell disease is an inherited blood disorder caused by abnormal hemoglobin, which can lead to red blood cell deformation, anemia, painful vaso-occlusive episodes, and other complications. The HBB gene encodes the beta-globin subunit of hemoglobin. A well-known disease-associated variant is HBB c.20A>T, which produces the HbS hemoglobin variant (p.Glu7Val using precursor-protein numbering, commonly called Glu6Val in mature beta-globin numbering). SCD is typically inherited in an autosomal-recessive pattern.

Predicting variant pathogenicity computationally is challenging because clinical classifications may be uncertain or conflicting, datasets may contain unequal numbers of pathogenic and benign variants, and population frequency alone cannot establish whether a variant causes disease. Duplicate records and overlapping information between training and test sets can also lead to misleading performance estimates. Therefore, careful filtering, consistent variant annotation, and appropriate evaluation metrics are essential.

3. Data Sources

Source	What I will get from it
ClinVar	HBB variant identifiers, coding and protein changes, clinical significance classifications, review status, and supporting evidence. The initial dataset will include pathogenic/likely pathogenic and benign/likely benign variants.
gnomAD	Population allele frequencies for available HBB variants, used as biological features and for describing variant frequency.
OMIM	Background information on SCD, HBB function, inheritance, and the gene–disease relationship.
Ensembl Variant Effect Predictor (VEP)	Variant consequence and transcript annotations, if needed and available.
SIFT, PolyPhen-2, CADD, or REVEL	Available in-silico prediction scores for comparison or as candidate features, depending on data availability.
4. Methodology / Approach

Step 1: Build a workflow to classify HBB variants as likely pathogenic or likely benign and compare baseline predictions with selected computational methods.

Step 2: Retrieve HBB variant records and clinical classifications from ClinVar, supplemented with population frequencies from gnomAD and relevant annotations.

Step 3: Standardize variant descriptions, check for duplicates, and document inclusion and exclusion criteria. Keep variants with uncertain or conflicting classifications separate from the initial binary dataset.

Step 4: Create a labelled dataset containing clinical classifications and available features, including variant consequences, amino-acid changes, population allele frequencies, and prediction scores.

Step 5: Establish a simple rule-based baseline and compare it with selected existing prediction tools or a basic machine-learning classifier, depending on dataset size and label quality.

Step 6: Evaluate performance using accuracy, sensitivity, specificity, and Matthews correlation coefficient (MCC). Use a suitable training/test split where applicable and check for duplicate records and potential data leakage.

Step 7: Present the results in tables and figures, compare the methods, and discuss limitations such as class imbalance, uncertain clinical labels, and the limits of computational predictions.

By the end of the project, we expect to produce a reproducible HBB variant-analysis workflow, a documented dataset, and a performance evaluation; the predictions will be research outputs, not clinical diagnoses.

5. AI Tool Disclosure

ChatGPT was used to help organize and edit this project proposal. The students will verify scientific claims and data sources, review and test any AI-assisted code, and ensure they can explain all methods and results in the submitted work.

References

National Center for Biotechnology Information. (n.d.). ClinVar. https://www.ncbi.nlm.nih.gov/clinvar/
gnomAD. (n.d.). Genome Aggregation Database. https://gnomad.broadinstitute.org/
Online Mendelian Inheritance in Man. (n.d.). OMIM. https://omim.org/
Ensembl. (n.d.). Variant Effect Predictor. https://www.ensembl.org/info/docs/tools/vep/index.html
