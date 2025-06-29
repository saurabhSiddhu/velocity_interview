# Day 1 Mock Interview: Aptitude & C MCQs

**Date:** 2025-06-28  
**Time Allotted:** 45 minutes

---

## Section 1: Aptitude (Quantitative & Logical)

1. (Time & Work) If 4 men can complete a task in 6 days, how many days will 3 men take to complete the same task?
2. (Profit & Loss) A shopkeeper buys an item for $200 and sells it for $250. Find the profit percentage.
3. (Speed & Distance) A car travels 60 km in 1.5 hours. What is its average speed?
4. (Percentages) What is 20% of 150?
5. (Averages) The average of 5, 7, 9, 11, 13 is?
6. (Ratio & Proportion) If the ratio of boys to girls in a class is 3:2 and there are 30 students, how many girls are there?
7. (Simple Interest) Principal = $1000, Rate = 5% per annum, Time = 2 years. Find the simple interest.
8. (Compound Interest) Principal = $2000, Rate = 10% per annum, Time = 2 years. Find the compound interest (compounded annually).
9. (Ages) The sum of ages of a father and son is 60 years. After 5 years, the father's age will be twice the son's age. Find their present ages.
10. (Logical Reasoning) If all roses are flowers and some flowers fade quickly, can we say that some roses fade quickly?

---

## Section 2: C Language MCQs (Input/Output & Error Finding)

1. What will be the output of the following code?

```c
#include <stdio.h>
int main() {
    int a = 5, b = 2;
    printf("%d", a / b);
    return 0;
}
```

A) 2.5 B) 2 C) 3 D) Error

2. What will be the output?

```c
#include <stdio.h>
int main() {
    int arr[3] = {1, 2, 3};
    printf("%d", arr[3]);
    return 0;
}
```

A) 3 B) 0 C) Garbage value D) Error

3. Find the error in the code:

```c
#include <stdio.h>
int main() {
    int x = 10;
    if(x = 5)
        printf("x is 5");
    return 0;
}
```

A) No error B) Assignment used instead of comparison C) Missing semicolon D) None

4. What will be the output?

```c
#include <stdio.h>
int main() {
    int i = 0;
    while(i < 3)
        printf("%d ", i);
        i++;
    return 0;
}
```

A) 0 1 2 B) 0 0 0 C) Infinite loop D) Compilation error

5. What is the output?

```c
#include <stdio.h>
int main() {
    printf("%d", sizeof('A'));
    return 0;
}
```

A) 1 B) 2 C) 4 D) Depends on compiler

6. What will be the output?

```c
#include <stdio.h>
int main() {
    int a = 10;
    printf("%d", ++a + a++);
    return 0;
}
```

A) 21 B) 22 C) 23 D) Undefined behavior

7. Find the error in the code:

```c
#include <stdio.h>
int main() {
    int arr[2];
    arr[0] = 1;
    arr[1] = 2;
    arr[2] = 3;
    printf("%d", arr[2]);
    return 0;
}
```

A) No error B) Array index out of bounds C) Compilation error D) None

8. What will be the output?

```c
#include <stdio.h>
int main() {
    int x = 5;
    printf("%d", x == 5 ? 10 : 20);
    return 0;
}
```

A) 5 B) 10 C) 20 D) Error

9. What is the output?

```c
#include <stdio.h>
int main() {
    int i = 0;
    for(; i < 3; )
        printf("%d ", i++);
    return 0;
}
```

A) 0 1 2 B) 1 2 3 C) 0 1 2 3 D) Compilation error

10. Find the error in the code:

```c
#include <stdio.h>
int main() {
    int *p;
    *p = 10;
    printf("%d", *p);
    return 0;
}
```

A) No error B) Dereferencing uninitialized pointer C) Compilation error D) None

---

**Instructions:**

- Attempt all questions in 45 minutes.
- For C MCQs, select the correct option and briefly explain your choice.
