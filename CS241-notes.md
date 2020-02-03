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

// Use typedef 
// 1
typedef enum { false, true } bool;
  // for C don't have bool as data type before C99 :(
  bool disaster = false;
  int i, j;
  for(i=0;i<100;++i)
  for(j=0;j<100;++j)
  {
    if((i + j) >= 150)
        disaster = true;
    if(disaster)
        goto error;
  }
  error :
  printf("Error occurred at i = %d & j = %d.\n", i, j);
  
  // 2
  typedef unsigned char BYTE;
  typedef unsigned char byte;
  
  // 3 struct
  typedef struct Books {
    char title[50];
    char author[50];
    char subject[100];
    int book_id;
  } Book;

   Book book;
 
   strcpy( book.title, "C Programming");
   strcpy( book.author, "Nuha Ali"); 
   strcpy( book.subject, "C Programming Tutorial");
   book.book_id = 6495407;
   
   // Pointer
   int x = 0;
  printf("%p\n", (void *)&x); // Use & to retrieve the address of a variable
  // (%p formats an object pointer of type void *)
  // => Prints some address in memory;

  // Pointers start with * in their declaration
  int *px, not_a_pointer; // px is a pointer to an int
  px = &x; // Stores the address of x in px
  printf("%p\n", (void *)px); // => Prints some address in memory
  printf("%zu, %zu\n", sizeof(px), sizeof(not_a_pointer));
  // => Prints "8, 4" on a typical 64-bit system

  
  
  
  

```
3. A pointer to void may be converted to or from a pointer to any incomplete or object type. A pointer to any incomplete or object type may be converted to a pointer to void and back again; the result shall compare equal to the original pointer.
