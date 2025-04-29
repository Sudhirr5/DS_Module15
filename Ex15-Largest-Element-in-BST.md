# Ex15 Largest Element in BST
### DATE: 17/03/2025
## AIM:
To Write a c program to find the largest value in a Binary Search Tree.

## Algorithm
1. Start the program
2. Initialize a pointer to the root of the BST. 
3. Move to the right child in a loop while it exists. 
4. Stop when the right child is NULL. 
5. Return the current node’s value as the largest.
6. End the program

## Program:
```
Program to find and display the priority of the operator in the given Postfix expression
Developed by: SUDHIR KUMAR. R
RegisterNumber: 212223230221
```
```
#include <stdio.h> 
#include <stdlib.h> 

struct node { 
    int info; 
    struct node *left, *right; 
}; 
struct node *createnode(int key) { 
    struct node *newnode = (struct node*)malloc(sizeof(struct node)); 
    newnode->info = key; 
    newnode->left = NULL; 
    newnode->right = NULL; 
    return newnode; 
} 

void inorder(struct node *root) { 
    if(root != NULL) { 
        inorder(root->left); 
        printf(" %d ", root->info); 
        inorder(root->right);
    } 
} 

void largest(struct node *root) { 
    while (root != NULL && root->right != NULL) { 
        root = root->right; 
    } 
    printf("\nLargest value is %d", root->info);
}

int main() { 
    struct node *newnode = createnode(25); 
    newnode->left = createnode(17); 
    newnode->right = createnode(35); 
    newnode->left->left = createnode(13); 
    newnode->left->right = createnode(19); 
    newnode->right->left = createnode(27); 
    newnode->right->right = createnode(55); 
    printf("Inorder traversal of tree 1 :"); 
    inorder(newnode); 
    largest(newnode); 
    return 0; 
}
```
## Output:

![Screenshot 2025-04-29 135420](https://github.com/user-attachments/assets/458c7fc7-d5a8-4cc5-a8bc-e5eeadff60da)

## Result:
Thus, the C program to find the largest value in a Binary Search Tree is implemented successfully.
