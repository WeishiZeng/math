script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

**The Cauchy-Schwarz Inequality**
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$


This sentence uses `$` delimiters to show math inline:  $\sqrt{3x-1}+(1+x)^2$

# Natural Numbers

## Peano Axioms

- **(Axiom 2.1)** Zero
    - 0 is a natural number
- **(Axiom 2.2)** $++$, the increment operation
    - if $n$ is a natrual number, then $n++$ is also a natural number.
- **(Axiom 2.3)** $0$ is the first
    - $n++ \neq 0$ for every natrual number n
- **(Axiom 2.4)** Uniqueness of increment
    - $n \neq m \implies n++ \neq m++$
- **(Axiom 2.5)** Principal of mathimatical induction
    - $[P(0) \land (P(n) \implies P(n++))] \implies [\forall n P(n)]$
      - $P(n)$ is a property pertaining to natural number $n$
- **(Proposition 2.2.14)** Strong principal of induction
    - $(\forall m \ge m_0) [[(\forall m_0 \le m' < m) P(m') \implies P(m)] \implies (\forall m \ge m_0) P(m)]$
      - $m_0$ is any natrual number, $P(m)$ is a property pertaining to natural number $m$
    - Break down version:
      - $\forall m_0 [(\forall m \ge m_0) Q(m) \implies (\forall m \ge m_0) P(m)]$
      - $Q(m)$ is defined as:
        - $(\forall m_0 \le m' < m) P(m') \implies P(m)$


