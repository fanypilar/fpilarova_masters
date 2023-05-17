# Description
**This repository contains files and a script that were created as a part of my master's thesis.**

The script downloads data of gene sequences and then processes them to be used in a CAAS analysis. 

In the repository, there are also a dataset and results of my master's thesis analysis (folder "masters_thesis_results"). The file "final_dataset.csv" is an output of the script and contains input dataset for the analysis. The file "results.xlxs" contains information about the dataset and results of the analysis. The data should be also available here https://drive.google.com/drive/folders/1PXH8xgirwP3VDi-dWPBErm0z5k5CdcXK?usp=share_link). 


# The repository contains: 
- "AnAge_dataset" with dataset downloaded 15. 4. 2023 from AnAge database website (https://genomics.senescence.info/species/index.html) (it is possible to replace it with an updated one)
- "AnimalTraits_dataset" with dataset downloaded 15. 4. 2023 from AnimalTraits database website (https://animaltraits.org/) (it is possible to replace it with an updated one)
- "masters_analysis_results" 
  - with the results of the run of the program with genes that were chosen for the analysis for my master's thesis 
  - and with the final dataset created by the program
- "script" with the program
- "README.md"


# To use the program it is needed to add downloaded programs into the main folder (fpilarova_masters-main):
- NCBI Datasets command line tool: save the program "datasets.exe" into folder "script". More info about NCBI Datasets, how to download etc., on NCBI docs website here: https://www.ncbi.nlm.nih.gov/datasets/docs/v1/download-and-install/#windows
- Clustal Omega: save the downloaded Clustal folder (with clustalo.exe program) as 'clustal-omega-1.2.2-win64' into the main folder. More info about Clustal Omega, how to download etc., on Clustal website here: http://www.clustal.org/omega/



# Information about the output files created by the program:

## Files in folder "CAAStools_files":
- folder "fasta_files" contains fasta files each with all selected ortholog sequences (of both short and long-living organisms); will be used for MSA 
- folder "MSA_results" contains MSA outputs; these are needed as input files in CAAStools Discovery analysis
- file "config.txt" with organisms traits info; needed as an input in CAAStools Discovery analysis

## Files in folder "results": 
- "anage_animaltraits_data_merge.csv" contains all data from AnAge and AnimalTraits merged
- "gene_in_multiple_paths_check.csv" contains information about in which paths are genes involved in
- "genes_organisms_check.csv" contains information about what data were downloaded from NCBI, i.e. what genes for what organisms
- "all_downloaded_sequences.csv" contains all information from stress molecules files downloaded from NCBI merged 
- "orthologs_count.csv" contains information about number of sequences that were downloaded for each gene
- "final_dataset.csv" contains the final dataset with data processed by the program
- "stress_molecules.csv" contains all stress molecules used for the analysis, i.e. those that were HGNC-checked and their sequences were available in the NCBI databases

# Additional information: 
The CAAStools Discovery analysis on files from "CAAStools_files folder" is then run in Ubuntu Linux.
More information about the tool is available in the article "CAAStools, a toolbox to identify and test Convergent Amino Acid Substitutions", here: https://www.biorxiv.org/content/10.1101/2022.12.14.520422v1 
