# Classwork Session 2

1. Use strong induction to prove that $\sqrt{2}$ is irrational

Our first step is to prove P(n), assuming P(k) is true for all k < n

$$∀n(\sqrt{2} ≠ \frac{n}{b}) \text{ where b is a positive integer } ≠ 0$$

Base case :

$n = 1$

$$\frac{1}{b} ≤ 1 < \sqrt{2}$$

$$∴ \frac{1}{b} ≠ \sqrt{2}$$

Induction Hypothesis : 

$$∀(k < n)(\sqrt{2} = \frac{k}{b})$$

Induction step : (using proof by contradiction)

$$\text{ Let } \sqrt{2} = \frac{n}{b}$$

$$⟹ n^2 = 2b^2$$

We can assert that $n^2$ is even since it is a factor of 2.

Given the fact : ($n^2$ is odd) → ($n$ is odd)

We can assert n to be even as well.

$$\text{ Let } n = 2t \text{ for some integer t}$$

$$⟹ (2t)^2 = 2b^2$$

$$2t^2 = b^2$$

Here we can see that b is even since, $b^2$ is a factor of two, and that means b must be even.

$$\text{ Let } b = 2s$$

$$⟹ \sqrt{2} = \frac{2t}{2s}$$

$$\sqrt{2} = \frac{t}{s} \text{ where } t < n$$

Since, the ratio $\frac{t}{s}$ has proven to be deducible, it does not qualify as a rational number. Therefore the proof by contradiction :

$$∴ \sqrt{2} \text{ is irrational }$$

---


2. From a deck of 52 replaceable cards, in how many ways can 10 cards be drawn so that the 10th card is the first repetition?


| | | | | | | | | | |
|- |- |- |- |- |- |- |- |- |- |

To divide the problem into subproblems :

First, if we find the number of ways to rearrange 9 chosen cards :

$$P(52, 9) = \frac{52!}{43!} $$

Now for the 10th card, we must pick the card which is the first. There are 9 possibilities.

$$∴ 9 × P(52, 9)  $$

---

3.  How many distinct four-digit integers can we make from the digits $0, 1, 3, 3, 6$?

- Things to note : 
     - 0 cannot be the first digit
     - 3's interchanged, don't count

To pick the first number, we have 4 digits to choose from excluding 0. Since 3 occurs twice, me factor our the number of occurrences when the 3s are swapped and the number is the same.

$$⟹ \frac{4!}{2!} = 12 \text{ ways to pick the first number}$$

With three digits left to choose, we have 2 cases :

i) the number contains one of the 3's : 

$$⟹ 3! \text{ ways to pick the rest of the numbers}$$

ii) the number contains both of the 3's : 

$$⟹ 3! \text{ ways to pick from the rest of the numbers }$$

$$∴ 12 + 3 × (6 + 6) = 48 \text{ total ways.}$$

---

4. Prove by Induction : 

$$∑ _{i = 1}^{n} \frac{1}{i(i + 1)} = \frac{n}{n + 1}$$

First, we assume P(1) is true.

Next, we prove P(n + 1) is true.

$$∑ _{i = 1}^{n} \frac{1}{(i + 1)((i + 1) + 1)} = ∑ _{i = 1}^{n} \frac{1}{(i + 1)(i + 2)} $$

$$\text{It follows that } P(n + 1) = \frac{1}{1.2} + \frac{1}{2.3} + \frac{1}{3.4} + ... + \frac{1}{n(n + 1)} + \frac{1}{(n + 1)(n + 2)}$$

Adding to the sum using the previously assumed sum,

$$\frac{n}{n + 1} + \frac{1}{(n + 1)(n + 1)} = \frac{1}{n + 1}(n + \frac{1}{n + 2})$$

$$⟹ \frac{1}{n + 1}(\frac{n(n + 2)}{n + 2} + \frac{1}{n + 2})$$

$$⟹ \frac{1}{n + 1}(\frac{n(n + 2) + 1}{n + 2}) = \frac{1}{n + 1}(\frac{n^2 + 2n + 1}{n + 2})$$

$$⟹ \frac{1}{n + 1}(\frac{(n + 1)^2}{n + 2}) = \frac{n + 1}{n + 2}$$

$$∴ ∑ _{i = 1}^{n} \frac{1}{i(i + 1)} = \frac{n}{n + 1} \text{ is true. }$$

---

