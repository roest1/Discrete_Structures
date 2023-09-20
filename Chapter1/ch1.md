# Discrete Structures

Discrete is finite; like calculus is continuous.

When we perform operations on numbers in discrete mathematics, we expand our knowledge of the structure in which math presents itself to the world.

- The most obvious example of this, are number sets

$\mathbb{N}$ - Natural numbers (**Discrete**)

$\mathbb{Z}$ - Integers (**Discrete**)

$\mathbb{Q}$ - Rational numbers (**Discrete**)

- With rational numbers, it's always possible to find at least one rational and one irrational number within *any* two rational numbers. However, they are countable, so we consider them discrete.

$\mathbb{R}$ - Real numbers (**Continuous**) 
     
- The domain of real numbers is called 'The continuum'.

> It is important to be creative in Discrete Structures

## Table of contents
1. Logic and Proofs
2. Induction
3. Recurrences
4. Counting
5. Sets, Functions, Relations
6. Discrete Probability
7. Trees & Graphs

---

**TERMS**

*Logic* - The basis of all mathematical and automated reasoning.
    
*Proof* - What makes the reasoning correct.

*Theorem* - Mathematical statement that's been proven to be true.

*Proposition* - Basic building block of all logic.
     
- A proposition can be true or false (NOT BOTH)

*Declarations* - Sentence that declares a fact.
     
- Be wary, declarations are not always true!

### Propositional Logic


Here, we formulate new math with **Compound Propositions**.
     
- new propositions formed from the combination of one or more prior propositions

⋆ To learn a math subject well, one must actively construct mathematical arguments on a given topic. It is stressed that one must not rely on exposition.

⋆ Knowing the proof to a theorem often makes it possible to manipulate the theorem in a flexible manner for alternative cases.

--- 
## Logical Operators

- Language processing

(creating compound propositions)

1. **Negation** -  **$¬  p$**            

2. **Conjunction** - **$p ∧ q$** 

     - True iff p AND q are true and false otherwise

3. **Disjunction** - **$p ∨ q$**       
⋆ *Inclusive*
     - False iff p AND q are false and true otherwise

4. **Exclusive Or** - **$p ⊕ q$**    

     - True iff ONLY ONE of p and q is true and false otherwise

5. **Conditional Statement** - **$p → q$**             
*⋆ Implication*
     - False iff the premise is true and the conclusion is false and true otherwise

> It is good to note :  This statement is asserting q to be true, given p is true.

6. **Bi-Conditional Statement** - **$p ↔ q$**               
  *⋆ iff*
     - True iff p equals q and false otherwise 
> Opposite : Negator of exclusive or (4.)

### Truth Table of Operators so far

| $p$ | $q$ | $p ∧ q$ | $p ∨ q$ | $p ⊕ q$ | $p → q$ | $p ↔ q$ |
| - | - |  -  | - | - | - | - |
| T | T | T | T | F | T | T | 
| T | F | F | T | T | F | F | 
| F | T | F | T | T | T | F | 
| F | F | F | F | F | T | T | 

---

  Computers use bits, where each bit is represented by boolean value. Bit operations, correspond to logical connectives. {∨ = OR, ∧ = AND, ⊕ = XOR, etc.}

  **The Conditional Statement**
  
  $$p → q$$
  The following statements are known to be equivalent to the implication : 
 
  - *The Converse* = $q → p$ (**Not always true**)
  - *The Inverse* = $¬ p → ¬ q$ (**Not always true**)
  - *The Contrapositive* = $¬ q → ¬ p$ (**Always true**)

  ### Precedence of Logical Operators

  1. $¬$  (Negator) 
  2. $∧$ (Conjunction)
  3. $∨$ (Disjunction)
  4. $→$ (implication)
  5. $↔$ (BiConditional implication)

  > When in doubt, use parentheses.
  
  ---

  Notice the truth equivalence : 

  $$p ∨ ⇁q → p ∧ q $$

| $p$ | $q$ | $¬ q$ | $p ∨ ¬ q$ | $p ∧ q$ |$p ∨ ¬ q → p ∧ q$ |
| - | - | - | - | - | - |
| T | T | F | T | T | T |
| T | F | T | T | F | F |
| F | T | F | F | F | T | 
| F | F | T | T | F | F |

Notice : 

**$$p ∨ ¬ q ⟹ p ∧ q ≡ q$$**

---

### Translating Sentences into Logical Equivalences

"You have a CS email account only if you are a CS major or you take a CS course"

- $p := \text{"you have a CS email account"}$
- $q := \text{"you are CS major"}$
- $r := \text{"you take a CS course"}$

$$p ↔ q ∨ r$$

"You cannot ride the roller coaster if you are under 4ᶠᵗ  tall unless you are older than 16"

- $p := \text{"you cannot ride the roller coaster"}$
- $q := \text{"you are under 4ᶠᵗ tall"}$
- $r := \text{"you are older than 16"}$

$$q ∨ ¬r ⟹ p$$ 

### Logic Puzzle

On an island, there are two types of people. One always tells the truth, and the other always lies.

- **A says** := "B always tells the truth"
- **B says** := "We are opposite types"

     = In fact, both are lying since they contradict our given premise.

--

There are 3 white hats and 2 black hats. Three men stand in a line in a dark closet. The men can infer their hat color given their order in line.
Two men don't know their hat color. What color is the one that knows?

          (1.) ←  (2.)  ← (3.)

     = (1.) Knows their color is white.

--

There's a room full of 16 people. Everyone is wearing a hat and at least one person has a white hat. On the 10ᵗʰ day, 10 people know their hat color. What color are the hats? Why?

     = As the days go, one more person finds their hat color is white.

---

In mathematics, we can replace statements that share the same truth value with their propositional equivalences.

Logic is analogous to algebra when it comes to operations.

**$p ∨ ¬ p$**  **Tautology** = A compound proposition which is always true.

**$p ∧ ¬ p$** **Contradiction** = A compound proposition that is always false.

> p → q ≡ ¬ p ∨ q

| $x$ | $y$ | $x ∨ y$ | $x ∧ y$ | $x ⊕ y$ | $x → y$ | $x ↔ y$ |
| - | - | - | - | - | - | - |
| 1 | 1 | 1 | 1 | 0 | 1 | 1 |
| 1 | 0 | 1 | 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 | 1 | 1 | 0 | 
| 0 | 0 | 0 | 0 | 0 | 1 | 1 |

---

A *Bit String* is a sequence of zero or more bits.

EX : 101010011
is a bit string with length = 9.

Find bitwise AND, OR and XOR of the bit strings : 
**01 1011 0110** and **11 0001 1101**

1. OR
**01 1011 0110**
**11 0001 1101**
                                                 
                                                 __________________
                                                 = 11 1011 1111 
2. AND

**01 1011 0110** 
**11 0001 1101**
                                                 
                                                 __________________
                                                 = **01 0001 0100**
3. XOR

**01 1011 0110** 
**11 0001 1101**
                                                 
                                                 __________________
                                                 = 10 1010 1011


System specifications should be consistent, meaning they should not contain any conflicting requirements that could be used to derive a contradiction.


## LAWS OF EQUIVALENCE

---

<div style="text-align: center"> IDENTITY LAWS </div>

