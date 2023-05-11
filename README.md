# Description
In this repository, there are files and a program that were created as a part of my master's thesis. 

It consists of a script that downloads data of gene sequences and then process them to be used in a CAAS analysis. Additionally, there are results of my master's thesis analysis (folder "masters_thesis_results" - "results.xlxs" contains results of my master's thesis analysis and "final_dataset.csv" contains dataset with data processed by the program; (I believe) it is available also here https://drive.google.com/drive/folders/1PXH8xgirwP3VDi-dWPBErm0z5k5CdcXK?usp=share_link). 


# The downloaded (main) folder contains: 
- "AnAge_dataset" with dataset downloaded 15. 4. 2023 from AnAge database website (https://genomics.senescence.info/species/index.html) (it is possible to replace it with an updated one)
- "AnimalTraits_dataset" with dataset downloaded 15. 4. 2023 from AnimalTraits database website (https://animaltraits.org/) (it is possible to replace it with an updated one)
- "script" with the program
- "README.md"


# To use the program it is needed to add downloaded programs into the main folder:
- NCBI Datasets command line tool: save the program "datasets.exe" into folder "script". More info about NCBI Datasets, how to download etc., on NCBI docs website here: https://www.ncbi.nlm.nih.gov/datasets/docs/v1/download-and-install/#windows
- Clustal Omega: save the downloaded Clustal folder (with clustalo.exe program) as 'clustal-omega-1.2.2-win64' into the main folder. More info about Clustal Omega, how to download etc., on Clustal website here: http://www.clustal.org/omega/



# Information about the output files created by the program:

## Files in folder "CAAStools_files":
- folder "fasta_files" containing fasta files each with all selected ortholog sequences (of both short and long-living organisms); will be used for MSA 
- folder "MSA_results" containing MSA outputs; these are needed as input files in CAASTools Discovery analysis
- file "config.txt" with organisms traits info; needed as an input in CAASTools Discovery analysis

## Files in folder "results": 
- "anage_animaltraits_data_merge.csv" contains all data from AnAge and AnimalTraits merged
- "gene_in_multiple_paths_check.csv" contains information about in which paths are genes involved in
- "genes_organisms_check.csv" contains information about what data were downloaded from NCBI, i.e. what genes for what organisms
- "all_downloaded_sequences.csv" contains all information from stress molecules files downloaded from NCBI merged 
- "orthologs_count.csv" contains information about number of sequences that were downloaded for each gene
- "final_dataset.csv" contains the final dataset with data processed by the program
- "stress_molecules.csv" contains all stress molecules used for the analysis, i.e. those that were HGNC-checked and their sequences were available in the NCBI databases

# Additional information: 
The CAASTools Discovery analysis on files from "CAASTools_files folder" is then run in Ubuntu Linux.
More information about the tool is available in the article "CAAStools, a toolbox to identify and test Convergent Amino Acid Substitutions", here: https://www.biorxiv.org/content/10.1101/2022.12.14.520422v1 