5.  Use strong induction to show that every positive integer n can be written as a sum of distinct powers of two, that is, as a sum of the integers $2^0 = 1$, $2^1 = 2$, $2^2 = 4$ etc. 

Inductive step : 

Two cases : 

Suppose even or odd sum.

Base case : $n = 1$ (odd)

applying induction, $n = 2(\frac{n + 1}{2})$

Therefore we can represent the sum n as a sum of powers of two. Note, the powers of two have to be distinct.

Examples : 

$$13 = 2^3 + 2^2 + 2^0$$

$$19 = 2^4 + 2^1 + 2^0$$

$$28 = 2^4 + 2^3 + 2^2$$

Base case : 

$$P(1) := 1 = 2^0 \text{ n is odd}$$

Induction Hypothesis : 

$$∀(k ≤ n)(k \text{ can be written as the sum of distinct powers of two})$$

To prove : $P(k + 1)$

Proof by cases : 

First case : 

- If k + 1 is odd then k is even.

Second case :

- If k + 1 is even then k is odd.

By taking the expansion of the integer, $\frac{k + 1}{2}$ we can multiply each term by 2 so it becomes the next power of 2.

$$∴ \text{ every integer n can be written as the sum of distinct powers of 2}$$

---

6. How many arrangements of the letters in MISSISSIPPI have no consecutive S's?

There are 11 letters in the word, Mississippi

⋆ our only requirement is that the S's cannot be touching.

$$∴ \binom{8}{4} × \frac{7!}{4!× 2!}$$

---

7.  In how many ways can the 26 letters in the English alphabet be arranged so that there are exactly seven letters between the letters A and B?

⋆ 26 letters in the alphabet

Consider 18 blocks, one of which is the block containing a, b, and the 7 chosen letters to be in between them.

This 9 letter block, leaves us with 17 letters left in the alphabet to choose from for the remaining 17 blocks.

We know that 18 objects, can be rearranged in 18! ways.

For our 9 letter block, a or b can be at the front/end so this gives us two subcases.

$$2 × (P(1, 1) × P(7, 7) × P(1, 1)) = 2 × 7!$$

Since, we have to choose the 7 letters to go in this block, knowing that a and b won't be available to choose, we have a set of size 24 to pick from.

$$⟹ \binom{24}{7} \text{ ways}$$

Applying fundamental rules of counting, this block has : 

$$2 × 7! × \binom{24}{7} \text{ ways of occurring }$$

However, note that this only accounts for the 9 letter block.

This entity makes for ONE block of the 18 which we plan to count the number of ways to rearrange.

We have that one block has : 

$$2 × 7! × \binom{24}{7} \text{ ways of occurring }$$

The number of ways to rearrange this block, and 17 more (18 total) :

$$18! × (2 × 7! × \binom{24}{7})$$
$$18! × (2 × 7! × \frac{24!}{7!× 17!}) = 2 × 18! × \frac{24!}{17!}$$

$$⟹ ∴  2 × P(24, 7) × 18!$$

---

8. A man has 10 friends. In how many ways can he go to dinner with two or more of them?

⋆ We must pick two or more

$$∴ 10 + 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 = 54 \text{ ways}$$



---

9. Three integers are selected from the integers $\{1, 2, ... , 1000\}$. In how many ways can these integers be selected such that their sum is divisible by 4?

$4n, 4n + 1, 4n + 2, 4n + 3$

$(0, 0, 0), (1, 1, 2), (0, 2, 2), (3, 3, 2)$

$$∴ \frac{250}{3} + 250^3 + 750 × (\frac{250}{2})$$

10. How many permutations of the 10 digits $\{0, 1, 2, ... , 9\}$ are there in which the first digit is greater than 1 and the last digit is less than 8?

⋆ Inclusion - Exclusion

$$10! - (2 × 9!) - (2 × 9!) + (4 × 8!)$$

11. 

- A. Show that the total number of permutations of p red balls and 0, or 1, or 2, ..., or q white balls is :


$$\frac{p!}{p!} + \frac{(p + 1)!}{p!1!} + \frac{(p + 2)!}{p!2!} + ... + \frac{(p + q)!}{p!q!}$$

-

$$\frac{p}{q} + \frac{(p + 1)!}{p!1!} + \frac{(p + 2)!}{p!2!} + ... + \frac{(p + q)!}{p!q!}$$


- B. Show that the sum is : 

$$= \frac{(p + q + 1)!}{(p + 1)!q!}$$

Suppose 