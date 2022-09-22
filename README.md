# Turing-Code-Challenge
Code Challenge solutions for Turing
## Problem 1
You're required to develop a game with weird rules where the scores of past rounds may affect future rounds scores. At the beginning of the game, you start with an empty record. You are given a list of strings ```ops```, where ```ops[i]``` is the ith operation you must apply to the record and is one of the following:
1. An integer ```x``` - Record a new score of x.
2. ```+`` - Record a new score that is the sum of the previous two scores. It is guaranteed there will always be two previous scores.
3. ```D``` - Record a new score that is double the previous score. It is guaranteed there will always be two previous scores.
4. ```C``` Invalidate the previous score, removing it from the record. It is guaranteed there will always be a previous score.
Return the sum of all the scores on the record
