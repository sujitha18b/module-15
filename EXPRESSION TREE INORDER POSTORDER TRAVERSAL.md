# Experiment 15D: Expression Tree – Inorder and Postorder Traversal

## Aim
To write a Python program to build the following expression tree and print the inorder and postorder traversal.


---

## Algorithm

1. Begin the program.
2. Import the necessary modules (`build`, `Node`) from the `binarytree` package.
3. Define a list `x` representing the binary tree in pre-order format.
4. Use the `build()` function to construct the expression tree from the list.
5. Print the inorder traversal of the expression tree using `.inorder`.
6. Print the postorder traversal of the expression tree using `.postorder`.
7. End the program.

---

## Program

from binarytree import heap, Node, build.


def heaptree(l):

    t = build(l)
    
    for i in t.values:
    
        print(i, "-->", end="")
        
    print("\nHeight : ", t.height)
    
    print("Is max heap? : ", t.is_max_heap)
    
    print("Is complete tree? : ", t.is_complete)
    

heaptree([89, 81, 76, 22, 14, 9, 54, 11])


## OUTPUT
![image](https://github.com/user-attachments/assets/401dde1b-f53b-4af2-8def-0cb8f35edfd8)


## RESULT
Thus, the Python program to build a heap tree, check if it is a max-heap and a complete tree, and print its height has been implemented and executed successfully.
