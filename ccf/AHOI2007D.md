## Description

The passage leading to the treasure house was opened, and down a long flight of stairs, through a short tunnel, you and Coco finally came to the door of the treasure house. What follows is the last challenge: as long as you can open the door of the treasure house, the treasure inside will be yours.

The door of the treasure house is still opened by a mechanism. This door is very strange. It is a square, divided into many smaller squares of the same size. These squares are either red or white. It seems that these squares form many red crosses. According to the treasure map, as long as you find the largest red cross on the door and press the square in the center of it, the door of the treasure house can be opened.

The red cross sign is also a square with side length $(2k+1)\times (2k+1)$, where $k$ is a non-negative integer. Its four sides are parallel to the sides of the door, and it consists of $(2k+1)\times (2k+1)$ small squares on the door. Here, the red cross symbol is based on white as the background color and red as the color of the cross. Suppose ```1``` is used for red and ```0``` is used for white. Corresponding to the data processed by the computer, barring the middle column and the middle row that are all ```1```s, the rest of the squares are all ```0```s. The following are several different sizes of signs:

```
1*1
1

3*3
010
111
010

5*5
00100
00100
11111
00100
00100
```

Xiao Keke is troubled by this mechanism, and now only depends on you. Please help him find the largest red cross sign on this door and output its side length.

## Input Format

The first line of the input file contains an integer $n$, which means that the gate consists of $n\times n$ squares.

The following $n$ lines have $n$ characters in each line, and each character is either ```0``` or ```1```. All zeros will not appear in the data.

## Output Format

Output a single integer, that is, the side length of the largest red cross.

```input1
5
00011
01011
11100
01001
00010
```
```output1
3
```

## Constraints

For $100\%$ data, $1\le n\le 2\times 10^3$. 
