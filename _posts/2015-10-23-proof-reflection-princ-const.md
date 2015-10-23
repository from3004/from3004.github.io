---
layout: post
title: Proof of the Consistency of the Reflection Principle
---
## Proof Sketch

Looking at the space $\\mathcal{A}$ of coherent probability distributions, we'll define a relation $R\\subset A^2$ where $xRy$ intuitively reads as $x$ is believed by $y$. We're looking for a coherent probability distribution $x$ that believes itself, that is $xRx$. We will use Kakutani's fixed point theorem to show that such a distribution must exist.

## Proof

Let us define a relation $R$ which will correspond to our notion that a probability distributions is 'believed' by another probability distribution.
$$xRy \\iff (a<x(\\varphi)<b \\rightarrow y(a<P(\\varphi)<b)=1$$
Intuitively, a reflective $P$ is just a $P$ that 'believes' in itself. That is, a $P$ such that $P \\in f(P)$.
By definition of $R$, a probability distribution $x$ satisfies the reflection principle if and only if $xRx$.
We will show that such a probability distribution exists using Kakutani's fixed point theorem.
Kakutani's fixed point theorem states that, given conditions (1) through (7) below, there exists $x$ such that $xRx$.

(1) $\\mathcal{A}$ is nonempty.

Because $T$ is consistent we can exhibit elements in $\\mathcal{A}$.
Let $T\*$ be a completion of $T$.
Every sentence is either true or false in $T\*$.
Let $\\mathbb{P}(\\varphi) = 1$ for all $\\varphi$ in $T\*$ and $\\mathbb{P}(\\varphi) = 0$ otherwise.
It is easy to see that $x$ is Gaifman coherent and thus an element of $\\mathcal{A}$.
Thus we have shown that $\\mathcal{A}$ is non-empty. Specifically, there is an element for each completion of $T$. However, note that there may be other elements that don't correspond to completions of $T$

(2) $\\mathcal{A}$ is compact.

$[0,1]$ is compact by the Bolzano-Weirstrauss theorem.
Tychonoff's theorem states that the product of any collection of compact topological spaces is compact with respect to the product topology.
Thus, $[0,1]^{L'}$ is compact.
Now, a closed subset of a compact space is compact.
$\\mathcal{A}\\subset [0,1]^{L'}$, so we need only show that $\\mathcal{A}$ is closed.

Fix a $\\varphi$.
We take the infinite sequence $x\_i(\\varphi)\\in\\mathcal{A}$.
We will prove that its limit $x$ is in $\\mathcal{A}$ by showing that the limit must satisfy all three of the Gaifman conditions with respect to $\\varphi$.

Condition 1: $x(\\varphi)\\in [0,1]$.

Note that this is a sequence of real numbers all in the interval $[0, 1]$.
Thus they must converge to a real number within that interval, so $x(\\varphi)\\in[0,1]$.

Condition 2: If $\\varphi$ is logically valid from $T$, then $x(\\phi)=1$.

This condition only applies if $\\varphi$ is logically valid in $T$, so assume that that is true.
Since every $x\_i$ is Gaifman coherent, $\\forall i, x\_i(\\varphi)=1$.
Then, we have a sequence of ones, so this must converge to one. Therefore, $x(\\varphi)=1)$.

Condition 3: $\\forall \\psi, x(\\varphi) -x(\\varphi\\wedge\\psi)-x(\\varphi\\wedge\\neg\\psi)=0$.

(Note that we have rewritten the condition to make this part clearer.)
Fix a $\\psi$.
Since the $x\_i$'s are all Gaifman coherent, $\\forall i\\forall \\psi, x\_i(\\varphi) -x\_i(\\varphi\\wedge\\psi)-x\_i(\\varphi\\wedge\\neg\\psi)=0$
This is a sequence of zeroes, so it must converge to zero, so $x$ fulfills Gaifman condition three.
Note that our choices of $\\varphi$ and $\\psi$ were arbitrary. Thus the conditions hold for all $\\varphi$ and $\\psi$. This implies that the limit $x$ is Gaifman coherent and therefore $\\mathcal{A}$ is closed.
Thus $\\mathcal{A}$ is compact.

(3) $\\mathcal{A}$ is convex.
Given any $x,z\\in\\mathcal{A}$, we will show that if $y$ is a linear combination of $x$ and $z$, then $y$ is Gaifman coherent ant therefore in $\\mathcal{A}$.
Like in the proof for the previous condition of Kakutani's theorem, we start by fixing a $\\varphi$.

Condition 1: $y(\\varphi) \\in [0, 1]$

We know that $x(\\varphi) \\in [0,1]$ and $z(\\psi) \\in [0,1]$.
Thus a linear combination of the two must be in $[0,1]$.

Condition 2: If $\\varphi$ is logically valid from $T$, then $y(\\varphi)=1$.

Assume $\\varphi$ is logically valid from $T$.
Then, $x(\\varphi)=1$ and $z(\\varphi)=1$, so any convex combination of ones must be one.
Thus, $y(\\varphi) = 1$.

Condition 3: $\\forall \\psi, z(\\varphi) -z(\\varphi\\wedge\\psi)-z(\\varphi\\wedge\\neg\\psi)=0$.

The condtion holds for $x(\\varphi)$ and $z(\\varphi)$.
Since convex combinations of zeroes are zero, $y(\\varphi)=0$.
Thus convex combinations of P1 and P2 satisfy all the Gaifman conditions. Thus they are in A. Thus A is convex.
Therefore, convex combinations of Gaifman coherent probability distributions are Gaifman coherent.

(4) $\\mathcal{A}$ is a subset of a locally convex Hausdorff space.

$\\mathcal{A}$ is a subset of $[0, 1]^{L'}$ which is a subspace of $R^{L'}$ which is locally convex and Hausdorff.

(5) $R$ has a closed graph.

Consider a convergent infinite sequence $(x\_i,y\_i)$ such that $\\forall i, x\_iRy\_i$. Say it converges to $(x,y)$.
We will show that $xRy$.
Fix $\\varphi, a, b$ such that $a < x(\\varphi) < b$.
Since $x\_i$ converges to $x$, $\\exists N. \\forall i > n, a < x\_i(\\varphi) < b.$
Since $x\_iRy\_i$, we have by definition that $\\forall i>n: y\_i(a < P(\\ulcorner \\varphi \\urcorner) < b) = 1$
This implies that $y(a < P(\\ulcorner \\varphi \\urcorner) < b) = 1$, or equivalently, $xRy$.
Thus $R$ has a closed graph.

(6) $\\forall x \\exists y$ s.t. $xRy$.

Given an $x\\in\\mathcal{A}$ we can construct a y such that $xRy$.
Take a completion $T^\*$ of the theory $T$ which includes all statements of the form $a < P(\\ulcorner \\varphi \\urcorner) < b$, where $a < x(\\varphi) < b$.
Since $x$ is Gaifman coherent, this theory is consistent.
Let $y$ assign $1$ to all statements in $T^\*$ and $0$ to all statements not in $T^\*$.
This $y$ satisfies $xRy$ and is Gaifman coherent.

(7) $\\forall x$ the set ${y \\in \\mathcal{A}: xRy}$ is convex.

Let $y\_0, y\_2$ be elements of the set ${y \\in A: xRy}$, and let $y\_1$ be any convex combination of $y\_0$ and $y\_2$.
We will show that $xRy\_1$ and therefore $y\_1$ is in the set ${y \\in A: xRy}$
Choose $\\varphi, a, b$ such that $a < x(\\varphi) < b$.
Because $xRy\_0$ and $xRy\_2$, we know that $y\_0(a < P(\\varphi) < b) = 1$ and $y\_2(a < P(\\varphi) < b) = 1$.
Thus $y\_1(a < P(\\varphi) < b) = 1$.
By convexity of $\\mathcal{A}$ we have that $y\_1$ is in $\\mathcal{A}$, so $xRy\_1$.
Therefore, ${y \\in A: xRy}$ is convex.
