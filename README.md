# PathoGFAIR: a collection of FAIR and adaptable (meta)genomics workflows for (foodborne) pathogens detection and tracking

PathoGFAIR is a collection of Galaxy-based FAIR workflows employing state-of-the-art tools to detect and track 
pathogens from metagenomic Nanopore sequencing. Although initially developed to detect pathogens in food 
datasets, the workflows can be applied to other metagenomic Nanopore pathogenic data. PathoGFAIR incorporates 
visualisations and reports for comprehensive results.

## PathoGFAIR implementation

The core of PathoGFAIR project is a series of 5 Galaxy-based workflows designed to process Nanopore sequencing 
data, detect pathogens, and track their presence across samples:

- **Preprocessing**: where the quality controlling, reads trimming for quality retaining, host sequences removal and other contaminating sequences removal take place
- **Taxonomy Profiling**: where taxonomy profiling takes place identifying and visualizing our samples' community abundances down to the subspecies level
- **Gene-based Pathogen Identification**: where we identify all possible pathogens by identifying all the Virulence factors (VFs) genes and their specific locations, we also identify Antimicrobial resistance genes (AMRs) within the same workflow.
- **Allele-based Pathogen Identification**: where we identify all the SNPs and variants and create the consensus sequences of all samples
- **Samples Aggregation and Visualisation**: where we visualize the outputs of the pathogens drawing a heatmap of all the found pathogenic genes for all samples,  phylogenetic trees relating samples together per common pathogenic genes found, and bar charts for important tabular outputs of previous workflows, *e.g.* number of identified SNPs and variants per sample, number of removed host reads and mapping depth and coverage.

![plot](docs/figures/Figure_1.png)

### Where to find the workflows? 

