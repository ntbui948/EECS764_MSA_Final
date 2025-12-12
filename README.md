# EECS 764 – Multiple Sequence Alignment Project (Code Summary)

This repository contains the code used for our project on Multiple Sequence Alignment (MSA).  
The goal of the project is to compare several MSA strategies and evaluate their accuracy and computational behavior:

1. VAT-based guide trees using both full VAT distances and mBed-style embeddings  
2. Progressive profile–profile alignment using guide trees  
3. Gibbs sampling as a refinement method on MSA for local alignments  
4. Evaluation of generated alignments against Pfam reference data

The scripts in this folder perform three major functions:

• Preparing FASTA input data (including converting Pfam SEED files)  
• Constructing guide trees with VAT and producing MSAs  
• Refining and evaluating alignments using Gibbs sampling and Pfam comparisons  

This codebase was used to generate the results presented in the final report and class presentation.

---

## Repository Contents (High-Level)

**VAT_guidetree4.py**  
Builds a full VAT distance matrix and constructs a UPGMA guide tree for progressive MSA.

**VAT_guidetree5.py**  
Uses VAT with mBed-style embeddings to build a faster approximate guide tree.

**normalize_alignments.py**  
Standardizes alignments (sequence order, naming, gap formatting) to enable comparisons.

**seed_to_fasta.py**  
Converts Pfam SEED files and extracted sequences into standard FASTA format.

**gibbs_test.py**  
Experimental Gibbs sampling refinement on MSA for computing optimal local alignment.

**test_alignment_to_pfam.py**  
Compares an alignment to the Pfam reference alignment using FastSP.

**VAT_guidetree4_prev.py / VAT_guidetree5_prev.py**  
Earlier versions of the VAT guide-tree implementations (kept for reference).

**README.md**  
This document.

---

## Notes

• Scripts assume access to VAT, Clustal Omega, and local Pfam files.  
• Paths may need adjustment depending on local machine setup.  
• This code supports the analysis and experiments described in the final report.

---

