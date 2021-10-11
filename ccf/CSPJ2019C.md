## Description

Xiaowei suddenly acquires a superpower. He knows the daily prices of $N$ souvenirs for the next $T$ days. The price of a souvenir refers to the number of gold coins required to buy the souvenir or the number of gold coins that can be earned by selling a souvenir.

Every day, Xiaowei can carry out the following two types of transactions any number of times:
1. Choose a souvenir. If he has enough gold coins with him, buy the souvenir at its price for that day.
2. Sell any souvenir he has and earn gold coins equal to the price of the souvenir for that day.

The gold coins earned by selling souvenirs on a day can be used to buy souvenirs on the same day too. Similarly, souvenirs purchased on a day can also be sold for gold coins on the same day.

After $T$ days, Xiaowei’s superpower will disappear. Therefore, he will sell all the souvenirs he still has on the $T$-th day.

Currently, Xiaowei has $M$ gold coins, and he wants to have as many gold coins as possible after the superpower disappears. What is the maximum number of gold coins he can have?

## Input Format

The first line contains three positive integers $T$, $N$ and $M$ - the number of days for which Xiaowei knows souvenir prices, the number of souvenirs, and the number of gold coins that Xiaowei currenly has.

$i$-th of the next $T$ lines contains $N$ positive integers $P_{i, 1}, P_{i, 2}, ..., P_{i, N},$ where $P_{i, j}$ denotes the price of the $j$-th souvenir on the $i$-th day.

## Output Format

Print one line containing a positive integer denoting the maximum number of gold coins Xiaowei can have after his superpower disappears.

```input1
6 1 100
50
20
25
20
25
50
```
```output1
305
```

The best strategy is:\
On the second day, spend all $100$ gold coins to buy $5$ units of souvenir $1$.\
Sell all the $5$ units of souvenir $1$ on the third day and get $125$ gold coins.\
Buy $6$ units of souvenir $1$ on the fourth day. $5$ gold coins are left.\
On the sixth day, sell all souvenirs for $300$ gold coins. On the fourth day there were $5$ gold coins remaining, so now there are $305$ gold coins remaining.\
After the superpower disappears, Xiaowei has $305$ gold coins, which is the maximum possible.

```input2
3 3 100
10 20 15
15 17 13
15 25 16
```
```output2
217
```

The best strategy is:\
On the first day, spend all the gold coins to buy $10$ units of souvenir $1$.\
Sell all the units of souvenir $1$ on the next day and get $150$ gold coins. Buy $8$ units of souvenir $2$ and $1$ unit of souvenir $3$. $1$ gold coin is remaining.\
On the third day, sell all souvenirs and get $216$ gold coins. On the second day, there was $1$ gold coin left, so in total there are $217$ gold coins left.\
After the superpower disappears, Xiaowei has $217$ gold coins, which is the maximum possible.

## Constraints

For $10\%$ of the data, $T = 1$.\
For $30\%$ of the data, $T \le 4, N \le 4, M \le 100, 10 \le P_{i, j} \le 1001$.\
For another $15\%$ of the data, $T \le 100, N = 1$.\
For another $15\%$ of the data, $T = 2, N \le 100$.\
For $100\%$ of the data, $T \le 100, N \le 100, M \le 10^3, 1 \le P_{i, j} \le 10^4$. It is guaranteed that at any time, the number of gold coins that Xiaowei has can't exceed $10^4$.
