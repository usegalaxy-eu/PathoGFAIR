# Foodborne-Project-Data-Analysis

This Github repository is created as part of Foodborne pathogens detection project under the fund of [EOSC life industry call 2021](https://www.eosc-life.eu/industrycall/), where we give the user more ideas using Jupyter notebooks to perform more analysis to the output results of the Galaxy workflows created.

We have created 5 Galaxy workflows and published them on the [IWC](https://dockstore.org/organizations/iwc), where we analyze microbiome nanopore datasets and identify all possible pathogens and track them amoung all samples. The workflows are created to be scalable to any other type of sequencing technique as well as agnostic such that it can detect all possible pathogens without specifying any pathogen species or giving any information about the input samples to the workflows. The 5 workflows are:

- **Pre-processing**: where the quality controlling, reads trimming for quality retaining, host sequences removal and other contaminating sequences removal takes place
- **Taxonomy Profiling**: where taxonomy profiling take place identifying and visualizing our samples' community abundances down to the subspecies level
- **Gene-based Pathogeneic Identification**: where we identify all possible pathogens by identifying all the Virulence factors (VFs) genes and their specific locations, we also perform more analysis by identifying the MLST scheme for all the samples and the AMR genes
- **SNP-based Pathogeneic Identification**: where we identify all the SNPs and and create the consensus sequences of all samples
- **All Samples Analysis**: where we visualize the outputs of the pathogens drawing a heatmap of all the found pathogenic genes for all samples, and phylogenetic trees relating samples together per common pathogenic genes found

## Analysis Jupyter Notebooks in this Repository

In this repository we have included 4 different Jupyter notebooks that extract the output tabulars of the identified VFs and AMR genes created after running the **Gene-based Pathogeneic Identification workflow** in a given Galaxy history and create different visualization plots other than the ones created in the **All Samples Analysis workflow** to give the user more ideas and options to analyse their samples and generate more visualization figures using more plotting existing libraries. 


The inputs to these notebooks are only the history ID where the workflows finished running in, and the Metadata tabular of the samples.
