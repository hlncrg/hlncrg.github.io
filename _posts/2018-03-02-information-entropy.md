---
layout: post
title: Splitting Desicion Trees on Information Entropy
---

ID3 is a classical algorithm for creating descision trees.  The splits in the tree are based on
the greedy minmization of information entropy.

-----


Iterative Dichotomiser 3 or ID3 is an algorithm for creating descion trees invented by Ross Quinlan
in 1986.  It is an excellent excuse to discuss information entropy.

Information entropy is a measure of disorder in data.  Indeed, the goal of decision trees in general are
to minimize the entropy in the encoding.  

# Encoding Data

In order to understand entropy on more than a superficial level, we first need a basic
understanding of different ways to encode information or data. 

![tree and entropy]
(https://github.com/hlncrg/hlncrg.github.io/blob/master/_posts/images/TreeAndEntropy.png) 

