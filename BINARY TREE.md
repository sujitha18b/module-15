# Experiment 15B: Binary Tree (Float Values)

## Aim
To write a Python program to build a binary tree with a root, left, and right node using float values.

---

## Algorithm

1. Start the program.
2. Import the `Node` class from the `binarytree` module.
3. Create a root node using the `Node` class and input a floating-point value for the root.
4. Create left and right child nodes for the root using floating-point values.
5. Convert the binary tree to a list.
6. Print the list of nodes.
7. End the program.

---

## Program

from binarytree import Node



l = []


for i in range(3):

    l.append(input())
    
    
root = Node(l[0])

root.left = Node(l[1])

root.right = Node(l[2])


print("Binary Tree : ")

for i in root.values:

    print(i, "--> ", end="")

## OUTPUT
![image](https://github.com/user-attachments/assets/8650cd2a-b9e9-481a-8b6b-c157f284128f)


## RESULT
Thus, the Python program to print a binary tree consisting of a root, left, and right node has been implemented and executed successfully.
