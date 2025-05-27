# Experiment 15A: Binary Search Tree

## Aim
To write a Python program to build a Binary Search Tree (BST) using a built-in function.


## Algorithm

1. Start the program.
2. Import the `Node` class from the `binarytree` module.
3. Define a function `_build_bst_from_sorted_values()` to build a BST recursively from a sorted list.
4. Define a function `left_subtree()` to print the values in the left subtree of the BST.
5. Accept input from the user for the number of elements.
6. Read the elements into a list.
7. Sort the list.
8. Build the BST by calling `_build_bst_from_sorted_values()` with the sorted list.
9. Print the postorder traversal of the BST.
10. Print the left subtree values.
11. Check and print whether the built tree is a Binary Search Tree.
12. End the program.

---

## Program
from binarytree import Node

def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values) == 0:
        return None
    mid_index = len(sorted_values) // 2
    root = Node(sorted_values[mid_index])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right = _build_bst_from_sorted_values(sorted_values[mid_index + 1 :])  
    return root

def left_subtree(l):
    for i in l.left.values:
        print(i, "-->", end="")
    return 

a = []
size = int(input())
for i in range(0, size):
    val = int(input())
    a.append(val)
x = sorted(a)

l = _build_bst_from_sorted_values(x)
print("Postorder :", l.postorder)
print("Left Subtree :")
left_subtree(l)
print("\nIs this a Binary Search Tree? ", l.is_bst)



## OUTPUT
![image](https://github.com/user-attachments/assets/17c2e9c4-eccc-4bff-ae87-b18883355ed1)


## RESULT
Thus, the Python program to build a binary search tree using a built-in function and perform postorder traversal has been implemented and executed successfully. The left subtree was printed, and it was verified that the tree is a Binary Search Tree.
