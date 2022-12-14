## What have we here?

I have uploaded a jupyter notebook script in which you can calculate the negative entropy of a column in an alignment I provide. 
In addition, there is a brief primer on entropy in biology and how to intuitively understand it.

I demonstrate a couple of very simple ways to visualize the data that might be useful for biologists just getting into analyzing data multiple sequence alignments.

You should feel free to edit this script to suit your needs. 

## Running the jupyter script

You will need Jupyter notebook on Anaconda, matplotlib, numpy, and biopython

Anaconda

```
https://www.anaconda.com/
```

matplotlib

```
pip install -U matplotlib
```

numpy

```
pip install numpy
```

biopython

```
pip install biopython
```

Once you have Anaconda, with the appropriate packages, open Jupyter Notebook from Anaconda-Navigator. 
The function that calculates the negative entropy requires the directory location of the MSA file you downloaded, 
in the signle quotes of ```direct = ''.```

## What should you see?

A histogram of the negative entropies in the alignment.

<img width="357" alt="Histogram_H" src="https://user-images.githubusercontent.com/111892527/187763026-7e62d991-77a4-478b-8787-557b0f9a75d7.png">

A plot of the negative entropy as a function of sites in the alignment.

<img width="641" alt="Sites_H" src="https://user-images.githubusercontent.com/111892527/187763082-2dc98dd6-c4c2-494a-b84d-dc530072be14.png">


