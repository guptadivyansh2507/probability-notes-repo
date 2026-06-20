## Problem

A fair die is rolled repeatedly and a running total is kept. Let p_n be the probability that the running total is ever exactly n.
Find a recurrence relation for p_n.

## My First Instinct
My first instinct was to think about all possible sequences of die rolls that could reach n.
Very quickly the number of possibilities exploded and the problem looked much more complicated than it actually was.

## What Assumption Was Missing?
I was trying to analyze the entire process at once.
The key idea was to condition on the first roll and let the rest of the process solve a smaller version of the same problem.

## Correct Model
Look only at the first roll.
* If the first roll is 1, we still need to reach n−1.
* If the first roll is 2, we still need to reach n−2.
* ...
* If the first roll is 6, we still need to reach n−6.

## Takeaway
When a probability process evolves over time, the first question should often be:
> What happens on the first step?
Many difficult-looking probability problems become simple recursive problems after conditioning on the first move.

## Real World Connection

This idea appears in random walks, Markov chains, expected value problems, option pricing. The process after the first step often looks exactly like a smaller version of the original process.
