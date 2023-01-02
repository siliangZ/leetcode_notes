# add
# delete(recursion)
1. find the node based on the value
2. check the node
    1. if node is leaf, then delete the node
    2. if node has left branch, then find the predecessor in left branch and swap the predecessor with the root and delete the predecessor in the left branch
    3. else if node has right branch, then find the successor in right branch and swap the successor with the root and delte the successor in right child
3. * pay attention to how to find predecessor and successor
# search
# update