---
pagetitle: "1. Axioms of Set Theory"
author: https://github.com/9beach

---
# [A solutions manual for Set Theory by Thomas Jech](README.md)
## Part I: Basic Set Theory
### 1. Axioms of Set Theory

**1.1.** Verify (1.1)$\qquad(a, b) = (c, d)$ if and only if $a = c$ and
$b = d$.

**_Proof._**&nbsp;$\quad$If $a=c$ and $b=d$, then $(a,b)=\{\{a\},\{a,b\}
\}=\{\{c\},\{c,d\}\}=(c,d)$. Assume that $(a,b)=(c,d)$ and $a=b$. Then
$\{\{c\},\{c,d\}\}=\{\{a\}\}$, thus $\{c,d\}\in\{\{a\}\}$ and
$\{c\}\in\{\{a\}\}$, so $\{c,d\}=\{a\}=\{c\}$. Hence $c=d=a$. Since it was
assumed that $a=b$, $a=c$ and $b=d$. Assume that $(a,b)=(c,d)$ and $a\neq b$.
Since $\{\{a\},\{a,b\}\}=\{\{c\},\{c,d\}\}$ and $\{a\}\neq\{a,b\}$,
$\{c\} =\{a\}$ and $\{a,b\} =\{c,d\}$. Therefore, $c=a$ and
$d=b$.$\quad\square$

**1.2.** There is no set $X$ such that $P(X)\subset X$.

**_Proof._**&nbsp;$\quad$If $P(X)\subset X$, then there is a
function $f$ from $X$ onto $P(X)$. But the set $Y =\{x\in X : x\notin
f(x)\}$ is not in the range of $f$: If $z\in X$ were such
that $f(z)=Y$, then $z\in Y$ if and only if $z\notin Y$, a contradiction.
Thus $f$ is not a function of $X$ onto $P(X)$, also a
contradiction.$\quad\square$

&nbsp;$\quad$Let
$$
\mathbb{N} =\bigcap\{X : X\text{ is inductive}\}.
$$
$\mathbb{N}$ is the smallest inductive set. Let us use the following notation:
$$
0 =\emptyset,\quad 1 =\{0\},\quad 2 =\{0, 1\},\quad 3 =\{0, 1, 2\},\quad
....
$$
If $n\in\mathbb{N}$, let $n + 1 = n\cup\{n\}$. Let us define $<$ (on
$\mathbb{N}$) by $n < m$ if and only if $n\in m$.\
&nbsp;$\quad$A set $T$ is transitive if $x\in T$ implies $x\subset T$.

**1.3.** If $X$ is inductive, then the set $\{x\in X : x\subset X\}$ is
inductive. Hence $\mathbb{N}$ is transitive, and for each $n, n=\{m\in
\mathbb{N} :m<n\}$.

**_Proof._**&nbsp;$\quad$Let $Y =\{x\in X : x\subset X\}$. Since
$\emptyset\subset X$ and $\emptyset\in X$, $\emptyset\in Y$. Now let
$y\in Y$. Since $Y\subset X$ and $X$ is inductive, $y\in X$, i.e.,
$\{y\}\subset X$, and $y\cup\{y\}\in X$. Since $y\subset X$, $y
\cup\{y\}\subset X$. Thus $y\cup\{y\}\in Y$. Therefore, $Y$ is
inductive.
\
&nbsp;$\quad$Let $Y_\mathbb{N} =\{x\in\mathbb{N} : x\subset
\mathbb{N}\}$, then $Y_\mathbb{N}\subset\mathbb{N}$, and since
$Y_\mathbb{N}$ is inductive, $\mathbb{N}\subset Y_\mathbb{N}$; thus
$\mathbb{N} = Y_\mathbb{N}$, and so we have that $x\in\mathbb{N}$ implies
$x\subset\mathbb{N}$. Therefore, $\mathbb{N}$ is transitive.
\
&nbsp;$\quad$It's clear that $k\in n\cup\{n\}$ if and only if $k
\in n$ or $k = n$. So it follows that for all $k, n\in\mathbb{N}, k< n + 1$
if and only if $k< n$ or $k = n$. Now we show that for each $n, n=\{m\in
\mathbb{N} :m<n\}$ by induction. Let $P(x)$ be the property “$x =\{m
\in\mathbb{N} : m < x\}$”. $P(0)$ holds, and assume that $P(n)$ holds.
$n + 1$ $=$ $n\cup\{n\}$ $=$ $\{m\in\mathbb{N} : m < n\}\cup\{n\}$ $=$
$\{m\in\mathbb{N} : m < n\text{ or } m = n\}$ $=$ $\{m\in\mathbb{N} :
m < n + 1\}$ $=$ $P(n+1)$ holds. Therefore, for each $n, n$ $=$
$\{m\in\mathbb{N} :m<n\}$.$\quad\square$

