## Section A Answers

### Q1. (a) Write a short note on type casting.
- Type casting is the process of converting a variable from one data type to another.
- It can be explicit (using casting operators) or implicit (automatic by the compiler).
- Example: Converting an `int` to a `float` using `(float)`.

### Q1. (b) Define relational operator?
- A relational operator compares two values and returns a boolean result (true or false).
- Common examples include `==`, `!=`, `<`, `>`, `<=`, and `>=`.
- Used in decision-making statements like `if` conditions.

### Q1. (c) Write and explain syntax of --for-- and do-while loop.
- **For loop syntax**: `for (initialization; condition; increment) { statement; }` - Executes a block of code repeatedly until the condition is false.
- **Do-while loop syntax**: `do { statement; } while (condition);` - Executes the block at least once, then repeats if the condition is true.
- Example: `for (i = 0; i < 5; i++)` vs. `do { i++; } while (i < 5)`.

### Q1. (d) Distinguish between while and do-while statements.
- `while` checks the condition before execution, so the loop may not run if the condition is false initially.
- `do-while` executes the block once before checking the condition, ensuring at least one execution.
- Example: `while (i < 0)` vs. `do { i++; } while (i < 0)`.

### Q1. (e) What is pseudocode?
- Pseudocode is a high-level description of a program using natural language and programming constructs.
- It is not executable but helps in planning and designing algorithms.
- Example: "Start, set x = 0, while x < 10, print x, increment x, end."

### Q1. (f) Write different notations in flow chart.
- Common notations include ovals (start/end), rectangles (process), diamonds (decision), and arrows (flow direction).
- Used to visually represent the logic and sequence of a program.
- Example: Oval for "Start", Diamond for "Is x > 0?".

### Q1. (g) How to declare and initialize flow chart.
- Declare a flowchart by starting with an oval ("Start") and ending with an oval ("End").
- Initialize by adding process boxes and decision diamonds with appropriate arrows.
- Example: Start → Process "Set x = 0" → End.

### Q1. (h) What is #include, #define
- `#include` is a preprocessor directive to include header files (e.g., `#include <stdio.h>`).
- `#define` is used to define constants or macros (e.g., `#define MAX 100`).
- Both are processed before compilation.

### Q1. (i) Write and explain the directives.
- Directives like `#include` and `#define` instruct the compiler on pre-processing tasks.
- `#include` adds external code, while `#define` substitutes text.
- Example: `#define PI 3.14` replaces `PI` with `3.14` in code.

### Q1. (j) Define pointer array syntax of function?
- A pointer array holds addresses of variables, syntax: `int *arr[5];` (array of 5 integer pointers).
- Function syntax with pointer array: `void func(int *arr[])` (pass array of pointers).
- Used for dynamic memory or multi-dimensional data handling.

### Q1. (k) What is array of strings?
- An array of strings is an array where each element is a string (array of characters).
- Syntax: `char str[5][10];` (5 strings, each up to 9 chars + null).
- Example: `str[0] = "hello";`.

### Q1. (l) Discriminate putc() and gets()
- `putc()` writes a single character to a file, syntax: `putc(ch, fp);`.
- `gets()` reads a string from stdin, syntax: `gets(str);` (now deprecated).
- Difference: `putc` is character-based, `gets` is string-based.

### Q1. (m) How can you compare two strings?
- Compare strings using `strcmp(str1, str2)` from `<string.h>`, returns 0 if equal.
- Compares lexicographically based on ASCII values.
- Example: `if (strcmp(str1, str2) == 0)`.

### Q1. (n) Define Data Types in C.
- Data types define the type of data a variable can hold (e.g., `int`, `float`, `char`).
- Includes primitive (int, char) and derived types (array, pointer).
- Example: `int x = 10;` declares an integer.

## Part B Answers

### Q2. Write the structure of C program and explain. Write a program to perform swapping of two numbers without using temporary variable.
A C program typically follows a structured format that includes several key sections. It begins with preprocessor directives like `#include <stdio.h>` to include necessary header files for input/output operations. Next, the `main()` function serves as the entry point where the program execution starts, enclosed within curly braces `{}`. Inside `main()`, global and local variables are declared, followed by the logic implemented using statements, loops, or conditionals. The program ends with a return statement, usually `return 0`, to indicate successful execution. Comments can be added using `//` or `/* */` for clarity.

