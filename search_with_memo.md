# Search with memo
DFS + Memo
通过构建问题的解空间，从而把问题转化成一个DFS可以使用的场景
## Features
1. the recursive function has a return value
2. the return value is only related to the input arguments
3. the memo struct is a part of the input arguments. It records the relationship between input arguments and output. It needs all input arguments. When the input arguments are complicate, the memo is not applicable.
## O(n)
total number of states * time cost of each state  
we will check the key of memo for the total number of states
