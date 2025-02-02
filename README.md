# Integer Division Truncation in C

This repository demonstrates an example of integer division truncation in C. Integer division in C truncates the result towards zero. This means that any fractional part is discarded, which can lead to unexpected results if not handled carefully.

## Bug

The `bug.c` file demonstrates a simple example of integer division: 

```c
int main() { 
    int x = 10;
    int y = 5; 
    int z = x / y; 
    printf("%d", z); 
    return 0; 
}
```

In this code snippet, `x` is divided by `y`. The expected result would be `2.0`, however, the result will be `2` because C's integer division truncates the result. This might lead to inaccurate calculations if you expect a floating-point value.  

## Solution

To address this, ensure that you are using floating-point data types (float or double) when floating-point precision is necessary.

The solution is provided in `bugSolution.c`. Using floating-point types will calculate and print the floating-point value.

```c
#include <stdio.h>
int main() {
    float x = 10.0; 
    float y = 5.0; 
    float z = x / y; 
    printf("%f", z); 
    return 0; 
}
```