**1.4.** If $X$ is inductive, then the set $\{x\in X : x\text{ is
transitive}\}$ is inductive. Hence every $n\in\mathbb{N}$ is transitive.

**_Proof._**&nbsp;$\quad$Let $Y =\{x\in X : x\text{ is transitive}\}$.
Since $\emptyset\in X$, and $\emptyset$ is transitive, $\emptyset\in Y$.
Now let $y\in Y$. Since $Y\subset X$ and $X$ is inductive, $y\in X$
and $y\cup\{y\}\in X$. If $z\in y\cup\{y\}$, then either $z\in y$ or
$z = y$; since $y$ is transitive, in any case, $z\subset y\cup\{y\}$. Thus
$y\cup\{y\}$ is transitive, and so $y\cup\{y\}\in Y$. Therefore,
$Y$ is inductive.\
&nbsp;$\quad$Let $Y_\mathbb{N} =\{x\in\mathbb{N} : x\text{ is
transitive}\}$. $Y_\mathbb{N}\subset\mathbb{N}$. Since
$Y_\mathbb{N}$ is inductive, $\mathbb{N}\subset Y_\mathbb{N}$; thus
$\mathbb{N} = Y_\mathbb{N}$. Therefore, every $n\in\mathbb{N}$ is
transitive.$\quad\square$

**1.5.** If $X$ is inductive, then the set $\{x\in X : x$ is transitive
and $x\notin x\}$ is inductive. Hence $n\notin n$ and $n\ne n + 1$ for
each $n\in\mathbb{N}$.

**_Proof._**&nbsp;$\quad$Let $Y =\{x\in X : x$ is transitive and $x
\notin x\}$. $\emptyset\in Y$. Now let $y\in Y$. Since
$Y\subset X$ and $X$ is inductive, $y\in X$ and $y\cup\{y\}\in X$. We
already have that $y\cup\{y\}$ is transitive. Suppose $y\cup\{y\}\in y
\cup\{y\}$. $y\cup\{y\} = y$ or $y\cup\{y\}\in y$, i.e., $y\cup
\{y\}\subset y$; in any case, $\{y\}\subset y$, a
contradiction. Thus $y\cup\{y\}\notin y\cup\{y\}$, and so $y\cup\{y\}
\in Y$. Therefore, $Y$ is inductive.\
&nbsp;$\quad$Let $Y_\mathbb{N} =\{x\in\mathbb{N} : x\text{ is
transitive and } x\notin x\}$, then $Y_\mathbb{N}\subset\mathbb{N}$, and
since $Y_\mathbb{N}$ is inductive, $\mathbb{N}\subset Y_\mathbb{N}$; thus
$\mathbb{N} = Y_\mathbb{N}$, and so $n\notin n$. Suppose $n+1=n$, i.e.,
$n\cup\{n\} = n$, then $\{n\}\subset n$, i.e., $n\in n$; a contradiction.
Therefore, $n\notin n$ and $n\ne n + 1$ for each $n\in\mathbb
{N}$.$\quad\square$

**1.6.** If $X$ is inductive, then $\{x\in X:x$ is transitive and every
nonempty $z\subset x$ has an $\in$-minimal $\text{element}\}$ is
inductive ($t$ is $\in$-_minimal_ in $z$ if there is no $s\in z$ such
that $s\in t$).

