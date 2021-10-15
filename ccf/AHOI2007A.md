## Description

Little Coco got a password box from nowhere. She heard that there's a treasure map about a treasure burried down long time ago inside the box so she want to open it to find that map. The box will be opened if you type in the correct password. After some deciphering, she found out that those icons at the back of the box represent a number and the relationship between this number and the correct password. Let this number be $x$, then the following rule will be fullfil:
* $0 \le x \le n$
* $x^2 \mod n = 1$

Little Coco knows that there maybe more than one $x$ that meets above conditions, and the password must be one of those $x$. Can you help Coco finding out those number? (It is guaranteed that $x, n$ are all positive integers).

## Input Format

A single line containing one integer $n$.

## Output Format

Contains all numbers $x$ that meet the conditions in increasing order, one each line. If there's no such $x$, you must print one line containing "None" (without the quote).

```input1
12
```
```output1
1
5
7
11
```

## Constraints

For $100\%$ data, $1 \le n \le 2 \times 10^9$.