$$p ∧ T₀ ≡ p$$
$$p ∨ F₀ ≡ p$$

<div style="text-align: center"> DOMINATION LAWS </div>

$$p ∨ T₀ ≡ T₀$$
$$p ∧ F₀ ≡ F₀$$

<div style="text-align: center"> IDEMPOTENT LAWS </div>

$$p ∨ p ≡ p$$
$$p ∧ p ≡ p$$

<div style="text-align: center"> DOUBLE NEGATION LAW </div>

$$¬ (¬ p) ≡ p$$

<div style="text-align: center"> COMMUTATIVE LAWS </div>

$$p ∨ q ≡ q ∨ p$$
$$p ∧ q ≡ q ∧ p$$

<div style="text-align: center"> ASSOCIATIVE LAWS </div>

$$(p ∨ q) ∨ r ≡ p ∨ (q ∨ r)$$
$$(p ∧ q) ∧ r ≡ p ∧ (q ∧ r)$$

<div style="text-align: center"> DISTRIBUTIVE LAWS </div>

$$p ∨ (q ∧ r) ≡ (p ∨ q) ∧ (p ∨ r)$$
$$p ∧  (q ∨ r) ≡ (p ∧ q) ∨  (p ∧ r)$$

<div style="text-align: center"> DEMORGAN'S LAWS </div>

$$¬ (p ∧ q) ≡ ¬ p ∨ ¬ q$$
$$¬ (p ∨ q) ≡ ¬ p ∧ ¬ q$$

<div style="text-align: center"> ABSORPTION LAWS </div>

$$p ∨ (p ∧ q) ≡ p$$
$$p ∧ (p ∨ q) ≡ p$$

<div style="text-align: center"> NEGATION LAWS </div>

$$p ∨ ¬ p ≡ T₀$$
$$p ∧ ¬ p ≡ F₀$$

---

Some examples of equivalences :

$a → b ≡ ¬ a ∨ b$

| $a$ | $b$ | $a → b$ | $¬ a$ | $¬ a ∨ b$ | 
| - | - | - | - | - |
| 1 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 
| 0 | 1 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 |

$a ∨ (b ∧ c) ≡ (a ∨ b) ∧ (a ∨ c)$

| $a$ | $b$ | $c$ | $b ∧ c$ | $a ∨ (b ∧ c)$ | $a ∨ b$ | $a ∨ c$ | $(a ∨ b) ∧ (a ∨ c)$ |
| - | - | - | - | - | - | - | - |
| 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 1 | 1 | 1 | 1 |
| 1 | 0 | 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

T₀ = Tautologies
F₀ = Contradictions

**If all values in the domain can be listed :**

$$∀xP(x) = P(x₁) ∧ P(x₂) ∧ ... ∧ P(xₖ)$$

and 

$$∃xP(x) = P(x₁) ∨ P(x₂) ∨ ... ∨ P(xₖ)$$

## CONDITIONAL EQUIVALENCES 

---

$$p → q ≡ ¬ p ∨ q$$
$$p → q ≡ ¬ q → ¬ p$$
$$p ∨ q ≡ ¬ p → q$$
$$p ∧ q ≡ ¬ (p → ¬ q)$$
$$¬ (p → q) ≡ p∧ ¬ q$$
$$p → q ∧ p → r ≡ p → q ∧ r$$
$$p → r ∧ q → r ≡ p ∨ q → r$$
$$p → q ∨ p → r ≡ p → q ∨ r$$
$$p → r ∨ q → r ≡ p ∧ q → r$$

### BI-CONDITIONAL EQUIVALENCES

$$p ↔ q ≡ p → q ∧ q → p$$
$$p ↔ q ≡ ¬ p ↔ ¬ q$$
$$p ↔ q ≡ (p ∧ q) ∨ (¬ p ∧ ¬ q)$$
$$¬ (p ↔ q) ≡ p ↔ ¬ q$$

---

Examples of equivalence :

$p → q ≡ ¬ q → ¬ p$

1. $p → q ≡ ¬ p ∨ q$ (Conditional Equivalence)
2. $¬ p ∨ q ≡ q ∨ ¬ p$ (Commutative Laws)
3. $q ∨ ¬ p ≡ ¬ (¬ q) ∨ ¬ p$ (Double Negation)
4. $¬ (¬ q) ∨ ¬ p ≡ ¬ q → ¬ p$ (Conditional Equivalence)

$p ∧ q → p ∨ q ≡ T₀$