## Precedence of logical operator
> The convention is described by Herbert Enderton in [A Mathematical Introduction to Logic](https://books.google.it/books?id=dVncCl_EtUkC&pg=PA78) page 78.

| Operator             | Name           | Precedence     |
| -------------------- | -------------- | -------------- |
| $\forall$, $\exists$ | Modifier       | Highest, apply to as little as possible |
| $\lnot$              | Negation       | Highest, apply to as little as possible |
| $\land$             | Conjunction    |
| $\lor$               | Disjunction    |
| $\implies$        | Implication    | Right associative |
| $\iff$    | Biconditional  |

- Examples (todo: Not convinced!!!)
    - $¬α ∧ β$ is $((¬α) ∧ β)$, and not $¬(α ∧ β)$
    - $∀x α → β$ is $(∀x α) → β$, and not $∀x(α → β)$
    - $∃x α ∧ β$ is $(∃x α) ∧ β$, and not $∃x(α ∧ β)$.
    - $α → β → γ$ is $α → (β → γ)$.

## Logic
- $\forall$ Equivalent
  - $(\forall x \in X)  Q(x)$
  - $\forall x [x \in X \implies Q(x)]$
- $\exists$ Equivalent
  - $(\exists x \in X)  Q(x)$
  - $\exists x [x \in X \land Q(x)]$

## Axioms of Equality (A.7)
How equality is defined depends on the class type of objects under consideration. But all **equality definition** should obey the following four axioms of equality:
1. Reflexive axiom.
    - Given any object x, we have x = x.
1. Symmetry axiom.
    - Given any two objects x and y of the same type, if x = y, then y = x.
1. Transitive axiom.
    - Given any three objects x, y, z of the same type, if x = y and y = z, then x = z.
1. Substitution axiom.
    - Given any two objects x and y of the same type, if x = y, then f(x) = f(y) for all functions or operations f.
    - Similarly, for any property P(x) depending on x, if x = y, then P(x) and P(y) are equivalent statements.
    - Note, when introducing an opertion to objects of type T, it's considered a **well-defined** operation only if it follows the Substitution axiom.



# Set Theory
## Axiom vs. Definition
An axiom is a assumption/rule that we decide we will follow/enforce.
Axioms come mainly in two different kinds: existential and universal.
1. Existential: there exists an empty set
2. Universal: all right angles are equal (?)


### ZFC Axiom of Set Theory
- *(Definition 3.1.1)* Informal Set
    - A set is unordered collection of objects(*)
    - If $x$ is an object, then
        - $x$ is an element(*) of set A, i.e. $x \in A$, if $x$ lies in the collection
        - $x \notin A$, if $x$ does not lie in the collection
- **(Axiom 3.1)** Sets are objects
    - A is a set => A is an object
        - In particular, given set A and B, it's meaningful to ask if $A \in B$
- *(Definition 3.1.4)* Equality
    - $A = B \iff \forall x [(x \in A \implies x \in B) \land (x \in B \implies x \in A)]$
- **(Axiom 3.2)** Empty set exists
    - $(\exists \emptyset) (\forall \:object\:x ) x \notin \emptyset$
- *(Lemma 3.1.6)* Single choice
    - $A \neq \emptyset \implies \exists x (x \in A)$
    - Note: the antecedent assumes non empty set A exists. this lemma does NOT prove that A exists
- **(Axiom 3.3)** Singleton/pair sets exist
    - Singleton $\{a\}$: $\forall (object \: a) \exists A \forall (object \: y) (y \in A \iff y = a)$
    - Pair $\{a, b\}$: $\forall (object \: a) \forall (object \: b) \exists A \forall (object \: y)(y \in A \iff y = a \lor y = b)$
- **(Axiom 3.4)** Pairwise union exists
    - $\forall A \forall B [A \cup B \: exists]$
    - $A \cup B$ is defined as:
      - $\forall x (x \in A \cup B \iff x \in A \lor x \in B)$
- *(Defnition 3.1.15)* Subsets
    - $A \subseteq B \iff \forall \:object\:x (x \in A \implies x \in B)$
- **(Axiom 3.5)** Axiom of specification/separation
    - Set $\{x \in A \mid P(x)\}$ exists
    - And it's defined as: $(\forall y) [y \in \{x \in A \mid P(x)\} \iff y \in A \land P(y)]$
- *(Defnition 3.1.23)* Intersections
    - $S_1 \cap S_2 := \{x \in S_1 \mid x\in S_2 \}$
    - In other words: $x \in S_1 \cap S_2 \iff x \in S_1 \land x\in S_2$
- *(Defnition 3.1.27)* Difference Sets
    - $A \backslash B := \{x \in A \mid x\notin B \}$
- **(Axiom 3.6)** Replacement
    - $(\forall x \in A) \forall y \{[\forall y_1 \forall y_2 (P(x,y1) \land P(x,y2) \implies y_1 = y_2)] \implies Set \: \{y | (\exists x \in A) P(x,y) \} \: exists \}$
      - Informal: $(\forall x \in A) \forall y [\text{at most one y for any x, s.t. P(x,y) holds} \implies \: \{y | (\exists x \in A) P(x,y) \} \text{exists}]$
    - $z \in \{y | (\exists x \in A) P(x,y) \} \iff (\exists x \in A) P(x,z)$
- **(Axiom 3.7)** Infinity
    - $\mathbb{N}$ exists, and its elements are called natural numbers.
    - $0 \in \mathbb{N} \land (n \in \mathbb{N} \implies n++ \in \mathbb{N})$ and Peano Axiom holds
- **(Axiom 3.8)** Universal specification (**Not chosen**)
  -  $\forall P [\forall x P(x) \: exists \implies \{x \mid P(x)\} \: exists]$
  - And it's defined as: $(\forall y) [y \in \{x \mid P(x)\} \iff P(y) \: is \: true]$
- **(Axiom 3.9)** Regularity/Foundation
  -  $(\forall set A \neq \emptyset) (\exists x \in A) [x \: is \: not \: a \: set \lor x \cap A  = \emptyset]$
- **(Axiom 3.10)** Power set
  -  $(\forall set X) (\forall set Y) (Y^X \: exists)$
  - $Y^X := \{f | f: X \to Y \}$
    - $f \in Y^X \iff f \: is \: a \: function \: with \: domain \: X \: and \: range \: Y$
- **(Axiom 3.11)** Union
  -  $(\forall x \in A) [x \: is \: a \: set] \implies \bigcup A \: exists$
  - $\bigcup A$ is defined as:
    - $x \in \bigcup A \iff (\exists S \in A) x \in S$
  - $\bigcup_{\alpha \in I} A_{\alpha} := \bigcup\{A_\alpha | \alpha \in I\}$
    - $x \in \bigcup_{\alpha \in I} A_{\alpha} \iff (\exists \alpha \in I) x \in A_\alpha$
  - $\bigcap_{\alpha \in I} A_{\alpha} := \{x \in A_\beta | (\forall \alpha \in I) x \in A_\alpha\}$
    - $x \in \bigcap_{\alpha \in I} A_{\alpha} \iff (\forall \alpha \in I) y \in A_\alpha$

## Functions
- *(Definition 3.3.1)* Functions
    - $(\forall set X) (\forall set Y) [(\forall x \in X) (\exists! y \in Y )P(x, y) \implies (\exists f: X \to Y) (\forall x \in X) (\exists! f(x) \in Y) P(x, f(x))]$
- *(Definition 3.3.7)* Equality of Functions
    - Consider two functions $f : X \to Y$ and $g : X \to Y$
      - Note $f$ and $g$ have the same domain and range.
    - $f = g \iff (\forall x \in X) [f(x) = g(x)]$
- *(Definition 3.3.10)* Composition
    - Consider two functions $f : X \to Y$ and $g : Y \to Z$
    - $(g \circ f)(x):= g(f(x))$
- *(Definition 3.3.14)* One-to-one functions (injective)
    - $x \neq x' \implies f(x) \neq f(x')$
- *(Definition 3.3.17)* Onto functions (Surjective)
    - Often written as $f(X) = Y$
    - $(\forall y \in Y) (\exists x \in X) f(x) = y$
