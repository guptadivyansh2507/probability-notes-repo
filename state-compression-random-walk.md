
## Problem
Calvin and Hobbes play games until one player leads by 2 wins. Calvin wins each game independently with probability p.
Find the probability that Calvin eventually wins the match.

## My First Instinct
My first instinct was to think about all possible sequences of wins and losses.
Very quickly this became messy because the match can continue for an arbitrary number of games.

## What Assumption Was Missing?
I was tracking too much information.
The entire history of the match does not matter. The only thing that matters is the current lead.

## Correct Model
Define the state as:
Current Lead = (Calvin Wins) − (Hobbes Wins)
The match starts at state 0.
Each game:
* Move +1 with probability p.
* Move -1 with probability 1-p.
The match ends when the lead reaches:
+2 (Calvin wins)
or
-2 (Hobbes wins)
This turns the problem into a random walk with absorbing states.
Instead of tracking every possible sequence of games, I only need to track the current lead.

## Takeaway
A difficult probability process often becomes much simpler after identifying the correct state.
The entire history may be irrelevant once the current state is known.

## Real World Connection
This idea appears in:
* Gambler's ruin
* Random walks
The key skill is often finding the smallest amount of information needed to describe the process.