1. $p ∧ q → p ∨ q ≡ ¬ (p ∧ q) ∨ (p ∨ q)$ (Conditional Equivalence)
2. $¬ (p ∧ q) ∨ (p ∨ q) ≡ (¬ p ∨ ¬ q) ∨ (p ∨ q)$ (DeMorgan's)
3. $(¬ p ∨ ¬ q) ∨ (p ∨ q) ≡ (¬ p ∨ p) ∨ (¬ q ∨ q)$ (Associative)
4. $(¬ p ∨ p) ∨ (¬ q ∨ q) ≡ T₀ ∨ T₀ ≡ T₀$ (Negation/Idempotent)

$¬ ( p ∨ (¬ p ∧ q)) ≡ ¬ p ∧ ¬ q$

1. $¬ ( p ∨ (¬ p ∧ q)) ≡ ¬ p ∧ ¬ (¬ p ∧ q)$ (DeMorgan's)
2. $¬ p ∧ ¬ (¬ p ∧ q) ≡ ¬ p ∧ [¬ (¬ p) ∨ ¬ q]$ (DeMorgan's)
3. $¬ p ∧ [¬ (¬ p) ∨ ¬ q] ≡ ¬ p ∧ (p ∨ ¬ q)$ (Double Negation)
4. $¬ p ∧ (p ∨ ¬ q) ≡ (¬ p ∧ p) ∨ (¬ p ∧ ¬ q)$ (Distributive)
5. $(¬ p ∧ p) ∨ (¬ p ∧ ¬ q) ≡ F₀ ∨ (¬ p ∧ ¬ q)$ (Negation)
6. $F₀ ∨ (¬ p ∧ ¬ q) ≡ (¬ p ∧ ¬ q) ∨ F₀$ (Commutative)
7. $(¬ p ∧ ¬ q) ∨ F₀ ≡ ¬ p ∧ ¬ q$ (Identity)

---

A compound proposition is *satisfiable* if there exists truth values to its parts which make its statement true. Otherwise if no such truth values exist, it is considered *unsatisfiable*.

The assessment of truth values which satisfies a compound proposition's statement is called a *solution*.

Example : 

$$(p ∨ ¬ q) ∧ (q ∨ ¬ r) ∧ (r ∨ ¬ p)$$

Notice, the latter compound proposition is satisfiable when p ≡ q ≡ r.

Similarly, 

$$(p ∨ q ∨ r) ∧ (¬ p ∨ ¬ q ∨ ¬ r)$$

This one is true when at least one of p, q, r is true and at least one is false.

If we wish to prove $(p ∨ ¬ q) ∧ (q ∨ ¬ r) ∧ (r ∨ ¬ p) ≡ (p ∨ q ∨ r) ∧ (¬ p ∨ ¬ q ∨ ¬ r)$, 

we get a contradiction. 

$∴ (p ∨ ¬ q) ∧ (q ∨ ¬ r) ∧ (r ∨ ¬ p)$ is unsatisfiable.

 ### Applications of Satisfiability

 Sudoku example
 Sudoku is represented by 9x9 grid with 9 3x3 subgrids called *blocks*
 
 These $9 × 9 = 81$ cells are called *givens*

 Sudoku puzzles can be based on any $n² ×  n²$ grids for n ϵ $ \mathbb{Z}⁺$

To encode a sudoku puzzle, let $p(i, j, n)$ denote the proposition (true) when n is the number in the (i, j) spot in the row x column grid.

That means there exists $9 × 9 × 9 = 729$ possible propositions

First, lets construct compound propositions that assert every p contains every number, where each cell holds at most one number.

> P(row, column, 3x3 block)

Therefore, to computationally solve our sudoku puzzle, we must find the truth values for all 729 propositions for P(i, j, n) where {i, j, n ϵ [1, 2, 3,..,9]}

For each cell with a given value, we assert P(i, j, n) to be true where the cell at the (i, j) position is n.

To assert every row contains every number, logically : 

$$∧_{i = 1}^{9}∧_{n = 1}^{9}∨_{j = 1}^{9} P(i, j, n)$$

Next, to assert every column contains every number, logically :

$$∧_{j = 1}^{9}∧_{n = 1}^{9}∨_{i = 1}^{9} P(i, j, n)$$

Finally, to assert each block contains every number : 

$$∧_{r = 0}^{2}∧_{s = 0}^{2}∧_{n = 1}^{9}∨_{i = 1}^{3}∨_{j = 1}^{3} P(3r + i, 3s + j, n)$$

To assert no cell contains more than one number, we take the conjunction over all values of n, n', i, and j where :

$$\{n, n', i, j ϵ [1, 9] ∧ n ≠ n'\} P(i, j, n) → ¬ P(i, j, n')$$

## Predicate Calculus

We denote propositional functions P(x) for the proposition P.

This function takes the form of an n-tuple : P(x₁ , x₂ , ... , xₙ)

*Preconditions* - Statements that describe valid input
*Postconditions* - Conditions the output should satisfy

### Quantifiers

**Domain must be specified !**
- Universal and Existential quantifiers

Examples : 

- $z(z + 1)(z + 2)$ is divisible by 6 $∀z ϵ \mathbb{Z}$
- $q²$ is rational $∀q ϵ \mathbb{Q}$
- $r³ > 0 ∀r ϵ \mathbb{R}⁺$

The *Universal Quantification* of P(x) is the proposition : 
     
∀xP(x) =  "P(x) for all values of x in the domain"

A value for x which makes P(x) false, is called a *counter example*

What is the truth value of the Example :

$∀x(x² > x)$

1. if x is in the domain of all real numbers, then false 
2. if x is in the domain of all integers, then true


          ∀xP(x) is true when P(x) is true for every x and false otherwise.
          ∃xP(x) is true when there exists an x which makes P(x) true and false otherwise.

Be wary of the notation ∃!xP(x) for the unique existential meaning of x.

We can use quantifiers and propositional logic to express uniqueness, which in case would be accepted among more mathematicians.

$$∃!xP(x) ≡ ∃x[P(x) ∧ ∀y(P(y) → x = y)] ≡ ∃x[P(x) ∧ ∀y(x = y ∀ ¬ P(y))]$$

Example problems including the existential quantifier : 

- $(2²)^{z} + 1= $ is prime for $z ϵ \mathbb{Z} ⁺ $
- $r^s $ is rational for irrational numbers r and s.

### Quantifiers with restricted domains

An abbreviated notation is often used to restrict the domain of a quantifier

For all real numbers x, y, and z :

$$∀x<0(x^2 > 0) ≡ ∀x(x<0 → x^2 > 0)$$
$$∀y≠0(y^3 ≠ 0) ≡ ∀y(y ≠ 0 → y^3 ≠ 0)$$
$$∃z>0(z^2 = 2) ≡ ∃z(z > 0 ∧ z^2 = 2)$$

     ∀ and ∃ have higher precedence over all logical operators from propositional calculus.

---

There is a barber in Macomb who shaves everyone in Macomb that does not shave.

S(x, y) :

- x := people who shave themselves
- y := people who don't shave themselves

∴ we have a contradiction

> Check out the completeness and incompleteness theorem

Examples of *Procedural Languages* : 
- C, Java, C++

Examples of *Functional Languages* :
- (Lambda Calculus) Python
     - uses predicate logic

---

*Bound* variables have **quantifiers**, otherwise for variables not quantified, they are called *free*.

It is until **all variables are bounded**, then we have a proposition.

Example : 

$x > 0$

- $x$ := The subject (variable)
- $> 0$ := The predicate

Once x is assigned, we have a propositional function P : P(x)

In this case, P(0) = F and P(1) = T

Example :

$Q(x, y) := x = y + 3$

- Q(1, 2) = F
- Q(3, 0) = T 

$$∀x∀y ≡ ∀y∀x$$
$$∃x∃y ≡ ∃y∃x$$

**Scope**

$∀y≠0(y^3 ≠ 0) ∧ ∃x(x = 1) ≡ ∀x ≠ 0(x^3 ≠ 0) ∧ ∃x(x = 1)$

---

Every student in this class has studies calculus

- Q(x) := x has studied calculus

x ϵ All students in class

$$∀xQ(x) ≡ ∀x(x ϵ in class → Q(x))$$

If x's domain is all students at LSU?

Let y := kids not in class

$$∀x∃y(Q(x - y))$$
 
### Translating English Sentences into Logical Expressions

1. All lions are fierce
2. Some lion doesn't drink coffee
3. Some fierce creatures don't drink coffee

P(x) := "x is a lion", 
Q(x) := "x is fierce", 
R(x) := "x drinks coffee"

where the domain of x consists of all creatures

1. = $∀x(P(x) → Q(x))$
2. = $∃(P(x) ∧ ¬ R(x))$
3. = $∃x(Q(x) ∧ ¬ R(x))$

--

"If a person is a female and is a parent, then this person is someone's mother."

F(x) := "x is a female", P(x) := "x is a parent", M(x, y) := "x is a mother of y"

where the domain consists of all people.

$$∃y((F(x) ∧ P(x)) ∧ M(x, y))$$
$$∀x(F(x) ∧ P(x)) → ∃x∃y(M(x, y))$$
$$∀x(F(x) ∧ P(x)) → ∃y(M(x, y))$$
$$∀x∃y(F(x) ∧ P(x) → M(x, y))$$

> Logic programming is made up of prolog facts and prolog rules

"Every person has exactly one best friend"

B(x, y) := "y is a best friend of x"

 where the domain consists of all people.

 $$∃y(B(x, y) ∧ ∀z((z ≠ y) → ¬ B(x, y)))$$

 > 'There is a person 'y' who is best friend of 'x' and furthermore, for every peron 'z' if z is not y, then z is not allowed to be best friend of x.

 --

"There is a woman who has taken a flight on every airline in the world"

P(w, f) := "w has taken a flight f", 
Q(f, a) := "f is a flight of airline a"

where the domain consists of w, all women; f, all airplane flights; and a, all airlines;

$$∃w∀a∃f(P(w, f) ∧ Q(f, a))$$

--

"The sum of two positive integers is always positive"

$$∀x∀y((x > 0 ∧ y > 0) → (x + y) > 0)$$

--

"Every real number except 0, can find some real number such that their product is 1"

$$∀x(x≠0 → ∃ y(xy = 1))$$

--

Translate : 

$∃x∀y∀z((f(x, y) ∧ f(x, z) ∧ y ≠ z) → f(y, z))$

if f(x, y) := "x is a friend of y"

where the domain consists of all people.

> There is a person x for all types of people y and z, such that if x is a friend of y and z and y and z are different people, then y and z are friends with each other.

<div style="text-align: center"> DeMorgan's Laws on Logical Equivalences </div>

$$¬ ∀xP(x) ≡ ∃x¬P(x)$$
$$¬ ∃ xP(x) ≡ ∀x¬P(x)$$

Prove:  $¬∀x(P(x) → Q(x)) ≡ ∃x(P(x) ∧ ¬Q(x))$

1. (Converting implication) $¬∀x(P(x) → Q(x)) ≡ ¬∀x(¬P(x) ∨ Q(x))$
2. (DeMorgan's/ Double Negation) $¬∀x(¬P(x) ∨ Q(x)) ≡ ∃x(P(x) ∧ ¬Q(x))$

## Rules of Inference

- How to prove

An *argument* is a sequence of propositions (premisses) that end with a conclusion.

An argument is *valid* when all its premisses are true implies the truth of the conclusion as well.

**Valid Argument Form**

$$p → q$$
$$p    $$

<div style="text-align: center"> ---------- </div>

$$∴ q$$

| $p$ | $q$ | $p → q$ | $p → q ∧ p$ | $(p → q ∧ p) → q$ | 
| - | - | -       | - | - |
| 1 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 
| 0 | 1 | 1 | 0 | 1 |
| 0 | 0 | 1 | 0 | 1 |

Notice the tautology : $(p → q ∧ p) → q)$

This is a valid proof using truth tables.

> Note :
>
> ∃ used in english is shown with ∧ 
>    
> ∀  used in english is shown with → 


Usually, we can refer to truth tables when deciding arguments' validity.

*Rules of Inference* give us building blocks to construct more complicated argument forms

<div style="text-align: center"> LAW OF DETACHMENT / MODUS PONENS </div>

$$T₀ := (p ∧ p → q) → q$$

<div style="text-align: center"> MODUS TOLLENS</div>

$$T₀ := (¬ q ∧ p → q) → ¬ p$$

<div style="text-align: center"> HYPOTHETICAL SYLLOGISM</div>

$$T₀ := (p → q ∧ q → r) → (p → r)$$

<div style="text-align: center"> DISJUNCTIVE SYLLOGISM</div>

$$T₀ := (p ∨ q ∧ ¬ p) → q$$

<div style="text-align: center"> ADDITION</div>

$$T₀ := p → (p ∨ q)$$

<div style="text-align: center"> SIMPLIFICATION</div>

$$T₀ := (p ∧ q) → p$$

<div style="text-align: center"> CONJUNCTION</div>

$$T₀ := p ∧ q → (p ∧ q)$$
>                                        Premise := p, q; Conclusion := p ∧ q

<div style="text-align: center"> RESOLUTION </div>

$$T₀ := ((p ∨ q) ∧ (¬ p ∨ r)) → (q ∨ r)$$

<div style="text-align: center"> UNIVERSAL INSTANTIATION</div>

$$∀xP(x) → P(c) \text{ for any c}$$

<div style="text-align: center"> UNIVERSAL GENERALIZATION</div>

$$P(c) \text{ for any arbitrary c} → ∀xP(x)$$

<div style="text-align: center"> EXISTENTIAL INSTANTIATION</div>

$$∃xP(x) → P(c) \text{ for some element c}$$


<div style="text-align: center"> EXISTENTIAL GENERALIZATION</div>

$$P(c) \text{ for some element c} → ∃xP(x)$$


<div style="text-align: center"> UNIVERSAL MODUS PONENS</div>

$$∀x(P(x) → Q(x)) ∧ P(a),  \text{ where a is a particular element in the domain} → Q(a)$$

<div style="text-align: center"> UNIVERSAL MODUS TOLLENS</div>

$$∀x(P(x) → Q(x)) ∧  ¬ Q(a), \text{ where a is a particular element in the domain} → ¬P(a)$$

---
### Applying Rules of Inferences
| variable := proposition |
| - |
|$$\text{p := "It is sunny this afternoon"}$$ |
|$$\text{q := "It is colder than yesterday"}$$ |
|$$\text{r := "We will go swimming"}$$ |
|$$\text{s := "We play basketball"}$$|
|$$\text{t := "We go home early"}$$|

"It is not sunny this afternoon and it is colder than yesterday"

$$∴ ¬ p ∧ q$$

"We will go swimming, only if it is sunny"

$$∴ r → p$$

"If we don't swim, we play basketball"

$$∴ ¬ r → s$$

"If we play basketball, we go home early"

$$∴ s → t$$

All together, 

$$((¬ p ∧ q) ∧ (r → p) ∧ (¬ r → s) ∧ (s → t)) → t$$

**Proof**

1. (Simplification) ¬ p ∧ q ≡ ¬ p

$$((¬ p) ∧ (r → p) ∧ (¬ r → s) ∧ (s → t)) → t$$

2. (Modus Tollens) ¬ p ∧ r → p ≡ ¬ r

$$(¬ r ∧ (¬ r → s) ∧ (s → t)) → t$$

3. (Modus Ponens) ¬ r ∧ (¬ r → s) ≡ s

$$((s) ∧ (s → t)) → t$$

4. (Modus Ponens) s ∧ s → t ≡ t

$$∴ \text{ t }$$

--

| variable := proposition |
| - |
|$$\text{p := "You send me an email"}$$ |
|$$\text{q := "I finish my program"}$$ |
|$$\text{r := "I go to sleep early"}$$ |
|$$\text{s := "Wake up refreshed"}$$|

1. If you send me an email, then I will finish my program. 

$$p → q$$

2. If you do not send me an email, then I will go to sleep early.

$$¬ p → r$$

3. If I go to sleep early, I wake up refreshed.

$$r → s$$

All together,

$$((p → q) ∧ (¬ p → r) ∧ (r → s)) → (¬ q → s)$$

**Proof**

1. (Using Contrapositive) p → q ≡ ¬ q → ¬ p

$$((¬ q → ¬ p) ∧ (¬ p → r) ∧ (r → s)) → (¬ q → s)$$

2. (Hypothetical Syllogism) (¬ q → ¬ p) ∧ (¬ p → r) ≡ ¬ q → r

$$(¬ q → r ∧ (r → s)) → (¬ q → s)$$

3. (Hypothetical Syllogism) ¬ q → r ∧ r → s ≡ ¬ q → s

$$∴ ¬ q → s$$

--

| Propositional Functions |
| - | 
|$C(x) := \text{"x is a student in this class"}$ |
|$B(x) := \text{"x has read the book"}$|
|$P(x) := \text{"x passed the first exam"}$|

1. A student in this class has not read the book.

$$∃x(C(x) ∧ ¬B(x))$$

2. Everyone in this class passed the first exam.

$$∀x(C(x) → P(x))$$

We conclude :

$$∴ ∃x(P(x) ∧ ¬ B(x))$$

**Proof**

1. (Existential Instantiation) 

$∃x(C(x) ∧ ¬ B(x)) ≡ C(a) ∧ ¬ B(a)$

2. (Simplification) 

$C(a) ∧ ¬ B(a) → C(a)$

3. (Universal Instantiation)

$∀x(C(x) → P(x)) ≡ C(a) → P(a)$

4. (Modus Ponens) 

$C(a) ∧ (C(a) → P(a)) ≡ P(a)$

5. (Simplification) 

$C(a) ∧ ¬ B(a) ≡ ¬ B(a)$

6. (Conjunction)

$P(a) ∧ ¬ B(a)$

7. (Existential Generalization)

$∃x(P(x) ∧ ¬ B(x))$

----

# Intro to Proofs 
### Definition :

For all integers n,

$$\text{n is even if there exists integer k : n = 2k}$$
$$\text{n is odd if there exists integer k : n = 2k + 1}$$

*Parity* is described by the value of even or odd.

--

"If n is an odd integer then $n^2$ is odd"

$$∀nP(n → Q(n))$$

$P(n) := \text{"n is odd integer"}$

$Q(n) := \text{"n² is odd"}$

1. Assume P(n) to be true.

 - It follows from the definition, $n = 2k + 1$

2. To prove $n^2$ is odd

 - $n^2 = (2k + 1)^2$
 - $n^2 = 4k^2 = 4k + 1$
 - $n^2 = 2(2k^2 + 2k) + 1$
 - Let $L = 2k^2 + 2k$
 - $n^2 = 2L + 1$

 $∴ n^2 $ is odd by *direct proof*.

--

"If m and n are both perfect squares, then nm is also a perfect square"

**Definition** :

     A *Perfect square* is defined when there exists a b, such that $a = b^2$

1. Assume the premise is true.

- m and n are perfect squares.

$$∴ \text{by definition, we have integers s and t : } s^2 = m, t^2 = n$$

⋆ The goal is to prove mn is perfect square.

$$⟹ mn = s^2t^2 = (st)^2 = (ss)(tt) = (st)(st)$$

$$∴ \text{ mn is a perfect square}$$

## Proof by Contraposition

*Indirect Proofs* are proofs where we don't have premisses to start, and we have a conclusion.

* Idea : $p → q$ is true by proving $¬ q → ¬ p$

Example:

Prove if n is an integer and 3n + 2 is odd, then n is also odd.

1. First, we assume 3n + 2 is odd

$$⟹ 3n + 2 = 2k + 1 \text{ for k ϵ } \Z$$

We cannot conclude whether n is odd. So this attempt at direct proof is not valid.

1. To prove by **Contraposition** : First, we assume the conclusion is false.

$$⟹ n \text{ is even}$$

$$\text{By definition, } n = 2k \text{ for k ϵ }\Z$$

$$3n + 2 = 3(2k) + 2 = 6k + 2 = 2(3k + 1)$$

$$∵ 3n + 2\text{ is even it negates the conclusion. →  Which implies the hypothesis is true.}$$

$$∴ \text{if n is an integer and 3n + 2 is odd, then n is also odd is a true statement.}$$

Proof done by Contraposition.

--

Prove if n = ab where a and b are positive integers, then a ≤ √n or b ≤ √n

Attempt proof by contraposition : 

$$(a ≤ \sqrt{n}) ∨ (b ≤ \sqrt{n}) \text{ is false}$$

⋆ Using *Disjunction law* and *DeMorgan's law* :

$$(a > \sqrt{n}) ∧ (b > \sqrt{n})$$

> Fact : (0 < s < t) ∧ (0 < u < v) → su < tv

$$⟹ ab > \sqrt{n} \sqrt{n} = n$$

We have ab ≠ n : 

$$\text{this contradicts } ab = n $$

$$∴ \text{ The proof is true by contraposition}$$

If n = ab where a and b are positive integers, then a ≤ √n or b ≤ √n  is true.

---

In the implication : p → q we know it is always true when p is false. 

When we have this implication, if we prove p is false, we call it a *Vacuous proof*

- Vacuous proofs establish special cases

Example : 

Show P(0) is true where P(n) := "If n > 1 then n² > n" and the domain consists of all integers.

$$P(0) := (0 > 1) → 0^2 > 0$$

Vacuous proof.

Note we can also prove the implication p → q is true when we can assert q is true : *Trivial Proofs*

Let P(n) := "If a and b are positive integers, with a ≥ b, then aⁿ ≥ bⁿ where the domain consists of all positive integers.

1. First, we show P(0) is true.

$$P(0) := (a ≥ b) → a^0 ≥ b^0 = 1 ≥ 1$$

Trivial Proof.

**Definition :** The real number r is rational if there exists integers p and q with q ≠ 0 such that r = p/q. Otherwise, it is considered irrational.

Prove that the sum of two rational numbers is rational

1. Direct Proof Attempt : first, suppose we have rational numbers r and s.

$$\text{By definition, } r = \frac{p}{q}, s = \frac{t}{u}$$

where p, q, t, and u are integers and q ≠ 0 ≠ u

* Goal is to show r + s is rational

$$\frac{p}{q} + \frac{t}{u} = \frac{pu + qt}{qu} : qu ≠ 0$$

$$∴ r + s \text{ is rational}$$

Direct proof.

The sum of two rational numbers is rational is a true statement.

-- 

Prove if n is an integer and n² is odd then n is odd

1. Direct proof attempt : 

- Suppose n is an integer and n² is odd

$$⟹ n^2 = 2k + 1 \text{ for some integer k }$$

Since this is invalid, we try *proof by contraposition*,

1. Assume n is not odd 

$$⟹ n = 2k \text{ for some integer k }$$

$$n^2 = 4k^2 = 2(2k^2) = 2L \text{ where } L = 2k^2$$

Proof by contraposition.

If n is an integer and n² is odd then n must be odd.

## Proofs by Contradiction

We can show p is true for the implication p → q if the negation of p implies a contradiction.

Example : 

Show at least four of any 22 days must fall on the same day of the week.

1. Assume ¬ p is true.

$$⟹ \text{At most } 3/22 \text{ days fall on the same day of the week}$$

Knowing there are 7 days in a week, there are 21 possible days to be chosen.
So at most 3 of each chosen day could contradict a day of the week.
This contradicts the premise of having 22 days.

Therefore, after negating the premise, we found a contradiction.

Proof by contradiction.

At least four of any 22 days must fall on the same day of the week is true.

--

Prove $\sqrt{2}$ is irrational with proof by contradiction

1. Assume ¬ p is true. $\sqrt{2}$ is rational

⋆ The goal is to prove this truth implies a contradiction.

$$\text{By definition, } \sqrt{2} = \frac{a}{b} \text{ where a and b are integers and } b ≠ 0$$

It must be said also that a and b have no common factors so that it is in lowest terms.

$$\text{We have, } 2 = \frac{a^2}{b^2}$$

$$2b^2 = a^2$$

By definition of even integers, it follows that $a^2$ is even.

This allows us to use another Fact :

$$(a^2 \text{ is even}) → (a \text{ is even})$$

$$∴ a = 2c \text{ for some integer c}$$

$$⟹ 2b^2 = 4c^2$$

$$b^2 = 2c^2$$

Therefore we can prove both $b^2$ and $b$ to be even without loss of generalization.

This proof gives us a contradiction of the fact rational numbers can be expressed by non-deducible ratios, since a and b are even.

---

To recall, when we prove an implication p → q by contraposition :

1. First, we assume ¬ q is true. 
2. Then, show ¬ p is true.

To prove the implication p → q by contradiction :

1. First, assume both p and ¬ q are true.
2. Then, using the steps from ¬ q → ¬ p, show ¬ p is true

- This gives us the contradiction p ∧ ¬ p ≡ F₀ 

> All proofs by contraposition can be rewritten as proofs by contradiction.

Proof by contradiction example :

"If 3n + 2 is odd then n is odd"

1. Let p := "3n + 2 is odd" and q := "n is odd"

- Assume both p ∧ ¬ q are true 

$$(3n + 2 \text{ is odd}) ∧ (\text{n is even})$$

$$n = 2k \text{ for some integer k}$$

$$⟹ 3n + 2 = 3(2k) + 2 = 2(3k + 1)$$

$$\text{Let } t = 3k + 1$$ 

$$∴ 3n + 2 = 2t $$

We have 3n + 2 is even and 3n + 2 is odd.

Proof by contradiction.

Therefore if 3n + 2 is odd the n is also odd is a true statement.

---

## Proofs of Equivalence

The Bi-Conditional Statement

To prove p ↔ q is true :

1. Show p → q ∧ q → p is true

Example :

"If n is an integer, then n is odd if and only if $n^2$ is odd"

Let p := "n is odd" and q := "$n^2$ is odd"

1. Show p → q ∧ q → p

Proof by equivalence.

If we have 3 propositions, p, q, and r; We can prove them all equivalent if

$$p → r ∧ r → q ∧ q →  p$$

Example :

For all integers n, show the following statements to be equivalent :

| Propositions |
| - |
| $p := \text{"n is even"}$|
|$q := \text{"n - 1 is odd"}$|
|$r := "n^2 \text{ is even"}$|

1. Show p → q by Direct proof.

- Suppose p is true (n is even)

$$n = 2k \text{ for some integer k}$$

Consequently, 

$$n - 1 = 2k - 1 = 2(k - 1) + 1 = 2m + 1$$

Therefore n - 1 is odd.

Direct proof.

p → q is true.

2. Show q → r by Direct proof.

- Suppose q is true (n - 1 is odd)

$$⟹ n - 1 = 2k + 1 \text{ for some integer k}$$

$$n = 2k + 2$$

$$⟹ n^2 = (2k + 2)^2 = 4k^2 + 8k + 4 = 2(2k^2 + 4k + 2)$$

$$∴ p ↔ q ↔ r$$

Proof by equivalence.

--

To show ∀xP(x) is false, we simply need a *Counter example*

Example :

Show "Every positive integer is the sum of the squares of two integers" is false

1. Start search for counter example.

 - Looking for a particular integer not the sum of two squares

> The only perfect squares Not exceeding 3 : 0² = 0 and 1² = 1

Since there is no way to get the sum of 3 from numbers 0 and 1, our proposition is false.

Proof by counter example.

"Theorem := If n² is positive, then n is positive"

Let P(n) := "n is positive" and Q(n) := "n² is positive"

The statement ∀n(P(n) → Q(n)) cannot conclude P(n) by any valid rules of inference.

This is an example of *Fallacy of affirming the conclusion*

By counter example, this theorem can be proven false n = -1 and n² = 1


"Theorem" := If n is not positive then n² is not positive

This is the contrapositive of the ladder example.

p → q ≡ ¬ q → ¬ p

*Fallacy of circular reasoning* 

Be wary also, of *Fallacy of denying the hypothesis*

Many incorrect arguments come from the fallacy of *Begging the question*.

This happens when at least one step(s) of the proof are dependant on the truth of the statement being true.

---

### Terms

**Axioms** : statements we assume to be true

**Lemma** : proofs that solve a portion of a larger proof

**Corollary** : Theorem that is based on a prior proof

**Conjecture** : Statement that is being proposed to be true, usually on the basis of some partial evidence, heuristic argument, or intuition of expert. (When proved, they become theorems)

In proofs, axioms are the premisses.

Recap Proofs :

---

### Direct Proofs :

$$p → q$$

1. Assume p is true

- Using axioms, definitions, and previously proved theorems

2. Show q is also true

⋆ Here, we target the case where p is true and q is false never occurs.

Therefore p → q is always true.

Example:

Show if n is an odd integer, then $n^2$ is odd.

Let p be any number

Assume the proposition : Odd()

$$Odd(P) = ∃k(P = 2k + 1) \text{ for some integer k}$$

$$⟹ p^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(k^2 + 2k) + 1$$

$$\text{ Let } L = k^2 + 2k$$

$$p^2 = 2L + 1$$

∴ $p^2$ is odd

Example :

Show if m and n are both square numbers, then mn is also a square number

1. Assume m and n are both squares.

$$m = u^2 \text{ and }n = v^2$$

where u and v are integers.

Assume the proposition : Sq()

$$Sq(m) ≡ ∃u(m = u^2) ∧ Sq(n) ≡ ∃v(n = v^2)$$

Notice this statement is bi-conditional

$$mn = u^2v^2 = (uv)^2 = z^2$$

$$Sq(mn) ≡ ∃z(mn = z^2)$$

### Methods of Proving

**Proof by Contraposition**

p → q ≡ ¬ q → ¬ p

1. Assume ¬ q is true
2. Show ¬ p is also true

Example :

If n = ab where a and b are positive integers, then $a ≤ \sqrt{n} ∨ b ≤ \sqrt{n}$

$$∃a∃b(a > 0 ∧ b > 0) → n = ab$$

From DeMorgan's/Negation laws :

$$a > \sqrt{n} ∧ b > \sqrt{n}$$

$$⟹ ab > n ∴ n = ab \text{ is false}$$

Proof by contrapositive.

Proof by Contraposition :

- Assume $a > \sqrt{n} ∧ b > \sqrt{n}$

$$∴ ab > n ⟹ n ≠ ab$$

Since the negation of the conclusion implies the negation of the hypothesis, the original implication is true.

Example of Proof by Contraposition :

Show that if 3n + 2 is an odd integer, then n is odd

1. Assume n is even

$$n = 2k \text{ for some integer k}$$

$$⟹ 3n + 2 = 3(2k) + 2 = 2(3k + 1)$$

Since 3n + 2 is even when we assumed a to be even, that means if 3n + 2 were odd, then n would be odd also.

Proof by Contradiction :

$$¬ p → r ∧ ¬ r ≡ ¬ p → F₀ ≡ p$$

1. Assume ¬ p is true
2. Show for some proposition r :  $r ∧ ¬ r$ is true

Example :

Show if 3n + 2 is an odd integer, then n is odd.

Proof using contradiction :

1. Assume n is even

$$n = 2k \text{ for some integer k}$$

$$3(2k) + 2 = 2(3k + 1)$$

Since this factor is a multiple of 2, it is even.

We have a contradiction, therefore if 3n + 2 is an odd integer then n is always odd

Example :

Show $\sqrt{2}$ is irrational

Proof by Contradiction

1. Assume $\sqrt{2}$ is rational

 $$\sqrt{2} = \frac{a}{b} \text{ for some } a > 0, b > 0, b ≠ 0$$

 Futhermore, we must restrict a and b to have no common factors.

It follows that $a^2 = 2b^2$ where a is even.

Let $a = 2c$ for some integer c

$$(2c)^2 = 2b^2$$

Notice b is even here

Therefore we have that a/b is deducible, violating the definition for a rational number.

$$∴ \sqrt{2} \text{ is irrational }$$

Proof by Cases :

$$(p_1 ∨ p_2 ∨ ... ∨ p_k) → q ≡ p_1 → q ∧ p_2 → q ∧ ... ∧ p_k → q$$

⋆ Sometimes, to prove the implication p → q true, it can be easier using the equivalent disjunction for the premise.

Example :

If an integer n is not divisible by 3, then $n^2 = 3k + 1$f or some integer k

Proof by Cases :

|Propositions|
|-|
|$p := \text{"n is not divisible by 3"}$|
|$q := "n = 3m + 1 \text{ for some integer m"}$|
|$r := "n = 3m+  2 \text{ for some integer m"}$|

$$∴ p ≡ q ∧ p ≡ r$$

1. First Case :

$$n^2 = (3m + 1)^2 = 9m^2 + 6m + 1 = 3(3m^2 + 2m) + 1$$

$$∴ n^2 = 3k + 1 \text{ for some integer k}$$

2. Second Case :

$$n^2 = (3m + 2)^2 = 9m^2 + 12m + 4 = 3(3m^2 + 4m + 1) + 1$$

$$∴ n^2 = 3k + 1 \text{ for some integer k}$$

Since we obtain the desired conclusion for both cases of the hypothesis, our original statement is true.

If an integer n is not divisible by 3, then $n^2 = 3k + 1$ for some integer k is a true statement.

## Bi-Conditional Proving

"Everything implies everything"

$$p ↔ q ≡ p → q ∧ q → p$$

⋆ We need a circle of implication

Example: 

Show the following statements about the integer n are equivalent

| Propositions |
|-|
|$p := n \text{ is even}$|
|$q := n - 1\text{ is odd}$|
|$r := n^2 \text{ is even}$|

We have :

$$p → q ∧ q → r ∧ r → p$$

$$∴ p ↔ q ↔ r$$

1. Direct proof : p → q

Assert p is true

$$⟹ n = 2k \text{ for some integer k}$$

$$⟹ n - 1 = 2k - 1 = 2(k - 1) + 1$$

$$\text{ Let } m = k - 1 ⟹ n - 1 = 2m + 1$$

$$∴ \text{q is true}$$

2. Direct Proof : q → r

Assert q is true

$$⟹ n - 1 = 2k + 1 \text{ for some integer k}$$

$$n = 2k + 2$$

$$⟹ n^2 = (2k + 2)^2 = 4k^2 + 8k + 4 = 2(2k^2 + 4k + 2)$$

$$∴ \text{r is true}$$

3. Direct Proof of Proof by Contraposition : r → p

"If $n$ is odd then $n^2$ is odd"

$$∀n P(n → Q(n))$$

First step is to assert P(n) to be true.

By definition for odd numbers :

$$n = 2k + 1 \text{ for some integer k}$$

$$⟹ n^2 = (2k + 1)^2 = 2(2k^2 + 2k) + 1$$

### Existence Proof

$$∃xP(x)$$

When we find x that makes P(x) true, we call that x, *a witness*

When we find a witness, our proof becomes constructive.
Otherwise the proof is non-constructive.

Example :

Show there is a positive integer that can be written as the sum of cubes of positive integers in two different ways.

> The Hardy - Ramanujan number = 1729

$$1729 = 1^3 + 12^3 = 9^3 + 10^3$$

--

Show that there are irrational numbers r and s such that $r^s$ is irrational

Consider : $(\sqrt{2}^{\sqrt{2}})^{\sqrt{2}}  $

Existence Proof :

1. First case :

$$r^s \text{ is rational }$$

2. Second case :

$$r^s \text{ is irrational}$$

Note : $\text{(irrational)}^{\sqrt{2}}$ is always rational.

---

⋆ Remember base cases!

In *Proof by cases* we need to ensure the cases are exhaustive.

## Proof Strategies

Showing $\sqrt{3}$ is irrational : 

- Recall similar theorems, and see if we can adapt the previous theorem to the new case.

Proof : 

Any rational number, p can be written :

$$p = \frac{a}{b} \text{ where a and b are both multiples of 3}$$

It follows :

$$p ≠ \frac{a}{b}$$

--

Sometimes, it may be difficult to prove q directly (implication)

⋆ p → q

- If we can prove p in the implication : p → q, then by modus ponens, q is going to be true.

This strategy is called *Backward Reasoning*

Example :

Show that for distinct positive real numbers x and y, $\frac{1}{2}(x + y) > \sqrt{xy}$

1. 

$$\frac{1}{4}(x + y)^2 > xy → \frac{1}{2}(x + y) > \sqrt{xy}$$

2. 

$$(x + y)^2 > 4xy → \frac{1}{4}(x + y)^2 > xy$$

3. 

$$x^2 + 2xy + y^2 > 4xy → (x + y)^2 > 4xy$$

4. 

$$x^2 - 2xy + y^2 > 0 → x^2 + 2xy + y^2 > 4xy$$

5. 

$$(x - y)^2 > 0 → x^2 - 2xy + y^2 > 0$$

6. 

$$(x - y)^2 > 0 \text{ is always true}$$

Therefore, since x and y are distinct, 

$$\frac{1}{2}(x + y) > \sqrt{xy} \text{ is always true}$$

--

*Exhaustive proofs* are prove all possibilities to a particular theorem.

Example :

Prove $(n + 1)^3 ≥ 3^n$ if n is a positive integer with $n ≤ 4$

Proof by exhaustion : 

Since we only have 4 possible cases that apply to this theorem, we can perform proof by exhaustion : 

$$n = 1 : (2)^3 ≥ 3^1 ⟹ 8 ≥ 3 $$

$$n = 2 : (3)^3 ≥ 3^2 ⟹ 27 ≥ 9 $$

$$n = 3 : (4)^3 ≥ 3^3 ⟹ 64 ≥ 27 $$

$$n = 4 : (5)^3 ≥ 3^4 ⟹ 125 ≥ 81 $$

Proof is true.

--

Prove only consecutive positive integers not exceeding 100 that are perfect powers are 8 and 9.

> Definition : a number is considered a perfect power if it can be written equal to nᵃ where a is an integer greater than 1.

Proof by Exhaustion : 

The squares of positive integers not exceeding 100 are : 

$1, 4, 9, 16, 25, 36, 49, 64, 81, 100$

The cubes :

$1, 8, 27, 64$

The fourth powers : 

$1, 16, 81$

The fifth powers : 

$1, 32$

The sixth powers : 

$1, 64$

And past the sixth power, there are no other numbers other than 1 that are under 100.

We can conclude that n = 8 is the only perfect power n, for which n + 1 is also a perfect power

That is : $2^3 = 8$ and $3^2 = 9$ are the only two consecutive perfect powers not exceeding 100.

--

Proof by cases example :

Prove if n is an integer, then $n^2 ≥ n$

1. n = 0 ⟹ $0^2 ≥ 0$ True

2. n ≥ 1 ⟹ $n × n ≥ n$ True

3. n ≤ -1 ⟹ $n^2 ≥ 0$ True

--

Formulate a conjecture about the final decimal digit of the square of an integer.

Proof by cases :

Take the set of squares : {1, 4, 9, 14, 25, 36, 49, 64, ....}

Notice how as the numbers increase, the final digit never contains a 2, 3, 7, or 8

We conjecture this theorem : 

$$\text{"The final decimal digit of every perfect square is} 0, 1, 4, 5, 6, \text{ or } 9"$$

> We can write n as 10a + b where a ≥ 0 and b ≥ 0
> 
> b can be any integer from 0 to 9

$$n = 10a + b$$

$$⟹ n^2 = (10a + b)^2 = 100a^2 + 20ab + b^2 = 10(10a^2 + 2b) + b^2$$

We can infer that the final decimal digit of $n^2$ is the final decimal digit of $b^2$, which is $(10 - b)^2 = 100 - 20b + b^2$

We can have a total of 6 cases : 

Let F(n) := the final digit of n

1. First case : 

$$(F(n) = 1 ∨ F(n) = 9) → (F(n^2) = 1 ∨ F(n^2) = 81) \text{ for n = 1, 9}$$

2. Second case : 

$$(F(n) = 2 ∨ F(n) = 8) → (F(n^2) = 4∨ F(n^2) = 64)\text{ for n = 2, 8}$$

3. Third case : 

$$(F(n) = 3 ∨ F(n) = 7) → (F(n^2) = 9 ∨ F(n^2) = 49)text{ for n = 3, 7}$$

4. Fourth case :

$$(F(n) = 4 ∨ F(n) = 6) → (F(n^2) = 16 ∨ F(n^2) = 36)\text{ for n = 4, 6}$$

5. Fifth case : 

$$F(n) = 5 → F(n^2) = 25\text{ for n = 5}$$

6. Sixth case : 

$$F(n) = 0 → F(n^2) = 0\text{ for n = 0}$$

Therefore, it is proven, the final decimal digit of $n^2$ where n is an integer is always either 0, 1, 2, 4, 5, 6, or 9

--

Show there are no solutions in integers x and y for $x^2 + 3y^2 = 8$

⋆ We can reduce the work needed to prove the statement, by checking *special cases*

$$[(|x| ≥ 3) → (x^2 > 8)] ∧ [(|y| ≥ 2) → (3y^2 > 8)]$$

This leaves possibilities for x to be : $\{-2, -1, 0, 1, 2\}$
and possibilities for y to be : $\{-1, 0, 1\}$

Exhaustive Proof : 

- Our possible values for $x^2$ are 0, 1, and 4

- Our possible values for $3y^2$ are 0 and 3

Using these numbers, or max possible sum (using 3 + 4) is 7.

Therefore it is impossible for $x^2 + 3y^2 = 8$ to hold when x and y are integers.

--

Show if x and y are integers and both xy and x + y are even, then both x and y are even.

Proof by Contraposition : 

Proof by cases : 

1. Suppose x ∨ y is even 

Without *loss of generality* we assume x is odd

$$⟹ x = 2m + 1 \text{ for some integer k}$$ 

2. We show xy is odd ∨ x + y is odd

- Two cases 

i.) y is even ⟹ y = 2n
ii.) y is odd ⟹ y = 2n + 1

