# The scripts and data used in the evolution analyses of the paper: Evolutionary fingerprint in rodent PD1 confers weakened activity and enhanced tumor immunity compared to human PD1 

Creators: Lin Chen <chenlin212@mails.ucas.ac.cn>  

Please contact Lin or Zhengting Zou <zouzhengting@ioz.ac.cn> for any inquiries or questions regarding the content and usage of this repository.

## 1. Data

- `0_data/`: This directory contains the data used in the molecular evolution analyses of the paper, organized into the following two parts.
	 - `0_data/fig5A_preITSM_pattern/`: Sequences and phylogeny used to produce Fig. 5A.
       - `5133_NT_AL_used_OrthoMaM.fasta`: The PD1 ortholog sequences used in fig5A, obtained from OrthoMaM with gene ID 5133. Species names are included in the sequence headers.
       - `PDCD1_protein_used_UniProt.fasta`: The PD1 ortholog sequences used in fig5A, obtained from UniProt. Species names and accession numbers are included in the sequence headers.
       - `PDCD1_refseq_protein_used_NCBI.fasta`: The PD1 ortholog sequences used in fig5A, obtained from NCBI Orthologs with gene ID 5133. Species names and accession numbers are included in the sequence headers.
       - `timetree.treefile`: Newick format tree file of the tree shown in fig5A, obtained from TimeTree5.
    
    -  `0_data/selectionAndASR/`: Sequences and phylogeny used for selection analyses and ancestral sequence reconstruction (ASR).
	      - `<Gene ID>_NT_AL.fasta`: The original codon alignment FASTA file used for selection analyses and ASR, obtained from OrthoMaM. The prefix of each file is the respective Gene ID in OrthoMaM.
        - `timetree_all_sp.treefile`: Newick format supertree file of the tree used for selection analyses and ASR, obtained from TimeTree5.


## 2. Scripts

- `1_script/`: This directory contains the scripts used in the molecular evolution analyses of the paper, with the following contents.

	 - `1_script/PD1_ASR.bash`: Bash script containing commands for the ASR analysis based on codon and amino acid alignments.
	 - `1_script/selection/`: This directory contains all Jupyter Notebook files `<Gene name>.ipynb` used for data cleaning and running hyphy for the selection analyses.

	   - Notes for the `<Gene name>.ipynb` files: 
				- Each file includes the Python codes for removing gap-rich sequences (according to the method described in the paper), building the tree files for selection analyses, and running hyphy.
        - "MRCA" parts focus on the most recent common ancestor (MRCA) branch of the clade of species according to the methods described in the paper.
        - "within_clade" parts focus on all branches within the clade, excluding the MRCA branch, according to the method described in the paper.
