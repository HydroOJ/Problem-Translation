## Description

You are given a positive integer $n$ and a sequence of integers $a_1, a_2, \cdots, a_{2n}$. The numbers $1, 2, \cdots, n$ each occur exactly twice in these $2n$ numbers. Create a sequence $b_1, b_2, \cdots, b_{2n}$ of the same length $2n$ by performing $2n$ operations. Initially, $b$ is an empty sequence. One of the following two operations can be performed at a time:

1. Add the first element of the sequence $a$ to the end of $b$ and remove it from $a$.
2. Add the last element of the sequence $a$ to the end of $b$ and remove it from $a$.

The goal is to make $b$ a **palindrome**, i.e., for all $1 \le i \le n$, $b_i = b_{2n + 1 - i}$ should be satisfied. Find whether this goal can be achieved, and if so, find the lexicographically smallest sequence of operations as described in the output format.

## Input Format

The first line contains an integer $T$ denoting the number of test cases. The first line of each test case contains a positive integer $n$ and the second line contains $2n$ space-separated integers $a_1, a_2, \cdots, a_{2n}$.

## Output Format

Print one line for each test case. If a palindrome can't be generated, print $-1$. Otherwise, print a string of length $2n$ consisting of the characters $L$ and $R$ (without spaces), where $L$ represents operation $1$ and $R$ represents operation $2$. The string should be the lexicographically smallest among the strings corresponding to all the sequences of operations that achieve the goal. A string $s_{1..2n}$ is lexicographically smaller than $t_{1..2n}$ if and only if there exists a position $1 \le k \le 2n$ such that $\forall 1 \le i < k$, $s_i = t_i$ and $s_k < t_k$.

```input1
2
5
4 1 2 4 5 3 1 2 3 5
3
3 2 1 2 1 3
```
```output1
LRRLLRRRRL
‐1
```

In the first test case, the generated sequence $b$ is $4\space 5\space 3\space 1\space 2\space 2\space 1\space 3\space 5\space 4$. It can be seen that this is a palindrome. Another possible sequence of operations is $LRRLLRRRRR$, but it is lexicographically larger than the answer sequence.

## Sample 2

See [palin2.in](file://palin2.in) and [palin2.ans](file://palin2.ans).

## Constraints

Let $\sum n$ denote the sum of $n$ over all $T$ test cases. It is guaranteed that for each test file, $1 \le T \le 100$, $1 \le n$, and $\sum n \le 5 \times 10^5$.

| Tests        | $T$       | $n$                 | $\sum n$            | Special nature |
|:------------:|:---------:|:-------------------:|:-------------------:|:--------------:|
| $1 \sim 7$   | $\le 10$  | $\le 10$            | $\le 50$            | No             |
| $8 \sim 10$  | $\le 100$ | $\le 20$            | $\le 1000$          | No             |
| $11 \sim 12$ | $\le 100$ | $\le 100$           | $\le 1000$          | No             |
| $13 \sim 15$ | $\le 100$ | $\le 1000$          | $\le 25000$         | No             |
| $16 \sim 17$ | $= 1$     | $\le 5 \times 10^5$ | $\le 5 \times 10^5$ | No             |
| $18 \sim 20$ | $\le 100$ | $\le 5 \times 10^5$ | $\le 5 \times 10^5$ | Yes            |
| $21 \sim 25$ | $\le 100$ | $\le 5 \times 10^5$ | $\le 5 \times 10^5$ | No             |

Special nature: If we delete two adjacent and equal numbers in $a$ at a time, there is a way to delete the entire sequence (e.g., $a = [1, 2, 2, 1]$).
