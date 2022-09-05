## What is ms_seqcon.py

This script will perform some useful multiple sequence alignment (MSA) manipulations. 
This was originally created for manipulating MSAs so I could perform extant sequence reconstruction (ESR) in another repository.

## Why do I need ms_seqcon.py?

If you are working with MSAs for bioinformatic purposes you don't want to write a bunch of separate scripts to do some common things.

These common things include;

-take an alignment and explode all seqs into individual sequence files                      

-calculate the number of taxa and the length of the alignment                     

-convert one alignment type into another  

-delete any column that is all gaps 

-apply gaps from MSA1 to MSA2

-get the fraction of identical residues between two MSA1 & MSA2, 
MSA1 considered true
 
## What do I need to use ms_seqcon.py?
This is all written in python, so you'll need a few packages.
biopython:
```
pip install biopython
```
numpy:
```
pip install numpy
```
argparse:
```
pip install argparse
```
regex:
```
pip install regex
```
os-sys:
```
pip install os-sys
```

## Using ms_seqcon.py
 
 usage:
 ```
 ./ms_seqcon.py -h
 ```
 
 output:
 ```
 usage: ms_seqcon.py [-h] [-E] [-M] [-R] [-D] [-G] [-C] [--MSA MSA [MSA ...]]
                    [--form1 FORM1 [FORM1 ...]] [--form2 FORM2 [FORM2 ...]]
                    [--direct DIRECT]

optional arguments:
  -h, --help            show this help message and exit
  -E, --explode         take an alignment and explode all seqs into individual
                        sequence files
  -M, --Aln_Dim         calculate the number of taxa and the length of the
                        alignment
  -R, --Reformat        convert one alignment type into another
  -D, --Delete          delete any column that is all gaps
  -G, --Gap             apply gaps from MSA1 to MSA2
  -C, --Correct         get the fraction of identical residues between two
                        alignments, MSA1 considered true
  --MSA MSA [MSA ...]   names of the MSA file(s)
  --form1 FORM1 [FORM1 ...]
                        input formats of the MSA file(s)
  --form2 FORM2 [FORM2 ...]
                        output format of the MSA file
  --direct DIRECT       where to direct files, default cwd
  ```
 
 example generating individual sequence fasta files:
 ```
 ./ms_seqcon.py -E --MSA Apico2020_seqs.fasta --form1 fasta
 ```
 
 example calculating fraction of identical residues between two alignments:
 ```
 ./ms_seqcon.py -C --MSA Apico2020_seqs_real.fasta Apico2020_seqs_recon.fasta --form1 fasta
 ```