- *(Definition 3.3.20)* Bijective functions (invertible)
    - both bijective and surjective; also called "perfect matching", "one to one correspondence".
    - $(\forall y \in Y) (\exists! x \in X) f(x) = y$
      - At least one $x$ because of surjectivity, and at most one $x$ because of injectivity
    - $(\forall x \in X) (\exists! y \in Y) f(x) = y$ by definition of "function"
    - ![bijective](img/function-bijective.png "Functions")
- *(Excercise 3.3.8)* Inclusion map (iota)
    -  $X \subseteq Y$, Inclusion map $\iota_{X \to Y}: X \to Y$ is defined as:
    - $(\forall x \in X) \iota_{X \to Y}(x):=x$
    - Identity map: $\iota_{X \to X}: X \to X$
- *(Definition 3.4.1)* Image of sets
    - $f(S) := \{f(x) | x \in S \}$
      - $|$ reads: "for some"
      - $y \in f(S) \iff (\exists x \in X) y = f(x)$
      - $f : X \to Y$, $S \subseteq X$, $f(S) \subseteq Y$
- *(Definition 3.4.4)* Inverse Images
    - $f^{-1}(U) := \{x \in X | f(x) \in U \}$
      - $|$ reads: "such that", "and"
      - $x \in f^{-1}(U) \iff f(x) \in U$
      - $f : X \to Y$, $U \subseteq Y$
- Function and set with |
    - *(Axiom 3.5 Specification)* Set $\{x \in A | P(x)\}$ exists
    - *(Axiom 3.6 Replacement)* Set $\{y | (\exists x \in A) P(x,y) \}$ exists
      - $z \in \{y | (\exists x \in A) P(x,y) \} \iff (\exists x \in A) P(x,z)$
    - *(Example 3.1.32)* $\{f(x) | x \in A \}$
      - shorthand for: $\{ y | y = f(x) \text{ for some } x \in A\}$
      - $y \in \{f(x) | x \in A \} \iff (\exists x \in A) y = f(x)$
    - *(Definition 3.4.1)* $f(S) := \{f(x) | x \in S \}$

### Cartesian Product of Set
- *(Definition 3.5.1)* Ordered pair
    - Ordered pair exists: $\forall x \forall y \exists (x,y)$
      - Proof by construction: $(x, y) := \{\{x\}, \{x, y\}\}$
    - Ordered pair equality: $(x, y) = (x', y') \iff x = x' \land y = y'$
- *(Definition 3.5.4)* Cartesian Product (Collection of ordered pairs)
  - $X \times Y := \{(x, y) | x \in X \land y \in Y\}$
    - $X \times Y$ is a set, and it exists.
    - $|$ reads "for some"
    - $a \in (X \times Y) \iff (\exists x \in X) (\exists y \in Y) a = (x, y)$
- *(Definition 3.5.7)* Ordered n-tuple and n-fold cartesian product
  - Ordered n-tuple
    - Notation
      - $(x_i)_{1 \leq i \leq n}$
      - $(x_1, ..., x_n)$
    - Equality
      - $(x_i)_{1 \leq i \leq n} = (y_i)_{1 \leq i \leq n} \iff (\forall i \in \{1,...,n\}) x_i = y_i$
  - N-fold cartesian product (of an ordered n-tuple of sets)
    - Notation
      - $X^n$
      - $\prod_{1 \leq i \leq n} X_i$
      - $\prod_{i=1}^n X_i$
      - $(X_1 \times ... \times X_n)$
    - Definition
      - $\prod_{1 \leq i \leq n} X_i := \{(x_i)_{1 \leq i \leq n} | (\forall i \in \{1,...,n\}) x_i \in X_i\}$
        - $a \in \prod_{1 \leq i \leq n} X_i \iff [(\forall i) [(1 \leq i \leq n) \implies(\exists x_i) x_i \in X_i]] \land a = (x_j)_{1 \leq j \leq n}$
- *(Excercise 3.5.7)* Coordinate Function and Direct Sum
  - Coordinate functions on $X \times Y$
    - $\pi_{X \times Y \to X} : X \times Y \to X$ and $\pi_{X \times Y \to X}(x,y) := x$
    - $\pi_{X \times Y \to Y} : X \times Y \to Y$ and $\pi_{X \times Y \to Y}(x,y) := y$
  - $(\forall f : Z \to X) (\forall g : Z \to Y) (\exists! h : Z \to X \times Y) \pi_{X \times Y \to X} \circ h= f \land \pi_{X \times Y \to Y} \circ h= g$
    - $h$ is the direct sum of $f$ and $g$, denoted $h := f \bigoplus g$
- *(Excercise 3.5.10)* Graph
  - $f : X \to Y$ is a function
  - Graph of $f$ is a set: $\{(x, f(x)) | x \in X\}$


## Format
$$
When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$
$$
R_{\mu \nu} - {1 \over 2}g_{\mu \nu}\,R + g_{\mu \nu} \Lambda
= {8 \pi G \over c^4} T_{\mu \nu}
$$
