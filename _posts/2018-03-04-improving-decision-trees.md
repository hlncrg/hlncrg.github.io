---
layout: post
title:  The Improved Decision Tree: C4.5
---

I would like to go over in detail the improvments
made by the C4.5 algorithm.

-----

From Wikipedia:

* Handling both continuous and discrete attributes - In order to handle continuous 
    attributes, C4.5 creates a threshold and then splits the list into those whose 
    attribute value is above the threshold and those that are less than or equal to it.
* Handling training data with missing attribute values - C4.5 allows attribute 
    values to be marked as ? for missing. Missing attribute values are simply not used in gain and entropy calculations.
* Handling attributes with differing costs.
* Pruning trees after creation - C4.5 goes back through the tree once it's been created 
    and attempts to remove branches that do not help by replacing them with leaf nodes.

References:
https://books.google.com/books?id=b3ujBQAAQBAJ&printsec=frontcover#v=onepage&q&f=false
