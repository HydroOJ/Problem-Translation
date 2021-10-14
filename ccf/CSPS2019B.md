## Description

In this question, we define a bracket string that meets the following requirements as a "legal bracket string":

1. `()` is a "legal bracket string".
1. If `A` is a "legal bracket string", then (A) is also a "legal bracket string".
1. If `A` and `B` are both "legal bracket strings", then `AB` is also a "legal bracket string".

The definition of **substring** and **different substring** in this question is as follows:

1. We use $S(l,r)$ ($1\le l \le r \le |S|$, which $|S|$ is the length of $S$) to represent a substring of $S$. It means a string consisting of **any** consecutive characters from $l$ to $r$ in $S$.
2. Two substrings of S are considered different if and only if their positions in S are different, (i.e. $l$ is different or $r$ is different).

Little Q has a rooted tree which rooted at node $1$ and the number of nodes is $n$. Except for node $1$, the parent node of node $u(2\le u\le n)$ is $f_u(1\le f_u <u)$.

Little Q finds that there is exactly one bracket on each node of this tree, which may be `(` or `)`. He defines $s_i$ as a string composed of brackets on the simple path from the root node to the node $i$ and arranged in sequence according to the sequence of the nodes.

Obviously $s_i$ is a bracket string , but it may not be a "legal bracket string". So now Little Q wants to find out how many **different** substrings of $s_i$ are legal bracket strings" for all $i(1\le i\le n)$.

Assuming that there are $k_i$ different substrings of $s_i$ as "legal bracket strings", you only need to tell Little Q the bitwise XOR of all $i\times k_i$, which is:
$$
(1\times k_1)\operatorname{xor}(2\times k_2)\operatorname{xor}(3\times k_3)\operatorname{xor}\cdots\operatorname{xor}(n\times k_n)
$$
Among them, $\text{xor}$ is bitwise XOR operation.

## Input Format

The first line contains an integer $n$, which represents the number of nodes in the tree.

The second line contains an bracket string of length $n$, which the $i$-th bracket represents the bracket on the $i$-th node.

The third line contains $n-1$ integer. The $i$-th integer represents the father of $(i+1)$-th node $f_{i+1}$.

## Output Format

Print one integer in a single line, which is the answer.

```input1
5
(()()
1 1 2 2
```

```output1
6
```

The shape of the tree is as follows:

![](https://hydro.ac/d/ccf/p/96/file/5dcfe9db2c334.png)

- The brackets on the simple path from the root to node $1$ are arranged in order to form a string of `(`, and the number of substrings that are "legal bracket strings" is $0$.
- The brackets on the simple path from the root to node $2$ are arranged in order to form a string of `((`, and the number of substrings that are "legal bracket strings" is $0$.
- The brackets on the simple path from the root to node $3$ are arranged in order to form a string of `()`, and the number of substrings that are "legal bracket strings" is $1$.
- The brackets on the simple path from the root to node $4$ are arranged in order to form a string of `(((`, and the number of substrings that are "legal bracket strings" is $0$.
- The brackets on the simple path from the root to node $5$ are arranged in order to form a string of `(()`, and the number of substrings that are "legal bracket strings" is $1$.

## Constraints

|      #      |     $n\le$     | Special Properties |
| :---------: | :------------: | :----------------: |
|  $1\sim 2$  |      $8$       |     $f_i=i-1$      |
|  $3\sim4$   |     $200$      |     $f_i=i-1$      |
|  $5\sim 7$  | $2\times 10^3$ |     $f_i=i-1$      |
| $8\sim 10$  | $2\times 10^3$ |        None        |
| $11\sim 14$ |     $10^5$     |     $f_i=i-1$      |
| $15\sim 16$ |     $10^5$     |        None        |
| $17\sim 20$ | $5\times 10^5$ |        None        |

