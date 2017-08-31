---
layout: post
title: Plink bfile manipulation
date: 2017-08-18
tags: ["genetics", "GWAS", "plink"]
---

[Plink](https://www.cog-genomics.org/plink2) is one of the most widely used software in GWAS field and its relative file format [bfile](https://www.cog-genomics.org/plink/1.9/formats#bed), a binary file used to store genotype information, may be more popular as supported by other softwares (e.g. [GCTA](http://cnsgenomics.com/software/gcta/#Overview)) as input files.

## "ped/map" files

In the plink file formats, `.ped/map` files are text files used together to store pedigree + genotype information and variant information, respectively. For example, the below commands show the basic information of the `test.map` and `test.ped`, which is converted from test.bed/bim/fam files in gcta 1.26 software package.


```
$ head -2 test.map
1	rs4475691	0	836671
1	rs28705211	0.0151734	890368

$ wc -l test.map
    1000 test.map
    
$ head -2 test.ped |cut -f 1-8 -d " "
1 11 0 0 1 -9 C C
2 21 0 0 2 -9 C C

$ wc -l test.ped
    3925 test.ped
$ head -1 test.ped|awk '{print NF}'
2006
``` 

`test.map` has 1000 lines, which represent 1000 variants with chromosome, SNP id, position in morgans and position in BP per line.

`test.ped` has 3925 lines, which represent 3925 individuals with pedigree information in the first 6 columns and genotype information for the other columns. As one genotype has two alleles, `test.ped` has 6 + 2 * 1000 = 2006 columns.


## "bed/bim/fam" files

The `.bed/bim/fam` files are also called bfile, which is the binary file of `.ped/map` files. The bed file is the test file for genotype, the bim file is for variant information (similiar with map file, added with reference and alternative allele) and the fam file is the text file for pedigree information (first 6 columns of ped file).

```
$ head -2 test.bim
1	rs4475691	0	836671	T	C
1	rs28705211	0.0151734	890368	C	G
$ head -2 test.fam
1 11 0 0 1 -9
2 21 0 0 2 -9
```

The `.bed/bim/fam` files are easy to read/write for softwares and can reduce the storage by more than 10-fold (30840+15776286/982003+34840+76286).

```
$ ls -l test.ped test.map
-rw-r--r--  1 huanwei.wang  Group-Yang     30840 18 Aug 13:42 test.map
-rw-r--r--  1 huanwei.wang  Group-Yang  15776286 18 Aug 13:42 test.ped
$ ls -l test.bed test.bim test.fam
-rw-r-----  1 huanwei.wang  Group-Yang  982003 18 Aug 10:44 test.bed
-rw-r-----  1 huanwei.wang  Group-Yang   34840 18 Aug 10:44 test.bim
-rw-r-----  1 huanwei.wang  Group-Yang   76286 18 Aug 10:44 test.fam
$ echo ""|awk '{print (30840+15776286)/(982003+34840+76286)}'
14.4604
```

The `.bed/bim/fam` and `.ped/map` files can be converted to each other by plink software.

```
# bfile to ped/map
$ plink2 --bfile test --recode --out test

# ped/map to bfile
$ plink2 --file test --make-bed --out test
```

## R package "plink2R"

Sometimes we need to use bfile to do more statsitcial analysis in R, so we need to read the bfile. One strategy is to convert it into text files `ped/map`, while we can also use R package [plink2R](https://github.com/gabraham/plink2R) to read directly.

Installation

```
devtools::install_github("gabraham/plink2R/plink2R")
```

Usage

```
> library(plink2R)
Loading required package: Rcpp
Loading required package: RcppEigen
Warning message:
package ‘Rcpp’ was built under R version 3.4.1
> dat <- read_plink("test")
> dim(dat$bed)
[1] 3925 1000
> dim(dat$fam)
[1] 3925    6
> dim(dat$bim)
[1] 1000    6
```

But the plink2R is relatively slow and takes more memory, so try to manipulate bfile using plink as much as possible.

```
> object.size(dat)
31908168 bytes
```

## C ad Python library "plinkio"

There is also packages for C and Python lauguage, e.g. [plinkio](https://github.com/mfranberg/libplinkio).

```
from plinkio import plinkfile

plink_file = plinkfile.open( "test" )
```
