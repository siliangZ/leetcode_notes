# core idea
Divide the big problem into small pieces and combine the result of small problem. It's very similar to divide and conquer. 
# Different between Divide and Conquer and Dynamic programming
Whether there is overlap in the child problem

# Two different implementation
* memory search(recursion)
* multiple loops
    * from top to bottom
    * from bottom to top


# Four Elements of DP
1. State Array: record each state in the domain
2. State Transfer function: describe how state is transfered between each other
3. Initialization: initialize the state array
4. Answer: find the answer from the state array

# Three application
1. find the maximum / minimum of something
2. the feasibility of some strategy
3. the total number of solutions, not the all solutions(different from finding the solution -> DFS)


# Categories
1. 坐标型
    1. 一维
    2. 二维
2. 前缀型
    1. 划分型
    2. 匹配型
3. 背包型
4. 区间型
5. 博弈型
6. 树型
7. 状态压缩型
It's categorized by the state and how state is represented

# axis DP
## one dimension state
dp[i] is from the start point to i, the solution(max, total solution, feasibility)
## two dimensions state
dp[i][j] is from the start point to (i, j), the solution of(max, total solutions, feaibility)

# prefix DP
## Division state
(based on the info, we select the state)
dp[i] is the solution(optima, solution, feasibility) of the first i character
dp[i][j] is solution of the first i character which is divided into j parts

## Match state
dp[i][j] is the first i character of the str1 matches the first j character of the str2

# Range DP
dp[i][j] is the solution of the range of i to j

# backpack DP
dp[i][j] is the solution(max, total, feasibility) of first i items which gives the sum of j  
**first** is a key word, remember there is a 0 prefix. So the dp will be (n + 1) * (m + 1)
**sum** is a key word here and we need to pay attention to
The solution is not related to the order of items.(set)
there could be three status kept in the DP array.
1. i: the first i items
2. j: the sum of some properties of item
3. state: another state of the items
状态层
决策层

## 01 backpack DP
if the item is selected or not. If it's selected, then it is **1** otherwise it's **0**

## minimum-partition
convert it into a backpack DP problem
sum - 2X
find the partition of array which sum closest to Sum/2
## 外卖优惠券
## 石头碰撞
The core is the minimum-partition
## backpack with value
state: 从前i个物品中挑出不超过j的体积的最大价值
It's close to the one of the implementation of 01 backpack DP.
## duplicate items 
a for loop for how many times we will select each item

## vs DFS
It depends on the relationship between n and m. if m >> 2^n, then DFS is faster than DP.
or when we could reach a solution from multiple combination, because DP reduces the space of child problem, DP is faster than DFS.

# DP Not applicable situation
1. find all solutions(the specific solution)
2. the input data is not ordered(data has no direction)
3. brute force algorithm is polynomial

# Steps to solove problem
1. determine if DP is applicable
2. determine the type of DP
3. solve the problem with four elements of DP(state, function, initialization, answer)

# Optimization
1. rolling array -> reduce the space complexity