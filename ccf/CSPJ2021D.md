## Description

Bear's fruit shop has a row of $n$ fruits. Each fruit is either an apple or an orange, numbered from left to right using positive integers $1, 2, 3, \dots, n$. The same kind of fruits appearing together is called a "block". The bear has to pick the row of fruits into several fruit baskets: each time, pick the leftmost fruit in each block simultaneously to form a fruit basket. Repeat this operation until there's no fruit left. Note that the "blocks" may change after each picking of a fruit basket. For example, when the only orange between two apple "blocks" is picked, the two apple "blocks" become one "block". Please help the bear to figure out the fruits contained in each fruit basket.

## Input Format

Read input from the file ```fruit.in```.

The first line contains a positive integer $n$ denoting the number of fruits.

The second line contains $n$ space-separated integers where the $i$-th integer denotes the type of fruit $i$ ($1$ for apples and $0$ for oranges).

## Output Format

Write output to the file ```fruit.out```.

Print several lines.\
The $i$-th line should correspond to the fruit basket consisting of the fruits picked in the $i$-th picking. Print the numbers of all fruits in the basket sorted in increasing order and separated by spaces.

```input1
12
1 1 0 0 1 1 1 0 1 1 0 0
```
```output1
1 3 5 8 9 11
2 4 6 12
7
10
```

Initially, the row of fruits is $1~1~0~0~1~1~1~0~1~1~0~0$. There are a total of $6$ blocks.\
In the first picking of fruits to form a fruit basket, the fruits numbered $1~3~5~8~9~11$ are picked.\
Now the remaining fruits are $1~0~1~1~1~0$. There are a total of $4$ blocks.\
In the second picking of fruits to form a fruit basket, the fruits numbered $2~4~6~12$ are picked.\
The remaining fruits are $1~1$. There is only $1$ block.\
In the third picking of fruits to form a fruit basket, the fruit numbered $7$ is picked.\
The last remaining fruit is $1$, and there is only $1$ block.\
In the fourth picking of fruits to form a fruit basket, the fruit numbered $10$ is picked.

```input2
20
1 1 1 1 0 0 0 1 1 1 0 0 1 0 1 1 0 0 0 0
```
```output2
1 5 8 11 13 14 15 17
2 6 9 12 16 18
3 7 10 19
4 20
```

## Sample 3

See [fruit3.in](file://fruit3.in) and [fruit3.ans](file://fruit3.ans).

## Constraints

For $10\%$ of the data, $n \le 5$.\
For $30\%$ of the data, $n \le 1000$.\
For $70\%$ of the data, $n \le 50000$.\
For $100\%$ of the data, $n \le 2 \times 10^5$.

Due to the large size of the data, it is recommended that C/C++ users use `scanf` and `printf` for input and output.
