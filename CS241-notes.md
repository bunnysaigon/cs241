//references: https://learnxinyminutes.com/docs/c/

1. Compiler flags

Compilation warnings and errors can be very useful information.
Explicitly using stricter compiler flags is recommended. Here are some recommended defaults:

```C
-Wall -Wextra -Werror -O2 -std=c99 -pedantic
```

2. Basic syntax
```C
// Define constants
#define DAYS_IN_YEAR 365

// Enumeration constants are also ways to declare constants.
// All statements must end with a semicolon
enum days {SUN = 1, MON, TUE, WED, THU, FRI, SAT};
// MON gets 2 automatically, TUE gets 3, etc.

// Import headers with #include
#include <stdlib.h>
#include <stdio.h>
#include <string.h>

// (File names between <angle brackets> are headers from the C standard library.)
// For your own headers, use double quotes instead of angle brackets:
//#include "my_header.h"

// Declare function signatures in advance in a .h file, or at the top of
// your .c file.
void function_1();
int function_2(void);




```
3. A pointer to void may be converted to or from a pointer to any incomplete or object type. A pointer to any incomplete or object type may be converted to a pointer to void and back again; the result shall compare equal to the original pointer.
