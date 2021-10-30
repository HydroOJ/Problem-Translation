## Description

The password box was finally opened, and lying inside was an ancient treasure map. A treasure left by an ancient monarch, it was hidden in an underground palace, undiscovered so far. To obtain the treasure, you must crack numerous mechanisms. Xiao Keke is not afraid. As his good friends, you just started the treasure hunt. After overcoming all hardships, you came to the entrance of the underground palace and encountered your first trouble. The gate of the palace could not be opened. After careful observation, Xiao Keke discovered that there are some numbers on the left half of the door, arranged like a matrix of dimensions $n\times n$, and the corresponding position of the right half of the door also has the same $n\times n$ numbers, but the numbers are all $0$. These $0$s can be changed into other numbers, even negative numbers, but the arrangement method will not change.

Little Coco carefully studied the treasure map and found that to open this door, the numbers on the right half of the door must be changed according to a certain rule. If assuming that the left $n\times n$ matrix is ​​$A$, and the changed right $n\times n$ matrix is $B$, this rule is that the product matrix $C$ of matrix $A, B$ satisfies $C_{i,j}=\sum_{k=1}^n a_{i,k}\times b_{k,j}$, and $C=A\times B=E_n$​.

Among them, $E_n$​ is:

- If $i=j$, $E_{i,j}=1$;
- Otherwise, $E_{i,j}=0$.

Namely, $B$ is the inverse matrix of $A$.

Can you help Coco open this door?


## Input Format

The first line of the input file contains an integer $n$.

In the next $n$ lines, each line contains $n$ numbers, and each element of $A$ is given in row major order, namely:

$A_{1,1}, A_{1,2},\dots ,A_{1,n},$

$A_{2,1}, A_{2,2},\dots ,A_{2,n},$

$\dots$

$A_{n,1}, A_{n,2}, \dots,A_{n,n}$

## Output Format

The output file contains $n$ lines: each line has $n$ integers, and it is between $-2\times 10^9$ and $2\times 10^9$, every two adjacent numbers separated by a space; that is, the matrix $B$ expressed in the row major order.

The input data ensures that this matrix $B$ exists, each element of $B$ is an integer, and it is between $-2\times 10^9$ and $2\times 10^9$.

Special note: Because the test adopts the file comparison method, if a number in the result is $0$, the program should output ```0``` instead of ```-0```.


```input1
3
1 -1 1
0 1 2
1 0 4
```
```output1
4 4 -3
2 3 -2
-1 -1 1
```

## Constraints

For $100\%$ data, $1\le n\le 200$, $-2\times 10^9 \le A_{i,j},B_{i,j}\le 2\times 10^9$.
