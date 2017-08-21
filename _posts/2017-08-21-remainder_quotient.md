---
layout: post
title: Remainder and quotient
date: 2017-08-21
tags: ["cs"]
---


From binary to decimal
----------------------

-   binary: "1101"
-   decimal: "13"

1 × 2<sup>4 − 1</sup> + 1 × 2<sup>3 − 1</sup> + 0 × 2<sup>2 − 1</sup> + 1 × 2<sup>1 − 1</sup>

=1 × 2<sup>3</sup> + 1 × 2<sup>2</sup> + 1 × 2<sup>1</sup> + 1 × 2<sup>0</sup>

=8 + 4 + 1 = 13

    BinToDec = function(x){
      sum(2^(which(rev(unlist(strsplit(as.character(x), "")) == 1))-1))
    }
    DecToBin = function(x){
      bin=""
      while(x != 0){
        bin = paste(x%%2,bin,sep="")
        x = x %/% 2
      }
      return(bin)
    }

    BinToDec("1101")

    ## [1] 13

    DecToBin(13)

    ## [1] "1101"

From n-ary to decimal
---------------------

    NaryToDec = function(x, n){
      sum(n^(which(rev(unlist(strsplit(as.character(x), "")) == 1))-1))
    }
    DecToNary = function(x,n){
      bin=""
      while(x != 0){
        bin = paste(x%%n,bin,sep="")
        x = x %/% n
      }
      return(bin)
    }

    NaryToDec("1101",2)

    ## [1] 13

    DecToNary(13,2)

    ## [1] "1101"

    DecToNary(13,3)

    ## [1] "111"

multiple loop indexs to one loop index
--------------------------------------

It's common for me to run a script using multiple loops to iterate.
I usually just put one for-loop into the nest of antoher for-loop.

But if I would like to parallel them using different nodes in a computing cluster and
submit a job array using one index, how to do it?

    for(a in 1:2){
      for(b in 1:3){
        for(c in 1:4){
          print(paste(a,b,c,sep=" "))
        }
      }
    }

    ## [1] "1 1 1"
    ## [1] "1 1 2"
    ## [1] "1 1 3"
    ## [1] "1 1 4"
    ## [1] "1 2 1"
    ## [1] "1 2 2"
    ## [1] "1 2 3"
    ## [1] "1 2 4"
    ## [1] "1 3 1"
    ## [1] "1 3 2"
    ## [1] "1 3 3"
    ## [1] "1 3 4"
    ## [1] "2 1 1"
    ## [1] "2 1 2"
    ## [1] "2 1 3"
    ## [1] "2 1 4"
    ## [1] "2 2 1"
    ## [1] "2 2 2"
    ## [1] "2 2 3"
    ## [1] "2 2 4"
    ## [1] "2 3 1"
    ## [1] "2 3 2"
    ## [1] "2 3 3"
    ## [1] "2 3 4"

    for(index in 1:24){
      ar = (index-1) %% 2 + 1; aq = (index-1) %/% 2
      br = (aq - 1) %% 3 + 1; bq = (aq - 1) %/% 3
      cr = (bq - 1) %% 4 + 1
      print(paste(ar,br,cr,sep=" "))
    }

    ## [1] "1 3 3"
    ## [1] "2 3 3"
    ## [1] "1 1 4"
    ## [1] "2 1 4"
    ## [1] "1 2 4"
    ## [1] "2 2 4"
    ## [1] "1 3 4"
    ## [1] "2 3 4"
    ## [1] "1 1 1"
    ## [1] "2 1 1"
    ## [1] "1 2 1"
    ## [1] "2 2 1"
    ## [1] "1 3 1"
    ## [1] "2 3 1"
    ## [1] "1 1 2"
    ## [1] "2 1 2"
    ## [1] "1 2 2"
    ## [1] "2 2 2"
    ## [1] "1 3 2"
    ## [1] "2 3 2"
    ## [1] "1 1 3"
    ## [1] "2 1 3"
    ## [1] "1 2 3"
    ## [1] "2 2 3"