Workflows are available on 2 workflows registries ([Dockstore](https://dockstore.org/organizations/iwc) and [WorkflowHub]()) and several Galaxy servers.

| Workflow Name | WorkflowHub | Dockstore | Galaxy Servers |
|---------------|-------------|-----------|----------------|
| Nanopore **Preprocessing**  (v 0.1)  | [ID 1061 v 0.1](https://workflowhub.eu/workflows/1061) | [nanopore-pre-processing/main:v0.1](https://dockstore.org/workflows/github.com/iwc-workflows/nanopore-pre-processing/main) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=a705370bc2c13d5c), [United States Galaxy Server](https://usegalaxy.org/published/workflow?id=574e42683dc3961b), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=25d52afddaa3451b) |
| **Taxonomy Profiling** and Visualization with Krona  (v 0.1)  | [ID 1059 v 0.1](https://workflowhub.eu/workflows/1059) | [taxonomy-profiling-and-visualization-with-krona/main:v0.1](https://dockstore.org/workflows/github.com/iwc-workflows/taxonomy-profiling-and-visualization-with-krona/main) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=10101558b211a782), [United States Galaxy Server](https://usegalaxy.org/published/workflow?id=8f5904693b5f74f4), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=d9ba165e6ae55417) |
| **Gene-based Pathogen Identification**  (v 0.1)  | [ID 1062 v 0.1](https://workflowhub.eu/workflows/1062) | [gene-based-pathogen-identification/main:v0.1](https://dockstore.org/workflows/github.com/iwc-workflows/gene-based-pathogen-identification/main) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=585c21b7b1d864fc), [United States Galaxy Server](https://usegalaxy.org/published/workflow?id=cce88bc57b180d09), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=ef8c22c2525063a2) |
| **Allele-based Pathogen Identification**  (v 0.1)  | [ID 1063 v 0.1](https://workflowhub.eu/workflows/1063) | [allele-based-pathogen-identification/main:v0.1](https://dockstore.org/workflows/github.com/iwc-workflows/allele-based-pathogen-identification/main) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=09c7069ae409c362), [United States Galaxy Server](https://usegalaxy.org/published/workflow?id=38911ba6f66d80f6), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=244ea5e94237ebad) |
| **Samples Aggregation and Visualisation**  (v 0.1)  | [ID 1060 v 0.1](https://workflowhub.eu/workflows/1060) | [pathogen-detection-pathogfair-samples-aggregation-and-visualisation/main:v0.1](https://dockstore.org/workflows/github.com/iwc-workflows/pathogen-detection-pathogfair-samples-aggregation-and-visualisation/main) | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=376119528377a3ae), [United States Galaxy Server](https://usegalaxy.org/published/workflow?id=2d3063882d8239ff), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=eda40b58616a0fe4)|
| **PathoGFAIR** 5in1  (v 0.1)  | Soon | Soon | [European Galaxy Server](https://usegalaxy.eu/published/workflow?id=0dce37adb369492c), [United States Galaxy Server](https://usegalaxy.org/published/workflow?id=e55593af91337a05), [Australian Galaxy Server](https://usegalaxy.org.au/published/workflow?id=f5f9808fb50b6f2c)|

### How to learn to use the workflows?

To assist in understanding and using the workflows, we provide extensive tutorial and recording available via 
the Galaxy Training Network [GTN](https://bit.ly/pathogen-tuto).

## Use Cases

To demonstrate PathoGFAIR and its features, 130 samples from 2 studies (without or with prior pathogen 
isolation) were analysed.

All samples contained pathogens known beforehand and were sequenced using Oxford Nanopore technology.

### Samples Without Prior Pathogen Isolation

Pathogens were deliberately spiked into 46 samples to mimic real-world scenarios given a [protocol](dx.doi.org/10.17504/protocols.io.8epv5x1jdg1b/v1) 
developed in the context of PathoGFAIR.

The full analysis can be found in a [dedicated Galaxy history](https://usegalaxy.eu/u/engy.nasr/h/biolytix-datasets-analysis).

### Samples With Prior Pathogen Isolation

To further test PathoGFair, 84 public datasets were used. The full analysis can be found in a [dedicated Galaxy history]().

## Benchmarking

To evaluate the effectiveness of PathoGFAIR workflows, a benchmarking analysis was performed comparing 
PathoGFAIR's pathogen detection capabilities with the systems and pipelines.

This section provides detailed instructions to replicate the PathoGFAIR benchmarking process, as outlined in our 
dedicated protocol on [protocols.io](https://dx.doi.org/10.17504/protocols.io.e6nvwbp4zvmk/v1). The focus here 
is on running the selected systems/pipelines used in our benchmarking.

### PathoGFAIR

- **Setup:** Import the [Galaxy history](https://usegalaxy.eu/u/engy.nasr/h/biolytix-datasets-analysis), 
which contains the benchmarking results of PathoGFAIR

- **Results:**
	- View the results directly.
	- Rerun PathoGFAIR workflows on the same 46 samples, available under dataset number `47:biolytix_classified_samples`.

### CZID (IDseq)

- **Setup:**
	1. Create an Account on [CZID](https://czid.org/): We used credentials from Engy Nasr, University of Freiburg.
	2. Create a public or private Project with the following details:
		- Name
		- Description
		- Analysis Type: Metagenomics
		- Sequencing Type: Nanopore
	3. Upload Datasets: Upload the 46 samples (total size: 7GB) either locally or from a public repository:
		- Local upload (our recommendation): Download the samples from our published [Galaxy history](https://usegalaxy.eu/u/engy.nasr/h/biolytix-datasets-analysis) and upload them.
		- Online upload: Use the NCBI repository PRJNA982679.
	4. Upload or Enter Metadata: Metadata fields we included are: host [Chicken], Ct value, sampling date, location, and nucleotide type [DNA], which are available in our metadata table in [`data/benchmark`](https://github.com/usegalaxy-eu/PathoGFAIR/tree/main/data/benchmark/PathoGFAIR_benchmark_samples_metadata.tsv).
		
		For a full list of possible fields to include, see: [CZID Metadata Dictionary](https://czid.org/metadata/dictionary).

- **Execution:** Sample uploads started on Tuesday, October 15th, at 9 AM. Dataset upload finished at 9:58 AM. Analysis was fully completed for all samples after: 1hour and 30 mins of the datasets finished upload.

- **Results:**
	View the analysis results: [CZID Results](https://czid.org/il2mk), use the drop down menu on the top left to switch between samples.

### BugSeq

- **Setup:**
	1. Create an Account on [BugSeq](https://app.bugseq.com/register): We used credentials from Engy Nasr, University of Freiburg.
	2. Upload datasets: Upload the 46 samples (total size: 7GB) either locally or via their BaseSpace, that you have to contact them for. We uploaded them from local directory, same as explained for CZID(IDseq)
	3. Set up parameters
		- Platform: Nanopore
		- Device & Chemistry: MinION/GridION/Flongle - R9.4.1
		- Metagenomic Database: NCBI nt (BugSeq recommendation for metagenomics samples)
		- Sample Type: Generic (BugSeq recommendation)
		- Sequenced Material: DNA
		- Outbreak Analysis (Genomic Relatedness Visualization): yes

- **Execution:** Sample uploads started on Tuesday, October 15th, at 11:30 AM. Dataset upload finished at 12:30 PM. Analysis was fully completed for all samples after: 1hour and 30 mins of the datasets finished upload.

- **Results:** On Tuesday, October 15th, at 15:21 PM, we received that the analysis had failed, as we have insufficient sample credits.  We sent to their support for help directly after receiving their email. They replied back that we can only analyse 10 samples not 46, so BugSeq will be removed from the benchmark.


## GitHub [Repository](https://github.com/usegalaxy-eu/PathoGFAIR/tree/main)

In the GitHub repository, you'll find sources (Jupyter notebooks) to replicate figures in the manuscript.

The notebooks are also designed to run on any Galaxy instance using Jupytool. 

### Requirements

- Python 3.11.4
- Jupyter

### Folder structure

- `data`: folder contains outputs of the workflows after running them on the paper-mentioned samples (BioProject PRJNA982679, BioProjects PRJNA942086 and PRJNA942088). The directory also includes the samples metadata.

- `bin`: folder with two Jupyter notebooks (1 per use case) for 
	- importing all tables from the `data` folder
	- generating all figures to the `results` folder. 

- `results`: folder with results after running the Jupyter notebooks on the workflows output datasets.

- `docs`: folder with figures (`docs/figures`) and tables (`docs/tables`) mentioned in the paper.

## Contributors

- [Engy Nasr](https://orcid.org/0000-0001-9047-4215)
- [Anna Henger](https://orcid.org/0009-0009-5853-8018)
- [Björn Grüning](https://orcid.org/0000-0002-3079-6586)
- [Paul Zierep](https://orcid.org/0000-0003-2982-388X)
- [Bérénice Batut](https://orcid.org/0000-0001-9852-1987)

## Contribution

Feel free to contribute, open issues, or provide feedback.

## Citation

If you use or refer to this project in your research, please cite the associated paper: 

> PathoGFAIR: a collection of FAIR and adaptable (meta)genomics workflows for (foodborne) pathogens detection and tracking
> Engy Nasr, Anna Henger, Björn Grüning, Paul Zierep, Bérénice Batut
> bioRxiv 2024.06.26.600753; doi: https://doi.org/10.1101/2024.06.26.600753 

