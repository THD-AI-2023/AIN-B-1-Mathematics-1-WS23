# Summary: Elementary Set Theory and Logic (WS 2023-24)

> Note❗ Markdown mathJax doesn't support `{}`, so for now it is `[]`

## Sets
- **Definition**: Sets are fundamental objects of mathematics and cannot be defined in terms of simpler objects.
- **Notations**:
  - **Element of a set**: $x \in S$
  - **Subset**: $T \subseteq S$
  - **Enumeration**: $[x_1, x_2, ... , x_n]$
  - **Set comprehension**: $[x | x \in S, P(x)]$
- **Important Sets**:
  - Empty set: $\emptyset$
  - Natural numbers: $N = [0, 1, 2, 3, ...]$
  - Integers: $Z$
  - Rational numbers: $Q$
  - Real numbers: $R$
  - Complex numbers: $C$
  - Intervals, e.g., $(a,b), [a,b),$ etc.
  
## Elementary Logic
- **Propositional logic** defines how logical statements can be combined and manipulated.
- **Notations**:
  - **And**: $P \land Q$
  - **Or**: $P \lor Q$
  - **Implies**: $P \Rightarrow Q$
  - **Equivalent**: $P \iff Q$
  - **Not**: $\neg P$
- **Tautology**: A statement always true.

## Quantifiers
- **Universal quantifier**: $\forall x \in S \cdot P(x)$
- **Existential quantifier**: $\exists x \in S \cdot P(x)$
- **Order of quantifiers is important**.

## Operations on Sets
- **Set Equality and Inclusion**:
  - Equality: $X = Y$
  - Inclusion: $X \subseteq Y$
- **Operations**:
  - **Union**: $X \cup Y$
  - **Intersection**: $X \cap Y$
  - **Difference**: $X \setminus Y$
  - **Complement**: $X^c$
  - **Symmetric difference**: $X \Delta Y$
  - **Power set**: $P(X)$
  - **Cartesian product**: $X \times Y$
  - **Disjoint union**: $X \sqcup Y$

---