**_Proof._**&nbsp;$\quad$Let $P(x)$ be the property "every nonempty $z
\subset x$ has an $\in$-minimal element" and let $Y =\{x\in X : x$ is
transitive and $P(x)\}$.
$\emptyset\in Y$. Let $y\in Y$. Since $Y\subset X$ and $X$ is
inductive, $y\in X$ and $y\cup\{y\}\in X$. We already have that $y
\cup\{y\}$ is transitive. Now we show that
$P(y\cup\{y\})$ holds. $y\notin y$; otherwise
$\{y\}$ $\subset y$ does not have an $\in$-minimal element ($\cdots y\in y
\in y\cdots$), a contradiction. There is no $a\in y$ such that
$y\in a$; otherwise $y\in a\in y\Rightarrow y\in a\subset
y\Rightarrow y\in y$.
Hence for every nonempty $z\subset y$,
if $m$ is an $\in$-minimal element
in $z$ then so is in $z\cup\{y\}$; otherwise $y\in m$, a contradiction.
Similarly, $P(\{y\})$ holds; otherwise $\cdots y\in y\in y\cdots$.
Therefore, $P(y\cup\{y\})$ holds and $Y$ is inductive.$\quad\square$

**1.7.** Every nonempty $X\subset\mathbb{N}$ has an $\in$-minimal
element.\
&nbsp;$\quad$[Pick $n\in X$ and look at $X\cap n$.]

**_Proof._**&nbsp;$\quad$Since $\mathbb{N}$ is the smallest inductive
set, by exercise 1.6, every $n\in\mathbb{N}$ has an $\in$-minimal element.
Let $n\in X$. If $n\cap X =\emptyset$, then
$n$ is an $\in$-minimal element. Suppose not. There exists $m\in X
\smallsetminus n$ such that $m\in n$, but then since $n=\{m\in\mathbb{N}:
m<n\}$, $n\cap X\neq\emptyset$; a contradiction. If $n\cap X\neq
\emptyset$, then $n\cap X$ has an $\in$-minimal element,
and it's an $\in$-minimal element of $X$; otherwise similarly to the
previous, a contradiction.$\quad\square$

**1.8.** If $X$ is inductive then so is $\{x\in X:x=\emptyset$ or $x=y\cup
\{y\}$ for some $y\}$. Hence each $n\ne 0$ is $m + 1$ for some $m$.

**_Proof._**&nbsp;$\quad$Let $A =\{x\in X:x=\emptyset\text{ or }x=
y\cup\{y\}$ for some $y\}$ and let $a\in A$ such that $a\neq\emptyset$. Since $a = y\cup
\{y\}$ for some $y$, so is $a\cup\{a\}$ for $a$, thus
$a\cup\{a\}\in A$. Therefore, $A$ is inductive, and each $n\ne 0$ is
$m + 1$ for some $m$.$\quad\square$

**1.9 (Induction).** Let $A$ be a subset of $\mathbb{N}$ such that $0
\in A$, and if $n\in A$ then $n+1\in A$. Then $A=\mathbb{N}$.

**_Proof._**&nbsp;$\quad$By definition, $A$ is an inductive subset of
$\mathbb{N}$. Therefore, $A =\mathbb{N}$.$\quad\square$

&nbsp;$\quad$A set $X$ _has $n$ elements_ (where $n\in\mathbb{N}$) if there
is a one-to-one mapping of $n$ onto $X$. A set is _finite_ if it has $n$
elements for some $n\in\mathbb{N}$, and _infinite_ if it is not finite.\
&nbsp;$\quad$A set $S$ is _T-finite_ if every nonempty $X\subset P (S)$ has a
$\subset$-maximal element, i.e., $u\in X$ such that there is no $v\in X$
with $u\subset v$ and $u\ne v$. $S$ is T-_infinite_ if it is not T-finite.
(T is for Tarski.)

**1.10.** Each $n\in\mathbb{N}$ is T-finite.

**_Proof._**&nbsp;$\quad$Let $A =\{n\in\mathbb{N} : n\text{ is
T-finite}\}$. We show that $A =\mathbb{N}$ by induction.\
&nbsp;$\quad$$P(\emptyset) =\{\emptyset\}$ has the only nonempty
subset $\{\emptyset\}$ that has a $\subset$-maximal element $\emptyset$.\
&nbsp;$\quad$Let $n\in A$, $X\subset P(n + 1)$, and $Y\subset
P(n)$. $X$ is either $Y$ or $\{x\cup\{n\} : x\in Y$\}. For the latter,
let $a$ be a $\subset$-maximal element of $Y$. Then it's clear that
$a\cup\{n\}$ is a $\subset$-maximal element of $Z$. Therefore, $X$ is
T-finite.$\quad\square$

