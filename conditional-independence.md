## Problem
You play two games against the same opponent. Does winning the first game affect the probability of winning the second?

## My First Instinct
My first instinct was that the games should be independent.
The result of Game 1 should not physically change the result of Game 2, so I thought:
P(Win Game 2 | Win Game 1) = P(Win Game 2)

## What Assumption Was Missing?
I ignored the hidden variable: the opponent's skill level.
Winning Game 1 gives information about how strong the opponent is. If I win the first game, it becomes more likely that the opponent is weaker than I initially thought.

## Correct Model
The games are not independent.
However, they are conditionally independent given the opponent's skill level.
Once the skill level is known, the outcome of Game 1 provides no additional information about Game 2.
The dependence comes entirely from uncertainty about the hidden variable.

## Takeaway
Two events can appear dependent simply because they both contain information about the same hidden cause.
Learning one event updates our belief about the hidden variable, which then changes the probability of the other event.

## Real-World Connection
This idea appears everywhere:
* Spam emails and word occurrences
* Diseases and symptoms
* Market regimes and stock returns
* Student ability and exam scores

Many apparent relationships disappear once the hidden variable is revealed.
