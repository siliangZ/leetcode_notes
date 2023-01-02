# Preorder
* root -> left -> right
* use stack
* process
    1. use a stack to record the order
    2. initialize the stack with root node
    3. pop the first element of stack and record it in the result
    4. push the right child and left child into stack(right first)
    5. continue iterate


# Inorder
* left -> root -> right
* process
    1. initailze the stack with all left child of the nodes from root
    2. each iteration, check the top element of the stack 
    3. check if it has right child, if it does, add all left child
    4. if it doesn't,(the current node is done), pop up the stack and check if the popped node comes from the left branch.
    5. if it does, then continue to next iter, otherwise continue to pop until the popped node comes from the left branch of the top node


# Postorder
* left -> right -> root
* process
    1. initialize the stack with root and record the last popped element
    2. check the top of the stack
        * if last element is not None and last element is the child of the top element -> top node is finished and popped the top node and record its value and continue the iteration
        * if the top node has right child then add to stack
        * if the top node has left child then add to stack
        * if the top node has no child, then pop the top node add value to result

        summary of two scenarios
        * children of currennt node is visited or it has not child node
        * children of current node is not visited yet