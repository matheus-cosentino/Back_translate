# Back_translate
A open access python script to generated an nucleotide alignment, having as input a aminoacid aligment originated from a nucleotide fasta. Ideal for dealing with large datasets.

# Installation
Acess your terminal and activate conda
```bash
conda activate
```
Copy the present repository
```bash 
git clone https://github.com/matheus-cosentino/Back_translate.git
cd Back_translate
```

Check if the python recognizes script with the help function

```bash
python backTranslate.py -h
```

output

```bash
usage: backTranslate.py [-h] [-nt NUCLEOTIDE_FILE] [-ali AMINO_ACID_FILE] [-out OUTPUT_FILE]
arguments:
  -h, --help            show this help message and exit
  -nt NUCLEOTIDE_FILE   nucleotide sequence file
  -ali AMINO_ACID_FILE  amino acid multiple alignment file
  -out OUTPUT_FILE      output file for nucleotide multiple alignment ````
```

# Example
For trying this script, a example dataset of Anelloviruses ORF1 can be found in the Example directory within this repository. 
The sequences were obtained from https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2022.1002963

The nucleotide sequence was translated by Aliview v.1.28 and the protein alignment was built with MAFFT v7.505 
In case of interest, do the alignment with the following commands.
```bash
cd Example
mafft Cosentino_2022_ORFsnt_Anello.translated.fas > aln_aa_Cosentino_2022_Anello.fasta
```
Transform your protein alignment in a nucleotide alignment with the following command.

```bash
python ../backTranslate.py -nt Cosentino_2022_ORFsnt_Anello.fas -ali aln_aa_Cosentino_2022_Anello.fasta -out aln_nt_aa_Cosentino_2022_Anello.fasta
```

# Citing
If this script was helpfull to you, consider citing it. :)

