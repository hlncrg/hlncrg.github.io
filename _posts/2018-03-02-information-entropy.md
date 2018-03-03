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

Let's start with a tree-based example.  

![Tree and entropy]({{ site.url }}/public/images/TreeAndEntropy.png) 

These trees represent the boolean function (A and B) or (A and C).  The first tree 
is as small as possible and encodes the information in a compact form.  The other
trees have one extra node that is unneccessary and therefore has more entropy.

Now that we have a visual representation of entropy, let's talk about formulas.

Entropy is defined as $$Entropy(X)=\sum P(x_i)\log_2 P(x_i)$$

