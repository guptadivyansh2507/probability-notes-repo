A spam filter uses 100 words or phrases. For each word W_j, we know:

* P(W_j | spam) = p_j
* P(W_j | not spam) = r_j

The key assumption is that the words are conditionally independent given whether the email is spam or not.

A new email contains words 23, 64, and 65 but none of the other 97 words.

We want to compute:

P(spam | all observed words and missing words)

---

## My First Instinct

My first instinct was to focus only on the words that appeared:

W_23, W_64, W_65

and ignore the words that did not appear.

This felt natural because the words that appear seem like the evidence.

---

## What Assumption Was Missing?

The absence of a word is also evidence.

If a word appears very frequently in spam emails but does not appear in this email, that should decrease the probability that the email is spam.

The event:

W_j^c

contains information too.

The problem is not:

P(spam | W_23, W_64, W_65)

The problem is:

P(spam | W_1^c, ..., W_22^c, W_23, W_24^c, ..., W_63^c, W_64, W_65, W_66^c, ..., W_100^c)

---

## Correct Model

Using conditional independence:

P(E | spam)

=
p_23 p_64 p_65

×

(1-p_1)(1-p_2)...(1-p_22)

×

(1-p_24)...(1-p_63)

×

(1-p_66)...(1-p_100)

Similarly:

P(E | not spam)

=
r_23 r_64 r_65

×

(1-r_1)(1-r_2)...(1-r_22)

×

(1-r_24)...(1-r_63)

×

(1-r_66)...(1-r_100)

Then Bayes gives:

P(spam|E)

=
[P(E|spam)P(spam)]

/

[P(E|spam)P(spam) + P(E|not spam)P(not spam)]

---

## Main Lesson

Conditional independence turns an impossible problem into a manageable one.

Without it, we would need to estimate probabilities for roughly:

2^100

possible word combinations.

With conditional independence, we only need probabilities for individual words.

---

## Real World Connection

Many machine learning models work by introducing assumptions that are not exactly true but make the problem solvable.

The important question is often not:

"Is the assumption perfectly true?"

but

"Does the assumption produce useful predictions?"

Naive Bayes is one of the classic examples of this idea.
