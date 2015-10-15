---
layout: post
title: Measures and Countably Additive Measures
---

In the course of writing up the new Definability of truth paper, I ran into a result that has not been written up.
This result has to do with how a reflective measure over some theory has assigns probability to standard models of PA given whether it is finitely or countably additive.

Now, while writing this result up on IAFF, I have run into a number of confusions surrounding measures. This post is my attempt to resolve these.

***

I don't like the few ways of introducing the concept that I have seen, so I am going to start by discussing some geometric intuitions.

Lines seem to have length; shapes seem to have area. Solids have volume. Objects have mass.
Usually, we think of these as well defined quantities.
The goal of defining measures is to capture the abstract and general properties of these intuitions.

So, what do length, area, volume, and mass have in common?

* One can add lengths of disjoint segments to get the total length of all those segments together.
* The length of an empty segment is zero.
* There is no such thing as negative length.

There are additional properties that these four have in common, but none are as salient or simple as the above.
Let's formalize these conditions.

We work in ZFC. (I will comment briefly later on why the specific choice of set theory is so important.)
We previously discussed assigning numbers, which we called lengths, to line segments.
A line segment is some interval in $\mathbb{R}$; shapes, solids, and so forth are similarily subsets of some $\mathbb{R}^n$.

Note that we don't want to restrict ourselves to just intervals.
It is easy to talk about the area of an object which consists of two disjoint squares.
We wish to generalize these assignments of lengths or areas, so let us jump to talking about subsets of $\mathbb{R}^n$ and functions from the powerset of $\mathbb{R}^n$ to the reals.

Let's call such a function $\mu$ a measure if it has the following properties:

1. $\mu(\emptyset)=0$
2. $\mu(A)\geq 0$
3. $A\cap B=\emptyset \Rightarrow \mu(A\cup B)=\mu(A)+\mu(B)$

These are exactly the similarities we noticed above, except put in symbols.

It seems like this should be sufficient, but I claim this fails in some cases we care about and that what looks like the obvious fix leads to more problems.

***

[TODO. I note that I am still confused about this next bit, as I cannot reconstruct the reasoning nor point to places where integration fails nor even articulate what sort of failures occur:
When calculating areas of less regular shapes, the tool of choice is integration. However, the "measure" we defined above does not have nice properties in general when integrated over.]
It turns out we can patch this fairly easily by adding another condition:

4. $\mu(\bigcup_i A_i)=\sum_{i}\mu(A_i)$ where all $A_i$s are disjoint.

We call this countable additivity and note that it subsumes condition 3 in the case of a union of just 2 disjoint sets.

Yet, this has an even more interesting failure mode.

[TODO. I also don't actually understand how this works: 
It turns out that if we just defini our measur over the power set of qhatever set we are interersted in, things break.
An example is the Banach-Tarski paradox, which shows that decomposing a ball into a finite number of sets of points and recombining them can yield a larger ball.
The problem here is that what we defined as measure does not match our intuitions about lengths and areas under certain transformations.
]

[TODO. Write about how to 
