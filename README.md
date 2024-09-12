# Ex.No: 3 Implementation of Minimax Search

REGISTER NUMBER : 212222040046

# AIM:
Write a mini-max search algorithm to find the optimal value of MAX Player from the given graph.

# Algorithm:

    Start the program
    import the math package
    Specify the score value of leaf nodes and find the depth of binary tree from leaf nodes.
    Define the minimax function
    If maximum depth is reached then get the score value of leaf node.
    Max player find the maximum value by calling the minmax function recursively.
    Min player find the minimum value by calling the minmax function recursively.
    Call the minimax function and print the optimum value of Max player.
    Stop the program.

# Program:
```
import math def minimax (curDepth, nodeIndex, maxTurn, scores, targetDepth):
base case : targetDepth reached

if (curDepth == targetDepth):
    return scores[nodeIndex]
if (maxTurn):
    return max(minimax(curDepth + 1, nodeIndex * 2,
        False, scores, targetDepth),
        minimax(curDepth + 1, nodeIndex * 2 + 1,
        False, scores, targetDepth))
else:
    return min(minimax(curDepth + 1, nodeIndex * 2,
        True, scores, targetDepth),
        minimax(curDepth + 1, nodeIndex * 2 + 1,
        True, scores, targetDepth))

Driver code

scores = [3, 5, 2, 9, 12, 5, 23, 20] treeDepth = math.log(len(scores), 2) # calculate depth of node log 8 (base 2) = 3) print("The optimal value is : ", end = "") print(minimax(0, 0, True, scores, treeDepth))

```
# Output:
![276075181-08b00b76-4a81-443a-bf05-b5c144d5c48f](https://github.com/user-attachments/assets/c3b323dd-8b0d-4256-953b-0f8df57e174d)


# Result:
Thus the optimum value of max player was found using minimax search.
