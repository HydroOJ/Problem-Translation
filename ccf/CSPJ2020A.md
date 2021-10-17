## Description

Generally speaking, a positive integer can be split into the sum of several positive integers.

Example: $1 = 1, 10 = 1 + 2 + 3 + 4$.

For a positive integer $n$ we call it _excellent_ if and only if under this kind of separation, $n$ is broken down into several different numbers such that each number is a positive power of $2$. Note that a number $x$ can be expressed as a positive power of $2$, if and only if $x = 2^k$ for some integer $k \ge 1$.

Example: $10 = 8 + 2 = 2^3 + 2^1$ is an excellent split. But, $7 = 4 + 2 + 1 = 2^2 + 2^1 + 2^0$ is not an excellent split, because $1$ is not $2$ to the power of a positive integer.

Now, given a positive integer $n$, you need to judge whether there is an excellent split among all the splits of this number. If so, please give a specific split plan.

## Input Format

The input is only one line, an integer $n$, that represents the number to be split.

## Output Format

If there is an excellent split among all the splits of this number, then you need to output each number in this split from largest to smallest, separated by a space between two adjacent numbers. It can be proved that after the order of splitting numbers is specified, the splitting plan is unique.

If there is no excellent split, output `-1`.

```input1
6
```

```output1
4 2
```

```input2
7
```

```output2
-1
```

## Constraints

For $20\%$ of the data, $n \le 10$.  
For another $20\%$ of the data,  $n$ is guaranteed to be odd.  
For another $20\%$ of the data, $n$ is guaranteed to be a positive power of $2$.  
For $80\%$ of the data, $n \le 1024$.  
For $100\%$ of the data, $1 \le n \le 10^7$.
