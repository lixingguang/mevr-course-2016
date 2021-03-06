# Practice

- The ```phangorn``` library in R contains functions to perform maximum likelihood based analyses of sequence data
  - While not the fastest program, it is very flexible
  - Can fit a wide variety of substitution models
- For large-scale phylogenetic inference, there are specialised (external) software packages available
  - RAxML/ExaML
  - PhyML
  - IQTREE
- As with alignment, we can use R to format the data, and call these external programs
- There is also an interface to RAxML in the ```ips``` package

## ```phangorn```

- Takes data in a special format, ```phyDat```
  - Sequences read in using ```ape``` are in ```DNAbin``` format
  - There is a convenience function called ```as.phyDat``` that can convert between them
- Can compare between different models using ```modelTest```
- Can fit models (and trees) using ```pml```

## RAxML

- [RAxML](http://sco.h-its.org/exelixis/web/software/raxml/index.html) is one of the fastest, most accurate phylogeny reconstruction software packages available
- It does *not* implement a wide variety of models, instead, it assumes a fairly complex one, which will probably be the best model if the dataset is variable enough

## PhyML

- [PhyML](https://code.google.com/p/phyml/) is slower than RAxML, but offers a wider variety of models
- Also offers an interactive (text) interface

## IQTREE

- [IQTREE](http://www.cibiv.at/software/iqtree/) is a fairly new phylogenetic software package
- It *does* implement a variety of models, and includes model selection and a fast bootstrap-like procedure

