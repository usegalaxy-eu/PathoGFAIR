# PathoGFAIR: Galaxy FAIR and Adaptable Workflows for Pathogen Detection and Tracking

## Overview

Welcome to the GitHub repository for the Foodborne Pathogen Detection and Tracking Project under the fund of [EOSC life industry call 2021](https://www.eosc-life.eu/industrycall/). This project aims to provide a comprehensive solution for the identification and tracking of (foodborne) pathogens using metagenomic (Nanopore) sequencing data. The workflows are developed using Galaxy, an open-source platform for FAIR data analysis.

![plot](docs/figures/Fig1_complete_workflow.png)

## Project Structure

- **Workflows:** The core of this project consists of a series of Galaxy-based workflows collectively known as PathoGFAIR. These workflows are designed for processing Nanopore sequencing data, detecting pathogens, and tracking their presence across samples. Workflows are available via the Galaxy Intergalactic Workflow Comission [IWC](https://dockstore.org/organizations/iwc)

	PathoGFAIR consists of 5 workflows that are created to be scalable to any other type of sequencing technique as well as agnostic such that it can detect all possible pathogens without specifying any pathogen species or giving any information about the input samples to the workflows. The 5 workflows are:

	- **Preprocessing**: where the quality controlling, reads trimming for quality retaining, host sequences removal and other contaminating sequences removal take place
	- **Taxonomy Profiling**: where taxonomy profiling takes place identifying and visualizing our samples' community abundances down to the subspecies level
	- **Gene-based Pathogen Identification**: where we identify all possible pathogens by identifying all the Virulence factors (VFs) genes and their specific locations, we also indentify Antimicrobial resistance genes (AMRs) within the same workflow.
	- **Allele-based Pathogen Identification**: where we identify all the SNPs and variants and create the consensus sequences of all samples
	- **PathoGFAIR Samples Aggregation and Visualisation**: where we visualize the outputs of the pathogens drawing a heatmap of all the found pathogenic genes for all samples,  phylogenetic trees relating samples together per common pathogenic genes found, and bar charts for important tabular outputs of previous workflows, e.g. number of identified SNPs and variants per sample, number of removed host reads and mapping depth and coverage.

| Workflow Name | WorkflowHub | Dockstore | Galaxy Servers |
|---------------|-------------|-----------|----------------|
| Nanopore **Preprocessing**    | [Link](https://workflowhub.eu/workflows/456) | [Link](https://dockstore.org/workflows/456) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=a705370bc2c13d5c), [American Galaxy Server](https://usegalaxy.org/published/workflow?id=e671ec98735c464e), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=5affb9f3f9a4ac9c) |
| **Taxonomy Profiling** and Visualization with Krona    | [Link](https://workflowhub.eu/workflows/789) | [Link](https://dockstore.org/workflows/789) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=10101558b211a782), [American Galaxy Server](https://usegalaxy.org/published/workflow?id=315cdc4dade62278), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=8515d70d553606e3) |
| **Gene-based Pathogen Identification**    | [Link](https://workflowhub.eu/workflows/789) | [Link](https://dockstore.org/workflows/789) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=585c21b7b1d864fc), [American Galaxy Server](https://usegalaxy.org/published/workflow?id=840e5ffeed517f2f), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=3ef3a7efb9764973) |
| **Allele-based Pathogen Identification**    | [Link](https://workflowhub.eu/workflows/789) | [Link](https://dockstore.org/workflows/789) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=09c7069ae409c362), [American Galaxy Server](https://usegalaxy.org/published/workflow?id=475a8a4da493b1a6), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=8fa27dbe47791b2a) |
| Pathogen Detection **PathoGFAIR Samples Aggregation and Visualisation**    | [Link](https://workflowhub.eu/workflows/789) | [Link](https://dockstore.org/workflows/789) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=376119528377a3ae), [American Galaxy Server](https://usegalaxy.org/published/workflow?id=5d23cb968b13a89f), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=8e9ccb80a107431e)|
| PathoGFAIR 5in1 Workflow   | [Link](https://workflowhub.eu/workflows/123) | [Link](https://dockstore.org/workflows/123) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=0dce37adb369492c) |

- **Training Material:** To assist users in understanding and using the workflows, we have provided extensive training material. This includes tutorials, documentation, and guidelines available via the Galaxy Training Network [GTN](https://bit.ly/pathogen-tuto).

- **Notebooks:** In this repository, you'll find Jupyter notebooks that utilize the output generated by the workflows. These notebooks are designed for reproducing paper-associated figures and allow users to produce similar extra figures other than the ones already included in workflow 2 and 5. The notebook is also designed to run on any Galaxy instance using Jupytool. 

## How to Run the Workflows

- **Galaxy Instance:** You can run the workflows on any Galaxy instance. The workflows are openly available on two workflow registries; WorkflowHub and Dockstore. You can directly use PathoGFAIR on the three main Galaxy servers; European, American, and Australian, or install it on any other Galaxy server.

- **Data Preparation:** Ensure your data is in the correct format and follows the specified guidelines. Please take a look at the training material for details on input requirements.

- **Workflow Execution:** Import the PathoGFAIR workflows into your Galaxy instance and follow the step-by-step instructions provided in the associated training material to execute the workflows on your data.

## Repository Contents

- **Jupter notebooks:** The `bin` directory contains Jupyter notebooks for post-processing and visualization of workflow results.

- **Workflows output datasets:** The `data` directory contains outputs of the workflows after running them on the paper-mentioned samples (BioProject PRJNA982679, BioProjects PRJNA942086 and PRJNA942088). The directory also includes the samples metadata.

- **Jupter notebooks results:** The `results` directory contains results after running the Jupyter notebooks on the workflows output datasets.

- **Publication figures:** The `docs/figures` directory contains all figures mentioned in the paper.

- **Publication tables:** The `docs/tables` directory contains all tables mentioned in the paper.


## Galaxy History

The [Galaxy history](https://usegalaxy.eu/u/engy.nasr/h/biolytix-datasets-analysis) includes the output of running PathoGFAIR workflows on 46 samples, sampled and sequenced by [Biolytix](https://www.biolytix.ch/en/).


## Contributors

- [Engy Nasr](https://orcid.org/0000-0001-9047-4215)
- [Anna Henger](0009-0009-5853-8018)
- [Björn Grüning](https://orcid.org/0000-0002-3079-6586)
- [Paul Zierep](https://orcid.org/0000-0003-2982-388X)
- [Bérénice Batut](https://orcid.org/0000-0001-9852-1987)

## Citation

If you use or refer to this project in your research, please cite the associated paper: [PathoGFAIR: a series of FAIR and adaptable (meta)genomics workflows for (foodborne) pathogens detection and tracking].

Feel free to contribute, open issues, or provide feedback.
