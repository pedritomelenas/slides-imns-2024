---
layout: cover
lang: en-en
theme: seriph
coverAuthorUrl: [https://www.ugr.es/local/pedro]
title: "The set of normalized ideals of a numerical semigroup"
coverDate: ""
background: ""
download: true
---

## The set of normalized ideals of a numerical semigroup

<br>

**Pedro A. García Sánchez** <br> Departamento de Álgebra and IMAG, Universidad de Granada
<br> *joint work with L. Casabella, M. D'Anna, S. Tringali, S. Bonzio (in order of appearance)*

<br><br>

### IMNS 2024, Jerez de la Frontera, July 2024

<br><br><br>

<div class="grid grid-cols-[6em_1fr] gap-4">
<div>

![](/logo-junta.png)

</div>
<div>
<br>
<p style="font-size:0.6em;  line-height: 1.5; text-align: left;">Funded by <em>Proyecto de Excelencia de la Junta de Andalucía (ProyExcel_00868)</em>. Proyecto financiado en la convocatoria 2021 de Ayudas a Proyectos de Excelencia, en régimen de concurrencia competitiva, destinadas a entidades calificadas como Agentes del Sistema Andaluz del Conocimiento, en el ámbito del Plan Andaluz de Investigación, Desarrollo e Innovación (PAIDI 2020). Consejería de Universidad, Investigación e Innovación de la Junta de Andalucía. </p>

</div>
</div>


---

# The ideal class monoid 

Let $S$ be a numerical semigroup

An **ideal** of $S$ is a set $I$ of integers such that

- $I+S\subseteq I$
- $z+I\subseteq S$ for some integer $z$ 

Let $\mathcal{I}(S)$ be the set of ideals of $S$

We write $I\sim J$ if there exists $z\in\mathbb{Z}$ such that $I=z+J$

The **ideal class monoid** of $S$ is 

$$
 \mathcal{C}\ell(S) = \mathcal{I}(S)/\sim  
$$

Addition is defined as $[I]+[J]=[I+J]$

---

# The set of normalized ideals 

Let $\mathcal{I}_0(S) = \{ I\in \mathcal{I}(S) : \min(I)=0 \}$, the set of normalized ideals of $S$

It follows easily that

$$
\mathcal{C}\ell(S)\cong \mathcal{I}_0(S), [I]\mapsto -\min(I)+I
$$

For $I\in \mathcal{I}_0(S)$, there exists $g_1,\dots,g_k\in\operatorname{G}(S)$ such that 

$$
I=\{0,g_1,\dots,g_k\}+S
$$

Moreover, $\{g_1,\ldots,g_k\}$ can be taken to be an anti-chain with respect to 

$$a\le_S b  \text{ if } b-a\in S$$

From this we can derive that 

$$
2^{\operatorname{m}(S)-1}+\operatorname{g}(S)-\operatorname{m}(S)+1\le |\mathcal{C}\ell(S)| \le 2^{\operatorname{g}(S)}-2^{\operatorname{g}(S)-\operatorname{t}(S)}+1
$$

---

# Apéry sets

Let $S$ be a numerical semigroup with multiplicity $m$, and let $I\in\mathcal{I}_0(S)$

$$
\operatorname{Ap}(I)= \{ i\in I : i-m\not\in I \}
$$

Notice that if $i\in I$, then $i+km\in I$ for every non-negative integer $k$; thus 

$$
\operatorname{Ap}(I)=\{w_0(I)=0,w_1(I),\dots,w_{m-1}(I)\}
$$ 

where $w_i(I)=\min(I\cap (i+m\mathbb{N}))$

Observe that $I=\operatorname{Ap}(I)+S$

$A=\{0,w_1,\ldots,w_{m-1}\}=\operatorname{Ap}(I)$ for some $I\in\mathcal{I}_0(S)$ if and only if 
$w_i+w_j(S)\ge w_{i+j}$ for all $i,j\in \{0,\dots,m-1\}$ ($i+j$ taken modulo $m$)

---

# Kunz coordinates

For every $i\in\{0,\dots,m-1\}$, $w_i(I)=k_i(I)m+i$

The tuple $(k_1(I),\dots,k_{m-1}(I))$ are the **Kunz coordinates** of $I$; we omitt $k_0(I)=0$

A tuple $(x_1,\dots,x_{m-1})\in\mathbb{N}^{m-1}$ are the Kunz coordinates of an ideal in $\mathcal{I}_0(S)$ if and only if 

$$
\begin{cases}
x_i\le k_i(S), \text{for all } i\in \{1,\dots,m-1\}\\
x_i+k_j(S)+\lfloor \frac{i+j}{m}\rfloor \ge x_{(i+j)\bmod m}, \text{for all } i,j\in \{1,\dots,m-1\}
\end{cases}
$$

<!--There is a one-to-one correspondence between $\mathcal{I}_0(S)$ and the set of non-negative integer solutions of the above system of linear inequalities-->

In particular,

$$
|\mathcal{C}\ell(S) | \le (k_1(S)+1)\times \dots \times (k_{\operatorname{m}(S)-1}(S)+1)
$$


Given $I,J\in \mathcal{I}_0(S)$, we have that 

<center>

$I\subseteq J$ if and only if $(k_1(J),\dots, k_{m-1}(J))\le (k_1(I),\dots,k_{m-1}(I))$

</center>

---

# Hasse diagram of $(\mathcal{I}_0(S),\subseteq)$

Let $S$ be a numerical semigroup with multiplicity $m$

<Transform :scale="0.9">

<div class="grid grid-cols-[60%_40%] gap-4">

<div>

- $\min_\subseteq(\mathcal{I}_0(S))=S$
- $\max_\subseteq(\mathcal{I}_0(S))=\mathbb{N}$

- Maximal non-trivial ideals:  
    
    $\{0,1,\dots,i-1,i+m,i+1,\dots,m-1\}+S$

    $|\operatorname{Maximals}_\subseteq(\mathcal{I}_0(S)\setminus\{\mathbb{N}\})|= m-1$

- Minimal non-tivial ideals: 
    
    $\{0,f\}+S$, $f\in\operatorname{Maximals}_{\le_S}(\mathbb{Z}\setminus S)$
    
    $|\operatorname{Minimals}_\subseteq(\mathcal{I}_0(S)\setminus\{S\})| = \operatorname{t}(S)$, the type of $S$
- Height equals $|\mathbb{N}\setminus S|+1$

</div>

<div>

<figure>

<img src="/NSGraph4.svg" alt="469-ideal-min-gen" width="90%">

<figcaption align="center">

Hasse diagram of $\footnotesize{(\mathcal{I}_0(\langle 4,6,9\rangle),\subseteq)}$, nodes labelled by sets of minimal generators

</figcaption>
</figure>


</div>

</div>

</Transform>

---

# How to fully recover $S$ from $(\mathcal{I}_0(S),\subseteq)$?

*Idea*: $\{0,g\}+S\subseteq \{0,g'\}+S$ if and only if $g'\le_S g$

Thus, if we can tell apart the ideals of the form $\{0,g\}+S$, with $g\in \mathbb{N}\setminus S$, then we recover $(\mathbb{N}\setminus S,\le_S)$

Define $\mathcal{P}_0(S) = \big\lbrace {\{0,g\}+S} : g\in \mathbb{N}\setminus S \big\rbrace\subseteq \mathcal{I}_0(S)$

**Result**: An ideal $I$ is in $\mathcal{P}_0(S)$ if and only if it only covers a unique ideal in the Hasse diagram of $(\mathcal{I}_0(S),\subseteq)$

<div class="absolute left-25% top-48%">

<img src="/469-blind-inclusion.svg" alt="469-ideal" width="40%">

</div>


<div class="absolute left-55% top-60%">

<img src="/469-gaps-blind.svg" alt="469-gap" class="right" width="40%">

</div>

<!--<div class="grid grid-cols-[45%_10%_45%] gap-4">

<div>


<img src="/469-blind-inclusion.svg" alt="469-ideal" style="float:right" width="35%">


</div>

<div>

<br>

</div>

<div>

<img src="/469-gaps-blind.svg" alt="469-gap" class="right" width="40%">


</div>


</div>-->

---

# How to fully reconstruct $S$ from $(\mathbb{N}\setminus S,\le_S)$?

*Idea*: counting "divisors"

For $h\in \mathbb{N}\setminus S$, set $\operatorname{nd}(h)=|\{ h'\in \mathbb{N}\setminus S : h'\le_S h\}|$

**Result:** For every $h,h'\in \mathbb{N}\setminus S$, $h\le h'$, 
$$|S\cap [h,h']| = \operatorname{nd}(h')-\operatorname{nd}(h)$$


<div class="absolute left-20% top-52%">

Our Hasse diaagram

<img src="/469-gaps-n-divs.svg" alt="469-gap-ndivs"  width="75%">


</div>

<div class="absolute left-50% top-52%">

Our semigroup

<br><br><br>
$0$, <v-click> $\textcolor{red}{\sout{1}}$, $\textcolor{red}{\sout{2}}$, $\textcolor{red}{\sout{3}}$, </v-click>  <v-click> $4$, </v-click> <v-click> $\textcolor{red}{\sout{5}}$, </v-click>  <v-click> $6$, </v-click> <v-click> $\textcolor{red}{\sout{7}}$, </v-click> <v-click> 8, 9, 10, </v-click> <v-click> $\textcolor{red}{\sout{10}}$, </v-click> <v-click> $11$, $\to$ </v-click> 

</div>


---

# Poset isomorphism

**Result:** If $S$ and $T$ are numerical semigroups such that the poset $(\mathcal{I}_0(S),\subseteq)$ is isomorphic to $(\mathcal{I}_0(T),\subseteq)$, then $S=T$


If $(\mathcal{I}_0(S),\subseteq)$ is isomorphic to $(\mathcal{I}_0(T),\subseteq)$, then $(\mathbb{N}\setminus S,\le_S)$ is isomorphic to $(\mathbb{N}\setminus T,\le_T)$

From $(\mathbb{N}\setminus S,\le_S)$ and $(\mathbb{N}\setminus T,\le_T)$, we recover $S$ and $T$; the "number of divisors" function is the same in both posets

Thus, $S=T$

---

# Monoid isomorphism problem

If $S$ and $T$ are numerical semigroups such that the monoid $(\mathcal{I}_0(S),+)$ is isomorphic to $(\mathcal{I}_0(T),+)$, can we ensure that  $S=T$?

For $I,J\in \mathcal{I}_0(S)$, write $I\preceq J$ if there exists $K\in \mathcal{I}_0(S)$ such that $I+K=J$


Recall that $S$ is *irreducible* if it is not the intersection of two semigroups properly containing it


1. Oversemigroups of $S$ are precisely the ideals of $\mathcal{I}_0(S)$ such that $I+I=I$ (idempotent)

1. Unitary extensions of $S$ are minimal idempotents with respect to $\preceq$ (idempotent quarks)

1. The genus of $S$ is the maximum $k$ such that there exists a chain $I_0\prec I_1 \prec \dots \prec I_k$ in $\mathcal{I}_0(S)$

1. For $E\in \mathcal{I}_0(S)$, with $E+E=E$, the set $C_E=\{I\in \mathcal{I}_0(S) : I+E=I\}=\mathcal{I}_0(E)$ 

---

# Monoid isomorphism

If $S$ and $T$ are numerical semigroups such that the monoid $(\mathcal{I}_0(S),+)$ is isomorphic to $(\mathcal{I}_0(T),+)$, then  $S=T$?

1. Apply induction on the genus: $S$ and $T$ have the same genus and the same unitary extensions

1. The intersection of all the unitary extensions of $S\neq \mathbb{N}$ equals $S$ or 
   
   $S\cup \{\operatorname{F}(S)\}$ (if $S$ is irreducible)


1. $S$ is irreducible if and only if $\mathcal{I}_0(S)$ has at most two quarks; if $S\neq \mathbb{N}$,
    
   - one quark means symmetric
    
   - two quarks translates pseudo-symmetry

1. In the irreducible case, we recover $\operatorname{F}(S)$ from the genus of $S$

---

# The other (unsolved) poset isomorphism

If $S$ and $T$ are numerical semigroups such that the poset $(\mathcal{I}_0(S),\preceq)$ is isomorphic to $(\mathcal{I}_0(T),\preceq)$, can we ensure that  $S=T$?


<div class="absolute left-35% top-25%">

<img src="/469-dotk.svg" alt="469-dotk" width="55%">


</div>
---

# What if we consider integral ideals?

An ideal $I$ of $S$ is *integral* if $I\subseteq S$; we denote by $\mathfrak{I}(S)$ the set of integral ideals of $S$ 

Set $\mathfrak{P}(S)=\{ a+S : a\in S\}$ the set of principal ideals of $S$


1. $\mathfrak{P}(S)$ is a divisor-closed submonoid of $\mathfrak{I}(S)$
    - For every $a,b\in S$, $(a+S)+(b+S)=(a+b)+S\in \mathfrak{P}(S)$
    - If $I,J\in \mathfrak{I}(S)$ and $I+J\in \mathfrak{P}(S)$, then $I,J\in \mathfrak{P}(S)$

1. Every (non-trivial) divisor-closed submonoid of $\mathfrak{I}(S)$ contains $\mathfrak{P}(S)$ 

1. Isomorphisms between monoids send divisor-closed submonoids to divisor-closed submonoids

1. If $S$ and $T$ are numerical semigroups, every isomorphism between $\mathfrak{I}(S)$ and $\mathfrak{I}(T)$ restricts to an isomorphism between $\mathfrak{P}(S)$ and $\mathfrak{P}(T)$

1. The monoid $\mathfrak{P}(S)$ is isomorphic to $S$ (under the map $a\mapsto a+S$)

---

# Ongoing problems

Let $S$ be a numerical semigroup and denote by $\mathcal{O}(S)$ the set of oversemigroups of $S$, which is the set of idempotent elments of $\mathcal{I}_0(S)$


<div class="grid grid-cols-[60%_40%] gap-4">

<div>

- Study the poset $(\mathcal{O}(S),\preceq)$

    - Detect oversemigroups by Kunz coordinates (done)
    - When is $(\mathcal{O}(S),\preceq)$ a lattice? (done)
    - When is $(\mathcal{O}(S),\preceq)$ a distributive lattice? (done)

- Determine when $\preceq$ equals $\subseteq$ in $\mathcal{I}_0(S)$

- Determine when $(\mathcal{I}_0(S),\preceq)$ is a lattice (done)


All these properties hold when the multiplicity of $S$ is small

</div>

<div>

<figure>
<img src="/31317.svg" alt="31317" width="75%">

<figcaption>

<p style="font-size:0.8em">

Hasse diagram of $(\mathfrak{I}_0(\langle 3,13,17\rangle),\preceq)$; nodes <br> labelled with their Kunz coordinates

</p>

</figcaption>
</figure>

</div>

</div>


---

# References

- V. Barucci, F. Khouja, On the class semigroup of a numerical semigroup, Semigroup Forum, 92 (2016), 377-392

- S. Bonzio, P. A. García-Sánchez, Posets and lattices of normalized ideals of numerical semigroups, in progress

- L. Casabella, M. D'Anna, P. A. García-Sánchez Apéry sets and the ideal class monoid of a numerical semigroup, Mediterr. J. Math. 21:7 (2024)

- P. A. García-Sánchez, The isomorphism problem for ideal class monoids of numerical semigroups, Semigroup Forum 108 (2024), 365–376.

- P. A. García-Sánchez, S. Tringali, Isomorphism problems for ideal semigroups and power semigroups, preprint (2024)

- M. Delgado,  P.A.  García-Sánchez,  and  J. Morais, NumericalSgps, A package for numerical semigroups, Version 1.3.1 (2022), (Refereed GAP package), https://gap-packages.github.io/numericalsgps

---
layout: cover
background: ""
---

# Thank you for your attention!

Find our more at [numerical-semigroups.github.io](http://numerical-semigroups.github.io/)

Slides produced with [slidev](https://es.sli.dev/)