Here’s an explanation of a program to swap two numbers without a temporary variable, which uses arithmetic operations. Consider two variables, `a` and `b`. The swapping can be done by adding `a` and `b` and storing the sum in `a`, then subtracting the original `b` from this sum to get the new `a`, and finally subtracting the new `a` from the sum to get the new `b`. This method avoids using extra memory.

**Program Example:**
```c
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("Before swapping: a = %d, b = %d\n", a, b);
    a = a + b;  // Step 1: Add both numbers
    b = a - b;  // Step 2: Subtract original b from sum to get new b
    a = a - b;  // Step 3: Subtract new b from sum to get new a
    printf("After swapping: a = %d, b = %d\n", a, b);
    return 0;
}```

### Q3. Define algorithm and Pseudocode. Write algorithm and pseudocode for finding factorial of a number.
An algorithm is a step-by-step procedure or set of rules to solve a problem or complete a task, expressed in a logical sequence. It acts as a blueprint for programming, ensuring clarity before coding. Pseudocode, on the other hand, is a high-level, human-readable description of an algorithm using a mix of natural language and programming constructs, without strict syntax rules. It helps plan the logic and is later translated into actual code.
Algorithm for Factorial of a Number:
Start.

Input a number n.

Initialize a variable fact to 1.

Check if n is less than 0, if yes, display an error and stop.

For each integer i from 1 to n, multiply fact by i.

After the loop, fact contains the factorial of n.

Display fact.

Stop.
Pseudocode for Factorial of a Number:
BEGIN
    INPUT n
    SET fact = 1
    IF n < 0 THEN
        PRINT "Factorial not defined for negative numbers"
        STOP
    END IF
    FOR i = 1 TO n DO
        SET fact = fact * i
    END FOR
    PRINT "Factorial of", n, "is", fact
END


### Q4. Explain various branching statements in C with examples. Write a program to generate prime numbers between 1 and n (given by user).
Branching statements in C control the flow of execution based on conditions. The primary ones are if, if-else, else-if ladder, and switch. The if statement executes a block if a condition is true. The if-else adds an alternative block for a false condition. The else-if ladder handles multiple conditions sequentially, and switch selects a case based on a value. These statements are crucial for decision-making.
Example of Branching:
if (a > b) printf("a is greater"); - Simple if.

if (a > b) printf("a is greater"); else printf("b is greater"); - If-else.

switch (day) { case 1: printf("Monday"); break; } - Switch.
Program to Generate Prime Numbers:
c
``` #include <stdio.h>
int main() {
    int n, i, j, isPrime;
    printf("Enter a number n: ");
    scanf("%d", &n);
    printf("Prime numbers between 1 and %d are: ", n);
    for (i = 2; i <= n; i++) {
        isPrime = 1;
        for (j = 2; j <= i / 2; j++) {
            if (i % j == 0) {
                isPrime = 0;
                break;
            }
        }
        if (isPrime) printf("%d ", i);
    }
    return 0;
}```


### Q5. Define an array. How to initialize one-dimensional array? Explain with suitable examples. Write a C program to sort the given array elements in Ascending order.
An array is a collection of elements of the same data type stored in contiguous memory locations, accessed using an index. It allows efficient data handling for multiple values under a single name. A one-dimensional array is a linear list, declared with a fixed size, e.g., int arr[5].
Initialization of One-Dimensional Array:
Direct initialization: int arr[5] = {1, 2, 3, 4, 5};.

Partial initialization: int arr[5] = {1, 2}; (remaining elements set to 0).

At runtime: scanf("%d", &arr[i]); to input values.
Program to Sort Array in Ascending Order:
c
``` #include <stdio.h>
int main() {
    int arr[100], n, i, j, temp;
    printf("Enter the size of array: ");
    scanf("%d", &n);
    printf("Enter %d elements: ", n);
    for (i = 0; i < n; i++) scanf("%d", &arr[i]);
    for (i = 0; i < n - 1; i++)
        for (j = 0; j < n - i - 1; j++)
            if (arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
    printf("Sorted array: ");
    for (i = 0; i < n; i++) printf("%d ", arr[i]);
    return 0;
}``` 


