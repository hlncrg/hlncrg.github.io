---
layout: post
title: Basic Probability Notes 
---

Some basic notes
-----

Probability of a union of A and B:

$$P(A \cup B)=P(A)+P(B)-P(A \cap B)$$

Probability of intersection of A and B:

$$P(A \cap B)=P(A)P(B|A)=P(B)P(A|B)$$

How to choose k out of n items:

||order|no order|
|-|-|-|
|w replacement|$n^k$|\frac{(n+k-1)!}{(n-1)!(k)!} = \binom{n+k-1}{k}|
|w/o replacement|\frac{n!}{(n-k)!}|\frac{n!}{k!(n-k)!} = \binom{n}{k}|