- **Navigation:**
  - [Summary](#summary-elementary-set-theory-and-logic-ws-2023-24)
    - [Sets](#sets)
    - [Elementary Logic](#elementary-logic)
    - [Quantifiers](#quantifiers)
    - [Operations on Sets](#operations-on-sets)
  - [Elementary Set Theory and Logic](#elementary-set-theory-and-logic)
    - [Sets](#sets-1)
    - [Elementary Logic](#elementary-logic-1)
    - [Quantifiers](#quantifiers-1)
    - [Operations on Sets](#operations-on-sets-1)
    - [Sets as Building Blocks](#sets-as-building-blocks)
  - [Whiteboard Notes](#whiteboard-notes)
    - [Set Builder Notations](#set-builder-notations)
    - [Russell's Paradox](#russells-paradox)
    - [Set Relations](#set-relations)
    - [Mathematical Notations](#mathematical-notations)
    - [Mathematical Statements](#mathematical-statements)
    - [Mathematical Expressions](#mathematical-expressions)
  - [Transitional Phrases in Mathematical Proofs](#transitional-phrases-in-mathematical-proofs)
    
---

# Elementary Set Theory and Logic
## Cezar Ionescu
### WS 2023-24

### Sets

Sets are the most fundamental objects of mathematics. As such, it is impossible to give a definition in terms of "simpler" objects. As Halmos says (Halmos 2017)

> [We assume] that the reader has the ordinary, human, intuitive (and frequently erroneous) understanding of what sets are; the purpose of this exposition is to delineate some of the many things one can correctly do with them.

#### Notation 1.
- Let $S$ be a set. We write $x \in S$ to denote that $x$ is an **element of $S$**, and $x \notin S$ to denote that $x$ is not an element of $S$.
- Let $S$ and $T$ be sets. We write $T \subseteq S$ to denote that $T$ is a **subset of $S$**, i.e., every element of $T$ is also element of $S$.
- Let $S$ be a set and $x_1, x_2, ..., x_n$ be elements of $S$. Then $[x_1, x_2, ... , x_n]$ denotes the set that comprises exactly these elements (enumeration notation).
- Let $S$ be a set and $P$ a family of statements indexed with elements from $S$. Then $[x | x \in S, P(x)]$ denotes the subset of elements of $S$ having the property $P$. This notation is called **set comprehension**.

#### Remark 1.
The set comprehension is used only to select subsets of a given set. Unrestrictive use leads to confusion. Consider the Russell set:

$R = [sets S | S \notin S]$

and the question whether $R \in R$ or not.

#### Notation 2.
We shall use the following notation for important sets:
1. The **empty set** will be denoted by $\emptyset$
2. The set of **natural numbers** will be denoted by $N$:

$N = [0, 1, 2, 3, ...]$

3. The set of integers will be denoted by Z:

$Z = [ ..., -2, -1, 0, 1, 2, ... ]$

4. The set of **rational numbers** will be denoted by $Q$:

$Q = [ \frac{m}{n} \mid m, n \in \mathbb{Z}, n > 0 ]$

5. The set of **real numbers** will be denoted by $R$. It contains all the numbers with a decimal expansion.

6. The set of **complex numbers** will be denoted by $C$:

$C = [ x + yi \, |\, x, y \in R ]$

where $i = \sqrt{-1}$.

7. Let $a, b \in R$. **Intervals** will be denoted by:

$(a,b) = [ x \in R \, |\, a < x < b ]$ 
$[a,b) = [ x \in R \, |\, a \leq x < b ]$ 
$(a,b] = [ x \in R \, |\, a < x \leq b ]$ 
$[a,b] = [ x \in R \, |\, a \leq x \leq b ]$ 
$(a,\infty) = [ x \in R \, |\, a < x ]$ 
$[a,\infty) = [ x \in R \, |\, a \leq x ]$ 
$(-\infty,b) = [ x \in R \, |\, x < b ]$ 
$(-\infty,b] = [ x \in R \, |\, x \leq b ]$

#### Remark 2.
- For any set $S$, we have $\emptyset \subseteq S$
- We have $N \subseteq Z \subseteq Q \subseteq R \subseteq C$.

### Elementary Logic

#### Propositional logic

##### Notation 3.
Let $P$ and $Q$ denote logical statements such as $x \geq y$ or "there exists a $x$, such that $x^2 < 0$".

1. $P \land Q$ denotes the logical statement **P and Q** (that is, both $P$ and $Q$ are true).
2. $P \lor Q$ denotes the logical statement **P or Q** (at least one of $P$ and $Q$ is true).
3. $P \Rightarrow Q$ denotes the logical statement **P implies Q** (if $P$ is true, then $Q$ is also true).

4. $P \iff Q$ denotes the logical statement *P is equivalent to Q*, or *P if and only if Q* (P and Q are either both true, or both false).

5. $\neg P$ denotes the logical statement *not P* (if P is true, then $\neg P$ is false, and the other way around).

---

**Example 1.** The following are tautologies:

- $P \vee \neg P$ (*law of excluded middle*)
- $\neg\neg P \Leftrightarrow P$ (*law of double negation*)
- $\neg(P \land \neg P)$ (*law of contradiction*)
- $(P \land (P \Rightarrow Q)) \Leftrightarrow Q$ (*modus ponens*)

## Quantifiers

Let $P(x)$ be a family of logical statements indexed on the elements of a set $S$, for example $x \ge 0$ for elements in $\mathbb{N}$.

**Notation 4.**
1. The symbol $\forall$ denotes the *universal quantifier* "for all". The statement $\forall x \in S \cdot P(x)$ is true if and only if the statement $P(x)$ is true for every $x \in S$.
2. The symbol $\exists$ denotes the *existential quantifier* "there exists". The statement $\exists x \in S \cdot P(x)$ is true if and only if there exists an element $x \in S$ such that $P(x)$ is true.

**Remark 3.** Note that you must always provide the set $S$ on which the statement $P$ is indexed! For example, $\forall x \in \mathbb{N} \cdot x \ge 0$ is true, but $\forall x \in \mathbb{Z} \cdot x \ge 0$ is false.

**Remark 4.** The order of quantifiers is important! For example, the following statements are not at all equivalent:

$\forall x \in S \cdot \exists y \in T \cdot P(x, y)$

$\exists y \in T \cdot \forall x \in S \cdot P(x, y)$

For example, let $S = T = \mathbb{N}$ and $P(x, y)$ be the statement $x \le y$. Then the first statement says that for any natural number we can always find a bigger one, while the second one states that there is a greatest natural number.

**Proposition 2. (De Morgan’s Laws for quantifiers)** Let $P(x)$ be a family of statements indexed by the elements $x$ of some set $S$. Then

$\neg(\forall x \in S \cdot P(x)) \Leftrightarrow \exists x \in S \cdot \neg P(x)$

$\neg(\exists x \in S \cdot P(x)) \Leftrightarrow \forall x \in S \cdot \neg P(x)$

The proof follows from the meaning of quantifiers.

## Definition 2. (Vacuously true statement)
Whatever the family of statements $P(x)$, the statement $\exists x \in \emptyset \, P(x)$ is always false (since no such $x$ can exist). Therefore the statement

$\neg(\exists x \in \emptyset \, P(x)) \iff \forall x \in \emptyset \, \neg P(x)$

is always true. A statement of the form

$\forall x \in \emptyset \, P(x)$

is called **vacuously true**, and is always true.

## Operations on sets

In what follows, let $X$ and $Y$ be subsets of a set $S$.

Using elementary logic, we can give a formal definition of set equality and inclusion.

### Definition 3.
1. $X = Y \iff \forall x \in S \, (x \in X \iff x \in Y)$
2. $X \subseteq Y \iff \forall x \in S \, (x \in X \implies x \in Y)$

It follows that

### Proposition 3.
$X = Y \iff (X \subseteq Y \, \text{and} \, Y \subseteq X)$

### Definition 4. (Operations on sets)
1. **union**: $X \cup Y = [ x | x \in S, x \in X \text{ or } x \in Y ]$
2. **intersection**: $X \cap Y = [ x | x \in S, x \in X \text{ and } x \in Y ]$
3. **difference**: $X \setminus Y = [ x | x \in S, x \in X \text{ and not } x \in Y ]$
4. **complement**: $X^c = [ x | x \in S, x \notin X ]$
5. **symmetric difference**: $X \Delta Y = X \setminus Y \cup Y \setminus X$
6. **power set**: $P(X) = [ Y | Y \subseteq X ]$

Alternatively:

$Y \in P(X) \iff Y \subseteq X$

7. **cartesian product:** $X \times Y = [(x, y) \mid x \in X, y \in Y]$
8. **disjoint union:** $X \sqcup Y = [(x, 0) \mid x \in X] \cup [(y, 1) \mid y \in Y]$

### Sets as Building Blocks

All the operations we have so far need some pre-existing sets to operate on, but all we need to get started is the empty set `{}` or $\varnothing$, and we can create a universe of sets that can be used to represent all mathematical objects that we need.

For example: the natural numbers. We can use the set $\varnothing$ to stand for zero, this will be our first natural number. So $0 = \varnothing$. Then, we could take:
- $1 = [\varnothing]$, that is, 1 has one element, namely the empty set. Note that this means that 1 is not the same set as 0, since 1 has an element, and 0 has none!
- $2 = [1]$, that is, 2 also has only one element, the number 1. 2 is different from 1, because while both have one element each, the two elements are different in each case.
- $3 = [2]$, and so on. In general, we'll have
    $n + 1 = [n]$

This is **recursive definition**. We have a starting point, $0 = \varnothing$, and a recursive clause, $n+1 = [n]$ which allows us to determine the set representation of any natural number. Conversely, if we are given a set representing a natural number, we can determine what natural number that is. We can even determine if a given set represents or not a given number, by the following algorithm:
- Is the set empty? If yes, it represents the number 0.
- If not, does the set contain more than one element? If so, then it does not represent any natural number.
- If not, then it must have exactly one element, and the answer is determined by applying the algorithm

# **Whiteboard Notes:**

---

$[ 2, 3, 5, 7 ]$
$[ 2, 3, 2, 5, 7, 2 ]$

Set Builder Notations:
$[ x | x \in S, P(x) ]$
$[ x | x \in \mathbb{N}, x \text{ is one of the first four primes } ]$

---

- $[ x | P(x) ]$

Russell's Paradox:
- $R = [ S | S \notin S ]$ (Russell def.)

- $x \in S$

Question:
- Is $R \in R$ ?

    - If yes, then contradiction. Because if $R \in R$, then by definition, $R \notin R$. Therefore, contradiction.

Can't have a set that contains all the universal sets without containing itself?

---

- **Natural Numbers (ℕ)**:  
    ℕ = { 0, 1, 2, ... }

- **Integers (ℤ)**:  
    ℤ = { ... -2, -1, 0, 1, 2, ... }

- **Rational Numbers (ℚ)**:  
    ℚ = { m/n | m ∈ ℤ, n ∈ ℕ > 0 }

- **Real Numbers (ℝ)**:  
    ℝ = { aₘaₙ...a₀.b₁b₂... | aᵢ, bⱼ ∈ {0, 1, ... 9} }

- **Complex Numbers (ℂ)**:  
    ℂ = { x + yi | x, y ∈ ℝ }
    i → "=" $\sqrt{-1}$

- **Interval [a, b]**:  
    [a, b] = { x | x ∈ ℝ, a ≤ x ≤ b }

- **Interval [a, ∞)**:  
    [a, ∞) = { x | x ∈ ℝ, a ≤ x }

---

### Logic Statement
$P \vee \neg P$
Which represents the **Law of Excluded Middle**.

### Set Relations
The relation between sets $X$ and $Y$ can be defined as:

1. $X = Y \iff \forall a (a \in X \Leftrightarrow a \in Y)$
   - This states that two sets $X$ and $Y$ are equal if and only if for any element $a$, $a$ is in $X$ if and only if $a$ is in $Y$.

2. $X \subseteq Y \iff \forall a (a \in X \Rightarrow a \in Y)$
   - This means that set $X$ is a subset of set $Y$ if and only if for every element $a$, if $a$ is in $X$, then $a$ is also in $Y$.

3. $X \neq Y \iff (X \not\subseteq Y \, \text{or} \, Y \not\subseteq X)$
   - This denotes that two sets $X$ and $Y$ are not equal if and only if either $X$ is not a subset of $Y$ or $Y$ is not a subset of $X$.

---

# Mathematical Notations

- The symbol for the empty set: $\varnothing$

- Inclusion notations:
  - $x \notin \varnothing$ *(Note: This indicates that any element 'x' is not a member of the empty set.)*
  - $x = [ ]$ or equivalently $x = \varnothing$
  - $x \neq y$
  - $x \subseteq y$ and $x \not\subseteq y$
  - $\varnothing = [ ]$
  - $\varnothing \subset y$ for any $y$
  - If $x \in \varnothing$, then $x \subseteq [ ]$

- It seems like there are other mathematical relations and symbols scribbled on the board, but without a clear context or order.

---

# Mathematical Statements

- For any element $x$:
  - The statement $x \in \varnothing$ is **false**.
  - Hence, $x \in \varnothing$ implies $x \in [ ]$ is **true**.
  
- Inclusion statements:
  - $\varnothing \subseteq y$
  - $[ ] \subseteq \varnothing$
  - Therefore, $\varnothing = [ ]$

**Transitional Phrases in Mathematical Proofs:**

- For any $x$
- Therefore
- Similarly
- Hence

*Note:* The "tombstone" symbol ☐ indicates the end of the discussion. Another notation used is "q.e.d."

---

## Mathematical Expressions:

1. **Intersection of Sets:**
   - $X \cap Y = [ a \mid a \in X \land a \in Y ]$

2. **Subset:**
   - $X, Y \subseteq S$

3. **Union of Sets:**
   - $X \cup Y = [ a \mid a \in S \land (a \in X \lor a \in Y) ]$

4. **Empty Set:**
   - $\emptyset = [ x \mid x \neq x ]$
