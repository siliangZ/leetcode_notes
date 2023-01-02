# use BFS to find all solutions
treat each solution as a point and the change between solution as the connection between points. Then find all solutions is equal to find all connected points

# serialize and deserialize the binary tree
remember to insert the empty node to keep the serialization be unique. 
We could use pre-order, in-order, post-order or level-order.

# two direction BFS
graph is represented as dict
use two queue and BFS from two ends
* it needs a start and a end