### Q6. What are the features of pointers? Write a C program to print address of a variable.
- Pointers are variables that store memory addresses of other variables, enabling direct memory manipulation. Key features include: they allow dynamic memory allocation, provide efficiency in passing large data structures, enable array handling, and support pointer arithmetic for traversing memory. They require careful use to avoid issues like dangling pointers.
Program to Print Address of a Variable:
c
``` #include <stdio.h>
int main() {
    int x = 10;
    int *ptr = &x;
    printf("Value of x: %d\n", x);
    printf("Address of x: %p\n", (void*)ptr);
    printf("Value via pointer: %d\n", *ptr);
    return 0;
}``` 

This program declares an integer x, a pointer ptr to its address, and prints both the value and address using %p with a type cast to void*. It showcases pointer dereferencing and address access.


### Q7. Define Structure and write the general syntax for declaring and accessing members. How to copy and compare structure variables? Illustrate with example.
A structure in C is a user-defined data type that groups different data types under a single name, allowing complex data representation. It’s declared using the struct keyword, and members are accessed with the dot (.) operator for objects or arrow (->) for pointers.
General Syntax:
Declaration: struct struct_name { data_type member1; data_type member2; } var;.

Accessing: var.member1 = value;.

Example: struct Student { int id; char name[20]; };.
Copying and Comparing Structure Variables:
Structures can be copied by assignment, copying all members. Comparison requires member-wise comparison since direct == isn’t allowed.
Example Program:
c
``` #include <stdio.h>
struct Student {
    int id;
    char name[20];
};
int main() {
    struct Student s1 = {1, "Alice"};
    struct Student s2, s3;
    s2 = s1;  // Copying s1 to s2
    printf("s2 id: %d, name: %s\n", s2.id, s2.name);
    s3.id = s1.id;
    strcpy(s3.name, s1.name);  // Member-wise copy
    int equal = (s1.id == s3.id && strcmp(s1.name, s3.name) == 0);
    printf("s1 and s3 equal: %d\n", equal);
    return 0;
}```


## Part C Answers

### Q8. Illustrate computer with a neat and clean diagram. Explain their functional units in detail. (15 Marks)
Diagram image - https://imgs.search.brave.com/jg3xtdAWAtXTWx5TW8LlWQCyMaMLt7tB0vXzLZ2Ybcs/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9pbWFn/ZXMuZWRyYXdzb2Z0/LmNvbS9hcnRpY2xl/cy9ibG9jay1kaWFn/cmFtLW9mLWNvbXB1/dGVyL2Jsb2NrLWRp/YWdyYW0tb2YtYS1j/b21wdXRlci5wbmc
A computer is an electronic device that processes data based on user instructions, and its structure can be illustrated with a neat block diagram. Picture a central **Central Processing Unit (CPU)** connected to **Memory (RAM and ROM)**, **Input Devices** (e.g., keyboard, mouse), **Output Devices** (e.g., monitor, printer), and **Storage Devices** (e.g., hard drives, SSDs), all linked via a **Motherboard**. Arrows indicate the data flow between these components, starting from input, processed by the CPU, stored or displayed as output.

The functional units are the backbone of this system:
- **Input Unit**: This unit includes peripherals like the keyboard and mouse, which allow users to feed data or commands. The data is converted into a binary format and sent to the CPU for processing, forming the first step in the computing cycle.
- **Central Processing Unit (CPU)**: Known as the computer’s brain, it comprises the Arithmetic Logic Unit (ALU) for performing calculations and logical operations, and the Control Unit (CU) for managing the fetch-decode-execute cycle. It coordinates all activities, making it the core processing element.
- **Memory Unit**: This includes RAM (volatile, used for temporary storage during program execution) and ROM (non-volatile, containing permanent instructions like BIOS). RAM speeds up processing by holding active data, while ROM ensures the system boots correctly.
- **Output Unit**: Devices such as monitors and printers receive processed data from the CPU and present it to the user. This unit completes the cycle by providing tangible or visual results.
- **Storage Unit**: Hard drives or SSDs provide long-term data storage, retaining files and programs even when the power is off. This unit supports data persistence, complementing the temporary nature of RAM.

