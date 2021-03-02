### HW 8: Connect `n` processes with one pipe

An arbitrary number of arguments is passed to the program: CMD1, CMD2, ..., CMDN.
It is necessary to implement the equivalent of running them on the command line: CMD1 | CMD2 | ... | CMDN.
The parent process must end most recently! You must use only one pipe!

#### Examples
##### Input: `./a.out ls wc wc`
##### Output:
       1       3      25

#### Deadline:
Mar 15, 23:59:59

#### Points:
This task costs 12pts
