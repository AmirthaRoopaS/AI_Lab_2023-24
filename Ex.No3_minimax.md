# Ex.No: 3  Implementation of Minimax Search
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
Write a mini-max search algorithm to find the optimal value of MAX Player from the given graph.
### Algorithm:
1. Start the program
2. import the math package
3. Specify the score value of leaf nodes and find the depth of binary tree from leaf nodes.
4. Define the minimax function
5. If maximum depth is reached then get the score value of leaf node.
6. Max player find the maximum value by calling the minmax function recursively.
7. Min player find the minimum value by calling the minmax function recursively.
8. Call the minimax function  and print the optimum value of Max player.
9. Stop the program. 

### Program:
import math
def minimax (curdepth, nodeindex, maxturn, scores, targetdepth):
    if(curdepth == targetdepth):
        return scores[nodeindex]
    if(maxturn):
        return max(minimax(curdepth + 1,nodeindex*2,False,scores,targetdepth),minimax(curdepth + + 1,nodeindex*2 + 1,False, scores, targetdepth))
    else:
        return min(minimax(curdepth + 1, nodeindex * 2, True, scores, targetdepth),minimax(curdepth + 1, nodeindex * 2 + 1, True, scores, targetdepth))
scores = [3, 5, 2, 9, 12, 5, 23, 20]
treedepth = math.log(len(scores), 2)
print("The optimal value is : ",end = " ")
print(minimax(0, 0, True, scores, treedepth))

### Output:
![image](https://github.com/AmirthaRoopaS/AI_Lab_2023-24/assets/143496311/cacdcf62-0e7e-478d-ad65-2b89465e1b5b)

### Result:
Thus the optimum value of max player was found using minimax search.