Together, these units enable the computer to perform complex tasks efficiently, from data input to final output, making it an indispensable tool in modern technology.

---

### Q9. What is the difference between algorithm, pseudocode, and flow chart? Draw a flow chart to check if a number is prime or not. (15 Marks)
An algorithm, pseudocode, and flow chart are essential tools in problem-solving and programming, each serving a distinct purpose. An **algorithm** is a step-by-step procedure or set of rules to solve a problem, written in a logical sequence using natural language or basic constructs. It focuses on the logic and flow without syntax, acting as a foundation for coding. **Pseudocode**, on the other hand, is a more structured, human-readable representation of an algorithm, blending natural language with programming-like syntax (e.g., loops, conditionals) but not executable. It bridges the gap between algorithm and code. A **flow chart** is a graphical representation using symbols like ovals (start/end), rectangles (process), diamonds (decisions), and arrows (flow), visually depicting the algorithm’s logic for better understanding.

**Differences:**
- **Purpose**: An algorithm defines the solution logic, pseudocode refines it into a code-like format, and a flow chart provides a visual overview.
- **Format**: Algorithms are text-based with steps, pseudocode uses semi-structured text, and flow charts use diagrams.
- **Usage**: Algorithms are abstract, pseudocode is a planning tool, and flow charts aid in debugging or explanation.

``` diagram link  : https://imgs.search.brave.com/0Hl8KC7img-GUi-FbCy3rV_u0Yqs8TospQXrvM9MNYw/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly93d3cu/dzNyZXNvdXJjZS5j/b20vdzNyX2ltYWdl/cy9jLWZvci1sb29w/LWV4ZXJjaXNlLTMy/LnBuZw ```

### Q11. What is a pointer? Write a C program to read a set of strings and sort them in alphabetical order. Explain declaration and initialization of array of strings. (15 Marks)
- A pointer in C is a variable that stores the memory address of another variable, enabling direct memory access and manipulation. It’s declared with an asterisk (*), e.g., int *ptr, and is powerful for dynamic memory allocation, passing large data efficiently, and array handling. Dereferencing (*ptr) accesses the value at that address.
Program to Read and Sort Strings Alphabetically:
c
``` #include <stdio.h>
#include <string.h>
int main() {
    int n, i, j;
    printf("Enter the number of strings: ");
    scanf("%d", &n);
    char str[100][50]; // Array to hold strings
    printf("Enter %d strings:\n", n);
    for (i = 0; i < n; i++) scanf("%s", str[i]);
    // Bubble sort for strings
    for (i = 0; i < n - 1; i++)
        for (j = 0; j < n - i - 1; j++)
            if (strcmp(str[j], str[j + 1]) > 0) {
                char temp[50];
                strcpy(temp, str[j]);
                strcpy(str[j], str[j + 1]);
                strcpy(str[j + 1], temp);
            }
    printf("Sorted strings:\n");
    for (i = 0; i < n; i++) printf("%s\n", str[i]);
    return 0;
}```

- This program uses strcmp to compare strings and swaps them using a temporary array, sorting them alphabetically.
- Declaration and Initialization of Array of Strings:
An array of strings is a 2D array where each element is a string (array of characters). It’s declared as char str[row][col], where row is the number of strings and col is the maximum length of each string (plus 1 for the null terminator).

Declaration: char str[5][20]; creates an array for 5 strings, each up to 19 characters.

Initialization: 
Direct: char str[3][10] = {"apple", "banana", "cherry"}; (remaining elements auto-filled with null).

Partial: char str[3][10] = {"apple"}; (others set to empty strings).

Runtime: Use loops with scanf to input values, as shown in the program.
This structure is useful for handling multiple strings, with memory allocated contiguously for efficient access.

