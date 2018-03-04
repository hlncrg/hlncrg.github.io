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
trees have one extra node that is unneccessary.

In term of computation, having a larger tree is bad because is requires more steps
to calculate.  In terms of data, A is the most informative element and
asking what its value is first makes us come to a conclusion faster on
average.  A fancier way of saying this is that few bits are needed to 
store the same information.


Now that we have a visual representation of information
let's talk about formulas.

# Entropy of the system

Entropy is defined as $$Entropy(X)=\sum P(x_i)\log_2 P(x_i)$$ where $$P(x_i)$$ is 
the probability of an outcome and $$\log_2 P(x_i)$$ is the number of bits
need to encode the outcome.  In other words, this is the expectation 
value of the number of bits needed to encode the information.  

To apply this formula we need one more component, the probabilities of each
combinations.  Here is a table of the combinations:

|A|B|C||
|-|-|-|-|
|1|1|1|T|
|1|1|0|T|
|1|0|1|T|
|1|0|0|F|
|0|1|1|F|
|0|1|0|F|
|0|0|1|F|
|0|0|0|F|

We have been implicitly assuming that each of these cases is equally likely.
We can think of this table as our training set essentially.

First we calculate the entropy without any splits.  The probability of a true
is 3 out of 8 and the probability of a false is a 5 out of 8. 
The entropy is therefore $$-3/8\log(3/8)-5/8\log(5/8)=0.66$$. 
If the probability had been 50/50 then the entropy would be 1 and
we would need to 

# References

<iframe width="560" height="315" src="https://www.youtube.com/embed/eLlYSpVjH94" 
frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe> 
