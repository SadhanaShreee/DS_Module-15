# Ex15 Largest Element in BST
## DATE: 26-=03-2025
## AIM:
To Write a c program to find the largest value in a Binary Search Tree.

## Algorithm
1. Initialize a pointer to the root of the BST.
2. Move to the right child in a loop while it exists.
3. Stop when the right child is NULL.
4. Return the current node’s value as the largest.   

## Program:

```
Program to find and display the priority of the operator in the given Postfix expression
Developed by: SADHANA SHREE B 
RegisterNumber: 212223230177

#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* left;
    struct Node* right;
};


struct Node* createNode(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->left = newNode->right = NULL;
    return newNode;
}


struct Node* insert(struct Node* root, int value) {
    if (root == NULL)
        return createNode(value);
    if (value < root->data)
        root->left = insert(root->left, value);
    else
        root->right = insert(root->right, value);
    return root;
}

int findLargest(struct Node* root) {
    if (root == NULL) {
        printf("Tree is empty\n");
        return -1;
    }
    while (root->right != NULL) {
        root = root->right;
    }
    return root->data;
}

int main() {
    struct Node* root = NULL;

    // Inserting values
    root = insert(root, 50);
    root = insert(root, 30);
    root = insert(root, 70);
    root = insert(root, 60);
    root = insert(root, 80);

    int largest = findLargest(root);
    printf("Largest value in BST: %d\n", largest);

    return 0;
}

```

## Output:

![Screenshot 2025-05-18 123907](https://github.com/user-attachments/assets/6ae2656e-bc5a-4cc1-a29a-707552ec0505)


## Result:
Thus, the C program to find the largest value in a Binary Search Tree is implemented successfully.
