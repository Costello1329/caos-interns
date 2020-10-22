# HW 4: normalize_path

### Task:
Implement function `extern void normalize_path(char * path);` which handles filepathes (ending with any symbol except /) and directory pathes (ending with /). \
Function must convert text to the canonic form:
+ remove duplication of consecutive /
+ handle fragments ./ and ../

Restrictions:
+ It's forbidden to use string library function.
+ Use pointer arithmetic.

#### Examples:
##### Input:
abrakadabra///abc
##### Output:
abrakadabra/abc
##### Input:
/var/log/../lib/./ejexec
##### Output:
/var/lib/ejexec

#### Points:
The task costs 9 points.

#### Deadline:
2-nd Nov 2020 23:59:59
