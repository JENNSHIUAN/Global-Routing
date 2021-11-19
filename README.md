# Globel Routing

This programming assignment asks you to write a global router that can route 2-pin nets (connection between two points). The problem description below is a simplified routing problem. Given the problem size (the number of horizontal and vertical tiles), capacity, and a netlist, the global router routes all nets in the routing region. The main objective is to minimize the total overflows. Here the overflow on a tile boundary is calculated as the amount of demand that excesses the capacity, i.e., overflow = max(0, demand-capacity)

## Input

The file format for the global routing is illustrated, with comments in italics (these will not be in actual input files). The 1st line gives the problem size in terms of the number of horizontal and vertical tiles. Each global routing tile (tile in short) has a capacity on its four boundaries to measure the available space, which is the maximum number of routing paths passing through boundaries. The capacity value is given by the 2nd line. The 3rd line gives the number of nets and following indicate each net, including starting position and terminal position. The input file format is as follows:

![alt text](https://github.com/JENNSHIUAN/Global-Routing/blob/main/Figure/inpur_format.PNG?raw=true)

## Output

All the routes in the output could only be horizontal lines and vertical lines. For example (18, 61)-(19, 62) is not acceptable, because it is diagonal. Remember that each route could be different either in the x or y location only, and the difference must be 1. The output file format is as follows:

![alt text](https://github.com/JENNSHIUAN/Global-Routing/blob/main/Figure/output_format.PNG?raw=true)

![Red text] Note that for a certain net, x11, y11, xk2 and yk2 must be the same as xs, ys, xt and yt in the input file respectively. Also, for any i, xi2 and yi2 must be the same as x(i+1)1 and y(i+1)1 respectively.


## Sample

###### Sample case

![alt text](https://github.com/JENNSHIUAN/Global-Routing/blob/main/Figure/sample_case.PNG?raw=true)

###### Sample Input File

![alt text](https://github.com/JENNSHIUAN/Global-Routing/blob/main/Figure/sample_input_file.PNG?raw=true)

###### Sample Output File

![alt text](https://github.com/JENNSHIUAN/Global-Routing/blob/main/Figure/sample_output_file.PNG?raw=true)

The total overflow is 1, which is caused by the boundary between tiles (1,1) and (1,2). (The total wirelength is 13.)

## Compile

```bash
$ gcc -o main main.c
```

## Usage

```bash
$ ./main [input file.in] [output file.out]
```

## REMARKS

This is a homework from Algorithm Design and Application Lesson NTUST 2019 fall semester.
