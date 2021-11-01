## Description

You are given a tree consisting of $n$ nodes numbered from $1 \sim n$ and $n - 1$ edges. Initially, each node has a label assigned to it from $1 \sim n$, and each label from $1 \sim n$ is assigned to **exactly** one node.

You need to perform **exactly** $n - 1$ edge deletion operations. In each operation, you need to select an edge that has **not been deleted**. Then, the labels assigned to the two nodes connected by this edge are **swapped**, and this edge is deleted.

After $n - 1$ operations, all edges will be deleted. Now, the nodes are arranged according to increasing order of the labels $1 \sim n$ to obtain a sequence of nodes $P_i$. Find the **lexicographically smallest** sequence $P_i$ that can be obtained by applying the operations in an optimal order.

![](file://pic1.png)

As shown in the figure on the left, initially, the numbers $1 \sim 5$ in the blue circles are the labels of nodes ②, ①, ③, ⑤, ④ respectively. The edges are deleted in the order (1)(4)(3)(2), which changes the tree to the figure on the right. The nodes are arranged by increasing order of their labels to obtain the sequence ①③④②⑤, which is the lexicographically smallest sequence among all possible results.

## Input Format

**The input contains multiple test cases.**

The first line contains a positive integer $T$ denoting the number of test cases.

For each test case:\
The first line contains an integer $n$ denoting the number of nodes in the tree.\
The second line contains $n$ integers where the $i$-th integer ($1 \le i \le n$) denotes the node which has label $i$ initially.\
Each of the next $n - 1$ lines contains two integers $x$ and $y$ denoting there's an edge between node $x$ and node $y$.

## Output Format

For each test case, print one line containing $n$ space-separated integers denoting the lexicographically smallest sequence $P_i$ that can be obtained by applying the operations in an optimal order.

```input1
4
5
2 1 3 5 4
1 3
1 4
2 4
4 5
5
3 4 2 1 5
1 2
2 3
3 4
4 5
5
1 2 5 3 4
1 2
1 3
1 4
1 5
10
1 2 3 4 5 7 8 9 10 6
1 2
1 3
1 4
1 5
5 6
6 7
7 8
8 9
9 10
```
```output1
1 3 4 2 5
1 3 5 2 4
2 3 1 4 5
2 3 4 5 6 1 7 8 9 10
```

## Sample 2

See the additional files [tree2.in](file://tree2.in) and [tree2.ans](file://tree2.ans) for details.

## Constraints

| Tests        | $n \le$         | Special nature                        |
|:------------:|:---------------:|:-------------------------------------:|
| $1 \sim 2$   | $10$            | None                                  |
| $3 \sim 4$   | $160$           | The tree is a chain                   |
| $5 \sim 7$   | $2 \times 10^3$ | The tree is a chain                   |
| $8 \sim 9$   | $160$           | There exists a node of degree $n - 1$ |
| $10 \sim 12$ | $2 \times 10^3$ | There exists a node of degree $n - 1$ |
| $13 \sim 16$ | $160$           | None                                  |
| $17 \sim 20$ | $2 \times 10^3$ | None                                  |

For all the tests: $1 \le T \le 10$, and it is guaranteed that the given edges form a tree.
