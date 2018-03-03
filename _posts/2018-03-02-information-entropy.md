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

Next let's talk about encoding these systems using bits.  Each bit is 
a node and 'yes' is encoded as 1 while 'no' is encoded as 0.  For 
the simplest tree, what are the combinations?  

Walking through the tree in depth first order we get:

|1(A)|1(B)|
|1(A)|0(B)|
|0(A)|1(C)|
|0(A)|0(C)|

Now that we have a visual representation of entropy and 
used the same systems to illustrate the use of bits 
to encode, let's talk about formulas.

Entropy is defined as $Entropy(X)=\sum P(x_i)\log_2 P(x_i)$ where $P(x_i)$ is 
the probability of an outcome and $\log_2 P(x_i)$ is the number of bits
need to encode the outcome.  In other words, this is the expectation 
value of the number of bits needed to encode the information.  

