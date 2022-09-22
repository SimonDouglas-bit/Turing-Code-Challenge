# Turing-Code-Challenge
Code Challenge solutions for Turing
## Problem 1
You're required to develop a game with weird rules where the scores of past rounds may affect future rounds scores. At the beginning of the game, you start with an empty record. You are given a list of strings ```ops```, where ```ops[i]``` is the ith operation you must apply to the record and is one of the following:
1. An integer ```x``` - Record a new score of x.
2. ```x```- Record a new score that is the sum of the previous two scores. It is guaranteed there will always be two previous scores.
3. ```D``` - Record a new score that is double the previous score. It is guaranteed there will always be two previous scores.
4. ```C``` Invalidate the previous score, removing it from the record. It is guaranteed there will always be a previous score.
Return *the sum of all the scores on the record.*

### Example:
```
Input: ops = ["5", "2", "C", "D", "+"]
Output: 30
Explanation:
"5" - Add 5 to the record, record is now [5].
"2" - Add 2 to the record, record is now [5, 2].
"C" - Invalidate and remove the previous score, record is now [5].
"D" - Add 2 * 5 = 10 to the record, record is now [5, 10].
"+" - Add 5 + 10 = 15 to the record, record is now [5, 10, 15].
The total sum is 5 + 10 + 15 = 30
```
### Instructions
Use the following function code snippet:
```
def calPoints(ops) -> int:
  record = []
  """
  Your code
  """
  result = None
  return result
```
## Solution in Python 3
```
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Wed Sep  7 19:06:11 2022

@author: sd
"""
record = []
ops = ["5","-2","4","C","D","+"]
x = int() #record a new score of x
#"+" record a new score, the sum of the previous 2 scores
#"D" - record a new score that is double the previous score
#"C" - remove the previous score from the record.
i  = 0

while i < len(ops):
    op = ops[i]
    print('op ' +op)
    
    if op == "D":
        index = len(record) - 1
        prev = int(record[index])
        score = prev * 2
        record.append(score)
        
    elif op == "+":
        index1 = len(record) - 1
        index2 = len(record) -2
        
        score = int(record[index1]) + int(record[index2])
        record.append(score)
                           
    elif op == "C":
        if len(record) >= 2:
            record.pop(-1)
            
    else:
        score = int(ops[i])
        record.append(score)      
        
    i = i + 1
result = 0

for i in record:
    result += i
return result
```