**1.11.** $\mathbb{N}$ is T-infinite; the set $\mathbb{N}\subset P$
($\mathbb{N}$) has no $\subset$-maximal element.

**_Proof._**&nbsp;$\quad$If $n\in\mathbb{N}$, then there is $n + 1$
such that $n\subsetneq n + 1$. Therefore, $\mathbb{N}\subset P(\mathbb{N})$
has no $\subset$-maximal element.$\quad\square$\
&nbsp;$\quad$_Note that $\mathbb{N}\in P(\mathbb{N})$, $\mathbb{N}
\subset P(\mathbb{N})$, and $\bigcup\mathbb{N} =\mathbb{N}$._

**1.12.** Every finite set is T-finite.

**_Proof._**&nbsp;$\quad$If $F$ is a finite set, then
there is a one-to-one mapping $f$ of $F$ onto some $n\in\mathbb{N}$.
Let ${A}\subset P(F)$ be a nonempty set and let ${B} =
\{ f(X)\subset P(n) : X\in {A}\}$. $B$ has
a $\subset$-maximal element. It's clear that for any $X$ and $Y\in A$,
$X\subset Y$
if and only if $f(X)\subset f(Y)$. Therefore, ${A}$ has a $\subset$-maximal
element.$\quad\square$

**1.13.** Every infinite set is T-infinite.\
&nbsp;$\quad$[If $S$ is infinite, consider $X =\{u\subset S : u\text{
is finite}\}$.]

**_Proof._**&nbsp;$\quad$Since $\emptyset\in X$, $X$ is nonempty. If
$X$ has a $\subset$-maximal element $m$, then $S\smallsetminus m\neq
\emptyset$; otherwise $S$ is a subset of a finite set, a contradiction.
Thus there exists $x\in S\smallsetminus m$, and so $m\subsetneq m\cup
\{x\}\in X$, also a contradiction.$\quad\square$

**1.14.** The Separation Axioms follow from the Replacement Schema.\
&nbsp;$\quad$[Given $\phi$, let $F =\{(x,x) :\phi (x)\}$. Then $\{x
\in X :\phi (x)\} = F(X)$, for every $X$.]

**_Proof._**&nbsp;$\quad$Let $\varphi(x, y)$ be $x = y\wedge
\phi(x)$. $F =\{(x,x) :\phi(x)\} =\{(x,y) :\varphi(x,y)\}$.
Since $\forall x\forall y\forall z(\varphi(x,y)\wedge
\varphi(x,z)\to y = z)$ holds, $\varphi(x,y)$ is a functional
formula. Therefore, we have that The Separation Axioms follow from the
Replacement Schema.\
&nbsp;$\quad$$F(X)$ $=$ $\{y : (\exists x\in X)\varphi(x, y)\}$ $=$
$\{y:(\exists x\in X)x = y\wedge\phi(x)\}$ $=$
$\{x:(\exists x\in X)\phi(x)\}$ $=$
$\{x\in X :\phi (x)\}$.$\quad\square$

**1.15.** Instead of Union, Power Set, and Replacement Axioms consider the
following weaker versions:

&nbsp;$\quad$(1.8) $\forall X\exists Y\bigcup X\subset Y$, i.e.,
$\forall X\exists Y(\forall x\in X)(\forall u\in x)u\in Y$,\
&nbsp;$\quad$(1.9) $\forall X\exists Y P(X)\subset Y$, i.e.,
$\forall X\exists Y\forall u(u\subset X\to u\in Y)$,\
&nbsp;$\quad$(1.10) If a class $F$ is a function, then $\forall X\exists
Y F(X)\subset Y$.

Then axioms 1.4, 1.5, and 1.7 can be proved from (1.8), (1.9), and (1.10),
using the Separation Schema (1.3).

**_Proof._**&nbsp;$\quad$Using the Separation Schema,\
&nbsp;$\quad$(1.8) $\implies$ $\{ x\in Y : (\exists a\in X)x\in a\} =
\bigcup X$,\
&nbsp;$\quad$(1.9) $\implies$ $\{ x\in Y : x\subset X\} = P(X)$,\
&nbsp;$\quad$(1.10) $\implies$ $\{ y\in Y : (\exists x\in X)\varphi(x,y,p)
\} = F(X)$.$\quad\square$
