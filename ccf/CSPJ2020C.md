## Description

Little C is eager to learn mathematical logic. One day, he discovered a special logical expression. In this kind of logical expression, all operands are variables and can only take the values $0$ and $1$. The calculation proceeds from left to right. If there are parentheses in the expression, the value of the sub-expression inside the parentheses is calculated first. In particular, this expression has only the following operations:
1. AND operation: ```a & b```. If and only if the values of both $a$ and $b$ are $1$, the value of the expression is $1$. Otherwise, the value of the expression is $0$.
2. OR operation: ```a | b```. If and only if the values of both $a$ and $b$ are $0$, the value of the expression is $0$. Otherwise, the value of the expression is $1$.
3. Negation operation: ```!a```. If and only if the value of $a$ is $0$, the value of the expression is $1$. Otherwise, the value of the expression is $0$.

Given a logical expression and the initial value of each operand, Little C wants to know the value of the original expression when the value of an operand is inverted.

In order to simplify the processing of expressions, we have the following conventions:

The expression will be given in the form of a **postfix expression**.

A postfix expression is defined as follows:
1. If $E$ is an operand, the postfix expression of $E$ is $E$ itself.
2. If $E$ is an expression of the form $E_1~\texttt{op}~E_2$, where $\texttt{op}$ is any binary operator with precedence no higher than the precedences of the operators outside the parentheses in $E_1$ and $E_2$, then the postfix expression of $E$ is $E_1'~E_2'~\texttt{op}$, where $E_1'$ and $E_2'$ are the postfix expressions of $E_1$ and $E_2$ respectively.
3. If $E$ is an expression of the form $E_1$, the postfix expression of $E$ is the postfix expression of $E_1$.

For convenience while taking input, there is a space around the AND operator (```&```), the OR operator (```|```), and the negation operator (```!```), but there is no space at the end of the input expression.

An operand is formed by concatenating the lowercase letter ```x``` with a positive integer which represents the subscript of this variable. For example, ```x10``` represents the variable $x_{10}$. It is guaranteed that each variable appears exactly once in the expression.

## Input Format

The first line contains a string $s$ denoting the expression as described above.

The second line contains a positive integer $n$ denoting the number of variables in the expression. The subscripts of the variables in the expression are $1, 2, \cdots, n$.

The third line contains $n$ integers, where the $i$-th integer denotes the initial value of the variable $x_i$.

The fourth line contains a positive integer $q$ denoting the number of queries.

Each of the next $q$ lines contains a positive integer denoting the subscript of the variable that needs to be inverted. Note that the modification done in each query is temporary, i.e., the modification done in the previous query doesn't affect the subsequent query.

It is guaranteed that the given expression is valid and the initial value of each variable is $0$ or $1$.

## Output Format

Print $q$ lines, one per query, containing the value of the expression ($0$ or $1$) for that query.

```input1
x1 x2 & x3 |
3
1 0 1
3
1
2
3
```
```output1
1
1
0
```

The infix expression equivalent to the given postfix expression is $(x_1 \& x_2) | x_3$.

In the first query, the value of $x_1$ is inverted. Now the values of the three variables are $0, 0, 1$. The value of the original expression is $(0 \& 0) | 1 = 1$.

In the second query, the value of $x_2$ is inverted. Now the values of the three variables are $1, 1, 1$. The value of the original expression is $(1 \& 1) | 1 = 1$.

In the third query, the value of $x_3$ is inverted. Now the values of the three variables are $1, 0, 0$. The value of the original expression is $(1 \& 0) | 0 = 0$.

```input2
x1 ! x2 x4 | x3 x5 ! & & ! &
5
0 1 0 1 1
3
1
3
5
```
```output2
0
1
1
```

The infix expression equivalent to the given postfix expression is $(!x_1) \& (!((x_2 | x_4) \& (x_3 \& (!x_5))))$.

## Constraints

For $20\%$ of the data, the expression contains only the AND operation (```&```) or only the OR operation (```|```).\
For another $30\%$ of the data, $|s| \le 1000, q \le 1000, n \le 1000$.\
For another $20\%$ of the data, the initial values of the variables are all $0$ or all $1$.\
For $100\%$ of the data, $1 \le |s| \le 10^6, 1 \le q \le 10^5, 2 \le n \le 10^5$.

$|s|$ represents the length of the string $s$.
