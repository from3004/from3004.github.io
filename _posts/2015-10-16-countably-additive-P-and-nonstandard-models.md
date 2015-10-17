---
title: Countably additive $\mathbb{P}$ and nonstandard models
layout: post
---
Background: Definability of Truth
***
We interpret a reflective $\mathbb{P}$ as a finitely additive measure over complete theories.
Abusing notation, we sometimes write $\mathbb{P}(\phi)$ and sometimes $\mathbb{P}(\{T:T\phi\in T\})$.
Define a standard theory as a pair $(\mathbb{N}, \overline{P})$, where $\mathbb{N}$ is the standard model of the natural numbers and $\overline{P}$ is a three place relation over naturals which satisfies the Gaifman conditions.
We claim that if $\mathbb{P}$ is countably additive, then it must assign probability zero to standard theories
***
Consider the sentence $G$ defined by $G \iff P(G) < 1$.
Then, $\mathbb{P}(G)=1$.
Applying the reflection principle, we get that 
$\forall\epsilon>0,\mathbb{P}(\{T:1-\epsilon<P(G)<1\in T\})=1.$
Now, $\{T:\forall \epsilon>0,1-\epsilon<P(G)<1\in T\}=\bigcap_{\epsilon>0}\{T:1-\epsilon<P(G)<1\in T\}$, so we applying countable additivity and De Morgan's law to get that $\mathbb{P}(\{T:\forall \epsilon>0,1-\epsilon<P(G)<1\in T\})=1$.
This means that any theory which does not have $\forall \epsilon>0,1-\epsilon<P(G)<1$ as an axiom, will be assigned probability zero by $\mathbb{P}$.
In particular, no standard theory can have such an axiom, as otherwise it would contain a number smaller than one which was also greater than any standard rational smaller than one.
