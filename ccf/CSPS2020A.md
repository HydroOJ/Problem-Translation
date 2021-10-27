## Description

To make calculations easier, astronomers use Julian Day to express time. The Julian Day is defined as the number of days that have elapsed from 12 noon on January 1, 4713 BC to a certain time thereafter. If it is less than one day, it is expressed as a decimal. If this astronomical calendar is used, every moment will be evenly mapped to the number axis, so that the difference between them can be easily calculated.

Now, given a Julian Day without a decimal part, please calculate the Gregorian date corresponding to the Julian Day (it must be 12 noon on a certain day).

Our current calendar is the Gregorian calendar, which was modified on the basis of the original Julian calendar by Pope Gregory XIII in 1582. It is not directly related to the Julian Day. Specifically, the current Gregorian calendar date is calculated according to the following rules:

1. After October 15, 1582 (inclusive): Gregorian calendar is applicable, $31$ days in January, $28$ days or $29$ days in February, $31$ days in March, $30$ days in April, $31$ days in May, $30$ days in June, July $31$ days, August $31$ days, September $30$ days, October $31$ days, November $30$ days, December $31$ days. Among them, the February of a leap year is $29$ days, and the average year is $28$ days. When the year is a multiple of $400$, or the year is a multiple of $4$ but not a multiple of $100$, the year is a leap year.
2. October 5th (inclusive) to October 14th (inclusive), 1582 AD: These dates have been deleted, and October 4th is followed by October 15th of the year.
3. Before October 4, 1582 AD (inclusive): the Julian calendar is applicable, and the number of days in a month is the same as the Gregorian calendar, but as long as the year is a multiple of $4$, it is a leap year.
4. Although the Julian calendar was only implemented in 45 BC and had undergone several adjustments in the early days, today humans are accustomed to deduct everything before October 4, 1582 according to the final rules of the Julian calendar. Note that the **year zero does not exist**, that is, the year following the year 1 BC is the year 1 AD. Therefore, the first year BC, the first 5 years, the first 9 years, the first 13 years... and so on should be regarded as leap years.

## Input Format

The input file name is `julian.in`.

The first line contains an integer $Q$, the number of test cases.

The next $Q$ lines contain non-negative integers. Each line contains $r_i$, $i$ -th Julian Day.

## Output Format

The output file is `julian.out`.

Output $Q$ lines where each line is a string $s_i$ representing the date for Julian Day, $r_i$.

The format is as follows:

1. If the year is after the AD, the output format is `Day Month Year`. The day, month, and year do not contain any leading zeros and are separated by a space. For example: at 12 noon on November 7, 2020, the output is `7 11 2020`.
2. If the year is BC, the output format is ` Day Month Year BC`. The year outputs the value of the year, and the rest is the same as after the AD. For example: at 12 noon on February 1, 841 BC, the output is `1 2 841 BC`.

```input1
3 
10
100
1000
```
```output1
11 1 4713 BC 
10 4 4713 BC
27 9 4711 BC
```

```input2
3 
2000000 
3000000
4000000
```
```output2
14 9 763 
15 8 3501
12 7 6239
```



## Constraints

|Test Point Number|$Q$=|$r_i\le$
|:---:|:---:|:---:|
|1|$10^3$|$365$|
|2|$10^3$|$10^4$|
|3|$10^3$|$10^5$|
|4|$10^4$|$3\times10^5$|
|5|$10^4$|$2.5\times10^5$|
|6|$10^5$|$2.5\times10^5$|
|7|$10^5$|$5\times10^6$|
|8|$10^5$|$10^7$|
|9|$10^5$|$10^9$|
|10|$10^5$|doesn't exceed $10^9$|