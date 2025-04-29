# Ex11 Tree Representation and Traversal
### DATE: 13/03/2025
## AIM:
To write a C function to perform post order traversal of a binary tree.

## Algorithm
1. Start the program 
2. Define a function display_postorder() that takes a pointer to the root node of the tree. 
3. Check if the current node (root_node) is not null. 
4. Recursively call display_postorder() for the left child of the current node. 
5. Recursively call display_postorder() for the right child of the current node. 
6. After visiting both children, print the value of the current node. 
7. End the program

## Program:
```
Program to perform post order traversal of a binary tree.
Developed by: SUDHIR KUMAR. R
RegisterNumber: 212223230221
```
```
/* 
struct node { 
    int value; 
    struct node *left_child, *right_child; 
};
*/
void display_postorder(struct node *root_node) { 
    if(root_node) { 
        display_postorder(root_node->left_child); 
        display_postorder(root_node->right_child);
        printf("%d\n", root_node->value); 
    } 
}
```
## Output:

![Screenshot 2025-04-29 133624](https://github.com/user-attachments/assets/0af88e31-78bc-4316-bb5a-8ac1f112c068)

## Result:
Thus, the function to perform post order traversal of a binary tree is implemented successfully
