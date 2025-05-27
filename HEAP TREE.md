# Experiment 15E: Heap Tree

## Aim
To write a Python program to build a heap tree using appropriate Python package and function.

---

## Algorithm

1. Start the program.
2. Import the `heapq` module.
3. Define a function `heaptree()` that takes a list `H` as input.
4. Use `heapq.heapify(H)` to convert the list into a valid heap (min-heap).
5. Print the created heap.
6. End the program.

---

## Program
class Node:

    def __init__(self, val, left=None, right=None):
    
        self.val = val
        
        self.left = left
        
        self.right = right
        

def isLeaf(node):

    return node.left is None and node.right is None

def process(op, x, y):

    if op == '+':
        return x + y
    if op == '-':
        return x - y
    if op == '*':
        return x * y
    if op == '/':
        return x / y

def evaluate(root):

    if root is None:
        return 0
    if isLeaf(root):
        return float(root.val)
    x = evaluate(root.left)
    y = evaluate(root.right)
    return (process(root.val, x, y))

root = Node('+')

root.left = Node('*')

root.right = Node(3)

root.left.left = Node(4)

root.left.right = Node(8)


print('The value of the expression tree is', evaluate(root))


## OUTPUT
![image](https://github.com/user-attachments/assets/65269e1c-9b7a-4380-91ea-8052e5c42664)

## RESULT
Thus, the expression tree is constructed and evaluated successfully using recursion.
