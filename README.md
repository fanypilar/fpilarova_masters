# It is needed to:
## 1. Rename downloaded folder (called here as a main folder) as "fpilarova_masters-main" (the script uses the name)
The downloaded (main) folder contains: 
- "AnAge_dataset" with dataset downloaded 15.4.2023 from AnAge database website (https://genomics.senescence.info/species/index.html)
- "AnimalTraits_dataset" with dataset downloaded 15.4.2023 from AnimalTraits database website (https://animaltraits.org/)
- "script" with the program
- "README.md"


## 2. Download:

NCBI Datasets command line tool: save the program "datasets.exe" into folder "script"
More info about NCBI Datasets, how to download etc. on NCBI docs website here: https://www.ncbi.nlm.nih.gov/datasets/docs/v1/download-and-install/#windows


Clustal Omega: save the downloaded Clustal folder (with clustalo.exe program) as 'clustal-omega-1.2.2-win64' into the main folder
More info about Clustal Omega, how to download etc. on Clustal website here: http://www.clustal.org/omega/

## 3. Into the main folder create folders: 

"CAASTools_files"
"NCBI_Datasets_download"
"analyses"
"results"
"stress_molecules"

# Information about the output files created by the script:
## Files in folder "analyses"
- "anage_animaltraits_data_merge.csv" contains all data from AnAge and AnimalTraits merged
- "gene_in_multiple_paths_check.csv" contains information about in which paths are genes involved in
- "genes_organisms_check.csv" contains information about what data were downloaded from NCBI, i.e. what genes for what organisms
- "all_downloaded_sequences.csv" contains all information from stress molecules files downloaded from NCBI merged 
- "orthologs_count" contains information about number of sequences that were downloaded for each gene

## Files in folder "results": 
- "organisms_lq.csv" contains information about bodymas, lifespan and lq of organisms that there are gene data available
- "long_living_organisms.csv" contains last decile of organisms_lq.csv, i.e. long-living organisms
- "short_living_organisms.csv" contains first decile of organisms_lq.csv, i.e. short-living organisms
- "long_selected_orthologs.csv" contains selected sequences of stress molecule genes of short-living organisms
- "short_selected_orthologs.csv" contains selected sequences of stress molecule genes of long-living organisms

## Files in folder "stress_molecules"

- "stress_molecules.csv" contains all stress molecules used for the analysis, i.e. those that were HGNC-checked and their sequences were available on NCBI website 
