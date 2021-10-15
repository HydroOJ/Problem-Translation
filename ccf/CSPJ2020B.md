## Description

NOI2130 will be held soon. In order to improve the viewing experience, CCF decided to reveal the scores of each participant one by one and broadcast real-time cutoffs. The win percentage of the competition is $w\%$, which means that among the participants who are currently in the top $w\%$, the minimum score of a participant is the current cutoff for winning.

More specifically, if the scores of $p$ participants have been revealed, the number of winners according to current scores is $\max(1, \floor{p * w\%})$, where $w$ is the win percentage of the competition, $\floor{x}$ is the largest integer that doesn't exceed $x$, and $\max(x, y)$ is the the larger number out of $x$ and $y$. If there are multiple participants with the same score as the cutoff, all of them are also winners, so the actual number of winners may be more than calculated above.

As a technician of the evaluation team, please help CCF write a live broadcast program.

## Input Format

The first line contains two integers $n$ and $w$ - the total number of participants and the win percentage respectively.

The second line contains $n$ integers denoting the scores of the participants that are revealed one by one (from left to right).

## Output Format

Print a single line containing $n$ space-separated non-negative integers denoting the cutoffs after the participants' scores are revealed one by one. The $i$-th integer should be the cutoff after the scores of the first $i$ participants have been revealed.

```input1
10 60
200 300 400 500 600 600 0 300 200 100
```
```output1
200 300 400 400 400 500 400 400 300 300
```

The first table below shows the number of winners as calculated by the formula after each participant's score is revealed. The first row contains the number of participants whose scores have been revealed, and the second row contains the corresponding number of winners as calculated by the formula. Note that after the 9th participant's score is revealed, the calculated number of winners is 5, but because there is another participant having the cutoff score, the actual number of winners is 6.

The second table below shows the scores of the participants from high to low (where the underlined score is the cutoff).

![](file://CSPJ2020B_1.png)

```input2
10 30
100 100 600 100 100 100 100 100 100 100
```
```output2
100 100 600 600 600 600 100 100 100 100
```

## Constraints

Tests $1 \sim 3$: $n = 10$\
Tests $4 \sim 6$: $n = 500$\
Tests $7 \sim 10$: $n = 2000$\
Tests $11 \sim 17$: $n = 10^4$\
Tests $18 \sim 20$: $n = 10^5$

For all the tests, each participant's score is a non-negative integer not greater than $600$, the win percentage $w$ is a positive integer, and $1 \le w \le 99$.

For calculating the number of winners, if you use floating-point numbers (such as float, double in C, C++, real, double, extended in Pascal, etc.) to store the win percentage $w$, the result of $5 \times 60\%$ may be $3.000001$, or it may be $2.999999$, or something else. The result of rounding down a number like this may be uncertain. Therefore, it is recommended to use only integers to calculate accurate values.