We have :

$$(x + y) = (2m + 1) + 2n = 2(m + n) + 1$$

$$∴ (x + y) \text{ is odd}$$

$$xy = (2m + 1)(2n + 1) = 4mn + 2m + 2n + 1 = 2(2mn + m + n) + 1$$

$$∴ xy \text{ is odd }$$

> We use loss of generality here because x and y could be interchanged.

--

Show it is true that every positive integer is the sum of 18 fourth powers of integers.

⋆ The fourth powers of integers are 0, 1, 16, 81, ... 

If we select 18 terms from these numbers that add up to n, then we have n as the sum of 18 fourth powers.

However, it is not true that every positive integer is the sum of 18 fourth powers. 

By counter example : 

79 is not the sum of 18 fourth powers.

> Fact : All possible integers up to 78 can be written as a sum of 18 fourth powers. 

Uniqueness Proofs : 

Some theorems assert the existence of a unique element with a particular property.

*Existence* := We show element x with desired property exists

*Uniqueness* := We show if y ≠ x → y doesn't have the desired property

Equivalently, if x and y both have the desired property we can show x = y.

To show uniqueness :

$$∃!xP(x) ≡ ∃x(P(x) ∧ ∀y(y ≠ x → ¬ P(y)))$$

Example : 

Show if a and b are real numbers and a ≠ 0, then there is a unique real number r such that ar + b = 0

