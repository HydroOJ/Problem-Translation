## Description

Kaikai's factory is producing some kind of magical parts, and the production process of magical parts is, naturally, also magical. The factory has $n$ workers numbered from $1$ to $n$. There are bidirectional conveyor belts between some workers. It is guaranteed that there is at most one conveyor belt between any two workers.

If worker $x$ wants to produce a part that is in the $L$-th stage ($L > 1$) of production, all workers who are directly connected to worker $x$ via a conveyor belt have to produce a part that is in stage $L - 1$ (but worker $x$ doesn't need to produce a stage $L - 1$ part).

If worker $x$ wants to produce a part that is in stage $1$ of production, all workers who are directly connected to worker $x$ via a conveyor belt have to provide worker $x$ with raw materials.

Xuan Xuan is worker $1$. Given $q$ work orders, the $i$-th work order is represented by two numbers $a_i$ and $L_i$ denoting that worker $a_i$ wants to produce a part in stage $L_i$ of production. Xuan Xuan wants to know whether he needs to provide raw materials to others for each work order. He knows that you are smart and can help him figure it out!

## Input Format

The first line contains three positive integers $n, m$ and $q$ - the number of workers, the number of conveyor belts, and the number of work orders respectively.

Each of the next $m$ lines contains two integers $u$ and $v$ ($u \neq v$) denoting that there is a conveyor belt between the workers $u$ and $v$.

Each of the next $q$ lines contains two positive integers $a$ and $L$ denoting that worker $a$ wants to produce a part in stage $L$.

## Output Format

For each work order print a single line containing ```Yes``` if Xuan Xuan needs to provide raw materials for that work order, and ```No``` otherwise.

```input1
3 2 6
1 2
2 3
1 1
2 1
3 1
1 2
2 2
3 2
```
```output1
No
Yes
No
Yes
No
Yes
```

![](file://5dbepjmh.png)

For the first work order, worker 1 wants to produce a stage 1 part, so worker 2 needs to provide raw materials.

For the second work order, worker 2 wants to produce a stage 1 part, so workers 1 and 3 need to provide raw materials.

For the third work order, worker 3 wants to produce a stage 1 part, so worker 2 needs to provide raw materials.

For the fourth work order, worker 1 wants to produce a stage 2 part, so worker 2 needs to produce a stage 1 part, and workers 1 and 3 need to provide raw materials.

For the fifth work order, worker 2 wants to produce a stage 2 part, so workers 1 and 3 need to produce a stage 1 part, and both of them need worker 2 to provide raw materials.

For the sixth work order, worker 3 wants to produce a stage 2 part, so worker 2 needs to produce a stage 1 part, and workers 1 and 3 need to provide raw materials.

```input2
5 5 5
1 2
2 3
3 4
4 5
1 5
1 1
1 2
1 3
1 4
1 5
```
```output2
No
Yes
No
Yes
Yes
```

![](file://tfom5z2s.png)

For the first work order, worker 1 wants to produce a stage 1 part, so workers 2 and 5 need to provide raw materials.

For the second work order, worker 1 wants to produce a stage 2 part, so workers 2 and 5 need to produce a stage 1 part, and workers 1, 3 and 4 need to provide raw materials.

For the third work order, worker 1 wants to produce a stage 3 part, so workers 2 and 5 need to produce a stage 2 part, workers 1, 3 and 4 need to produce a stage 1 part, and workers 2, 3, 4 and 5 need to provide raw materials.

For the fourth work order, worker 1 wants to produce a stage 4 part, so workers 2 and 5 need to produce a stage 3 part, workers 1, 3 and 4 need to produce a stage 2 part, workers 2, 3, 4 and 5 need to produce a stage 1 part, and all workers need to provide raw materials.

For the fifth work order, worker 1 wants to produce a stage 5 part, so workers 2 and 5 need to produce a stage 4 part, workers 1, 3 and 4 need to produce a stage 3 part, workers 2, 3, 4 and 5 need to produce a stage 2 part, all workers need to produce a stage 1 part, and all workers need to provide raw materials.

## Constraints

There are a total of 20 tests.\
$1 \le u, v, a \le n$\
Tests $1 \sim 4$: $1 \le n, m \le 1000, q = 3, L = 1$\
Tests $5 \sim 8$: $1 \le n, m \le 1000, q = 3, 1 \le L \le 10$\
Tests $9 \sim 12$: $1 \le n, m, L \le 1000, 1 \le q \le 100$\
Tests $13 \sim 16$: $1 \le n, m, L \le 1000, 1 \le q \le 10^5$\
Tests $17 \sim 20$: $1 \le n, m, q \le 10^5, 1 \le L \le 10^9$