Uniqueness Proof : 

The real number $r=  -\frac{b}{a}$ is a solution to $ar + b = 0$ 

$$∵ a(-\frac{b}{a}) + b = -b + b = 0$$

Consequently, there exists a real number r for which ar + b = 0

Now, suppose s is a real number such that as + b = 0

$$ar + b = as + b$$

where $r = -\frac{b}{a}$

$$ar = as$$

Given that a ≠ 0 

$$r = s$$

Therefore : 

$$(s ≠ r) → (as + b ≠ 0)$$

--

Given two positive real numbers x and y, their *arithmetic mean* is $\frac{(x + y)}{2}$ and their *geometric mean* is $\sqrt{xy}$

Can we prove that the arithmetic mean is greater than the geometric mean?

Backward Reasoning : 

$$\frac{(x + y)}{2} > \sqrt{xy}$$

$$\frac{(x + y)^2}{4} > xy$$

$$(x + y)^2 > 4xy$$

$$x^2 + 2xy + y^2 > 4xy$$

$$x^2 - 2xy + y^2 > 0$$

$$(x - y)^2 > 0 \text{ for } x ≠ y$$

Suppose now the proof using frontward reasoning : 

$$(x - y)^2 > 0$$

$$x^2 - 2xy + y^2 > 0$$

$$x^2 + 2xy + y^2 > 4xy$$

$$(x + y)^2 > 4xy$$

$$\frac{(x + y)^2}{4} > xy$$

$$\frac{(x + y)}{2} > \sqrt{xy}$$

Therefore it is true that the arithmetic mean is greater than the geometric mean

--
## Open Problems 

Fermat's Last Theorem : 

$$x^n + y^n = z^n$$

This equation has no solutions in integers x, y, and z with xyz ≠ 0 whenever n is an integer with n > 2

The infinitely many solutions are called *pythagorean triples* and they correspond to lengths of right triangles.

--

The 3x + 1 Conjecture : 

Let T be the transformation that sends an even integer x to x/2 and an odd integer x to 3x + 1

By continuously applying this conjecture, we should always arrive back at 1 (using positive integers)