All Answers (Part A, Part B, and Part C)
Part A Answers
Q1. (a) Write a short note on type casting.
Type casting is the process of converting a variable from one data type to another. It can be explicit (using casting operators like (float)) or implicit (automatic by the compiler).
Example: Converting an int to a float using (float).

Q1. (b) Define relational operator?
A relational operator compares two values and returns a boolean result (true or false). Common examples include ==, !=, <, >, <=, and >=. They are used in decision-making statements like if conditions.

Q1. (c) Write and explain syntax of --for-- and do-while loop.
For loop syntax: for (initialization; condition; increment) { statement; } - This loop executes a block of code repeatedly until the condition becomes false.

Do-while loop syntax: do { statement; } while (condition); - This loop executes the block at least once, then repeats if the condition is true.
Example: for (i = 0; i < 5; i++) vs. do { i++; } while (i < 5).

Q1. (d) Distinguish between while and do-while statements.
The while loop checks the condition before execution, so the loop may not run if the condition is false initially.

The do-while loop executes the block once before checking the condition, ensuring at least one execution.
Example: while (i < 0) vs. do { i++; } while (i < 0).

Q1. (e) What is pseudocode?
Pseudocode is a high-level, informal description of a program using natural language and programming constructs. It is not executable but helps in planning and designing algorithms.
Example: "Start, set x = 0, while x < 10, print x, increment x, end."

Q1. (f) Write different notations in flow chart.
Common flowchart notations include ovals (start/end), rectangles (process), diamonds (decision), and arrows (flow direction). They are used to visually represent the logic and sequence of a program.
Example: Oval for "Start", Diamond for "Is x > 0?".

Q1. (g) How to declare and initialize flow chart.
You "draw" or "construct" a flowchart rather than declare and initialize it. You start with an oval ("Start") and end with an oval ("End"). You then add process boxes (rectangles) and decision diamonds with appropriate arrows to show the flow.
Example: Start → Process "Set x = 0" → End.

Q1. (h) What is #include, #define
#include is a preprocessor directive used to include header files (e.g., #include <stdio.h>).

#define is used to define constants or macros (e.g., #define MAX 100).
Both are processed before compilation.

Q1. (i) Write and explain the directives.
Directives like #include and #define instruct the compiler on pre-processing tasks.

#include adds external code from header files.

#define substitutes text (defines symbolic constants or macros).
Example: #define PI 3.14 replaces PI with 3.14 in the code.

Q1. (j) Define pointer array syntax of function?
A pointer array holds addresses of variables. Syntax: int *arr[5]; (an array of 5 integer pointers).

Function syntax with a pointer array parameter: void func(int *arr[]) (pass an array of pointers).
Used for dynamic memory or multi-dimensional data handling.

Q1. (k) What is array of strings?
An array of strings is an array where each element is a string (which is an array of characters).
Syntax: char str[5][10]; (meaning 5 strings, each up to 9 characters + null terminator).
Example: str[0] = "hello"; (using strcpy is required for assignment).

Q1. (l) Discriminate putc() and gets()
putc() writes a single character to a file. Syntax: putc(ch, fp);.

gets() reads a string from standard input. Syntax: gets(str); (Note: gets() is now deprecated and unsafe; fgets() is preferred).
The main difference is putc is character-based, while gets is string-based.

Q1. (m) How can you compare two strings?
You compare strings using strcmp(str1, str2) from <string.h>. It returns 0 if the strings are equal, a negative value if str1 is lexicographically less than str2, and a positive value if str1 is lexicographically greater than str2.
Example: if (strcmp(str1, str2) == 0).

Q1. (n) Define Data Types in C.
Data types in C define the type of data a variable can hold (e.g., int, float, char), its memory size, and its range of values. They include primitive types (like int, char) and derived types (like array, pointer, struct).
Example: int x = 10; declares an integer.

Part B Answers
Q2. Write the structure of C program and explain. Write a program to perform swapping of two numbers without using temporary variable.
A C program typically follows a structured format that includes several key sections. It begins with preprocessor directives like #include <stdio.h> to include necessary header files for input/output operations. Next, the main() function serves as the entry point where the program execution starts, enclosed within curly braces {}. Inside main(), global and local variables are declared, followed by the program logic implemented using statements, loops, or conditionals. The program ends with a return statement, usually return 0, to indicate successful execution. Comments can be added using // or /* */ for clarity.

Here’s an explanation of a program to swap two numbers without a temporary variable, which uses arithmetic operations. Consider two variables, a and b. The swapping can be done by adding a and b and storing the sum in a, then subtracting the original b from this sum to get the new a, and finally subtracting the new a from the sum to get the new b. This method avoids using extra memory.

Program Example:

#include <stdio.h>

int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("Before swapping: a = %d, b = %d\n", a, b);

    a = a + b;  // Step 1: Add both numbers. 'a' now holds (original a + original b)
    b = a - b;  // Step 2: Subtract original b from sum. 'b' now holds (original a)
    a = a - b;  // Step 3: Subtract (original a) from sum. 'a' now holds (original b)

    printf("After swapping: a = %d, b = %d\n", a, b);
    return 0;
}

Q3. Define algorithm and Pseudocode. Write algorithm and pseudocode for finding factorial of a number.
An algorithm is a step-by-step procedure or set of rules to solve a problem or complete a task, expressed in a logical sequence. It acts as a blueprint for programming, ensuring clarity before coding. Pseudocode, on the other hand, is a high-level, human-readable description of an algorithm using a mix of natural language and programming constructs, without strict syntax rules. It helps plan the logic and is later translated into actual code.

Algorithm for Factorial of a Number:

Start.

Input a non-negative number n.

Initialize a variable fact to 1.

Check if n is less than 0:

If yes, display "Factorial not defined for negative numbers" and Stop.

Else (if n is 0 or positive):

Loop for each integer i from 1 to n:

Multiply fact by i (fact = fact * i).

After the loop, fact contains the factorial of n.

Display fact.

Stop.

Pseudocode for Factorial of a Number:

BEGIN
    INPUT n
    SET fact = 1

    IF n < 0 THEN
        PRINT "Error: Factorial not defined for negative numbers."
    ELSE IF n == 0 THEN
        PRINT "The factorial of 0 is 1."
    ELSE
        FOR i FROM 1 TO n DO
            SET fact = fact * i
        END FOR
        PRINT "The factorial of", n, "is", fact
    END IF
END

Q4. Explain various branching statements in C with examples. Write a program to generate prime numbers between 1 and n (given by user).
Branching statements in C control the flow of execution based on conditions. The primary ones are if, if-else, else-if ladder, and switch.

The if statement executes a block if a condition is true.

The if-else adds an alternative block for a false condition.

The else-if ladder handles multiple conditions sequentially.

The switch statement selects a case based on a value.

These statements are crucial for decision-making.

Examples of Branching:

if (a > b) printf("a is greater"); - Simple if.

if (a > b) printf("a is greater"); else printf("b is greater"); - if-else.

switch (day) { case 1: printf("Monday"); break; } - switch.

Program to Generate Prime Numbers:

#include <stdio.h>

int main() {
    int n;           // User-defined upper limit
    int i, j;        // Loop counters
    int isPrime;     // Flag to check if a number is prime (1 for prime, 0 for not prime)

    printf("Enter a number (n) to find prime numbers up to: ");
    scanf("%d", &n);

    if (n < 2) {
        printf("There are no prime numbers up to %d.\n", n);
        return 0;
    }

    printf("Prime numbers between 1 and %d are: ", n);

    // Loop through numbers from 2 to n
    for (i = 2; i <= n; i++) {
        isPrime = 1; // Assume current number 'i' is prime

        // Check for divisibility from 2 up to sqrt(i) for efficiency
        for (j = 2; j * j <= i; j++) {
            if (i % j == 0) { // If 'i' is divisible by 'j', it's not prime
                isPrime = 0; // Set flag to 0 (not prime)
                break;       // No need to check further divisors, break inner loop
            }
        }

        // If isPrime is still 1, then 'i' is a prime number
        if (isPrime) {
            printf("%d ", i);
        }
    }
    printf("\n"); // Newline for better formatting

    return 0;
}

Q5. Define an array. How to initialize one-dimensional array? Explain with suitable examples. Write a C program to sort the given array elements in Ascending order.
An array is a collection of elements of the same data type stored in contiguous memory locations, accessed using an index. It allows efficient data handling for multiple values under a single name. A one-dimensional array is a linear list, declared with a fixed size, e.g., int arr[5];.

Initialization of One-Dimensional Array:

Direct initialization: int arr[5] = {1, 2, 3, 4, 5};

Partial initialization: int arr[5] = {1, 2}; (remaining elements set to 0).

At runtime (user input): scanf("%d", &arr[i]); to input values into elements.

Program to Sort Array in Ascending Order (Bubble Sort):

#include <stdio.h>

int main() {
    int arr[100], n, i, j, temp;
    printf("Enter the size of array: ");
    scanf("%d", &n);

    printf("Enter %d integer elements:\n", n);
    for (i = 0; i < n; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", &arr[i]);
    }

    // --- Bubble Sort Algorithm for Ascending Order ---
    // Outer loop for passes (n-1 passes needed for n elements)
    for (i = 0; i < n - 1; i++) {
        // Inner loop for comparisons and swaps in each pass
        // The last i elements are already in place, so no need to compare them
        for (j = 0; j < n - i - 1; j++) {
            // Compare adjacent elements
            if (arr[j] > arr[j + 1]) {
                // Swap if the current element is greater than the next
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    // Print the sorted array
    printf("\nArray elements in Ascending Order: ");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}

Q6. What are the features of pointers? Write a C program to print address of a variable.
Pointers are variables that store memory addresses of other variables, enabling direct memory manipulation. Key features include:

They allow dynamic memory allocation.

Provide efficiency in passing large data structures to functions.

Enable array handling by treating array names as pointers.

Support pointer arithmetic for traversing memory.

Require careful use to avoid issues like dangling pointers or memory leaks.

Program to Print Address of a Variable:

#include <stdio.h> // Required for printf()

int main() {
    int x = 10;       // Declare an integer variable 'x' and initialize it
    int *ptr = &x;    // Declare an integer pointer 'ptr' and store the address of 'x' in it

    // Print the value of the variable 'x'
    printf("Value of x: %d\n", x);

    // Print the memory address of 'x' using the address-of operator (&)
    // %p is the format specifier for printing addresses.
    printf("Address of x (using &x): %p\n", (void*)&x);

    // Print the memory address stored in the pointer 'ptr'
    printf("Address stored in ptr: %p\n", (void*)ptr);

    // Print the value of 'x' by dereferencing the pointer 'ptr'
    // The dereference operator (*) retrieves the value at the address pointed to.
    printf("Value accessed via pointer (*ptr): %d\n", *ptr);

    return 0; // Indicate successful execution
}

Q7. Define Structure and write the general syntax for declaring and accessing members. How to copy and compare structure variables? Illustrate with example.
A structure in C is a user-defined data type that groups different data types under a single name, allowing complex data representation.

General Syntax:

Declaration:

struct struct_name {
    data_type member1;
    data_type member2;
    // ...
}; // Semicolon is essential here

Accessing members:

Using the dot operator (.) for structure variables: variableName.member1 = value;

Using the arrow operator (->) for pointers to structures: pointerToStruct->member1 = value;

Example Structure Definition:

struct Student {
    int id;
    char name[20];
    float gpa;
};

Copying Structure Variables:
Structures can be copied by assignment (=), which performs a member-wise copy of all fields.

Comparing Structure Variables:
Direct comparison (==) is not allowed for entire structures. You must compare members individually.

Example Program (Copying and Comparing Structures):

#include <stdio.h>
#include <string.h> // For strcpy and strcmp

struct Student {
    int id;
    char name[20];
};

int main() {
    struct Student s1 = {1, "Alice"}; // Initialize s1
    struct Student s2;                // Declare s2
    struct Student s3;                // Declare s3

    // --- Copying s1 to s2 by assignment ---
    s2 = s1;
    printf("s2 after assignment from s1: ID=%d, Name=%s\n", s2.id, s2.name);

    // --- Member-wise copy from s1 to s3 ---
    s3.id = s1.id;
    strcpy(s3.name, s1.name); // Use strcpy for string members
    printf("s3 after member-wise copy from s1: ID=%d, Name=%s\n", s3.id, s3.name);

    // --- Comparing s1 and s3 members individually ---
    int are_equal = (s1.id == s3.id && strcmp(s1.name, s3.name) == 0);
    if (are_equal) {
        printf("s1 and s3 are identical (compared member-wise).\n");
    } else {
        printf("s1 and s3 are different.\n");
    }

    return 0;
}

Part C Answers
Q8. Illustrate computer with a neat and clean diagram. Explain their functional units in detail. (15 Marks)
A computer is an electronic device that processes data based on user instructions. Its fundamental architecture involves several interconnected functional units that work together to perform computing tasks.

Block Diagram of a Computer System
                      +-------------------+
                      |   Input Devices   |
                      | (Keyboard, Mouse) |
                      +---------+---------+
                                |
                                | Data/Instructions Flow
                                V
                      +-------------------+
                      |                   |
                      |   Memory Unit     |
                      | (RAM, ROM, Cache) |
                      |                   |
                      +---------+---------+
                                |
                                | Data/Instructions Flow
                                V
    +-------------------------------------------------------+
    |                        CPU                            |
    |  +----------------+   +----------------+   +--------+  |
    |  | Arithmetic Logic |   | Control Unit   |   | Registers|  |
    |  |  Unit (ALU)    |   |     (CU)       |   |          |  |
    |  +----------------+   +----------------+   +--------+  |
    |            |                   |                         |
    +-------------------------------------------------------+
                                |
                                | Processed Data Flow
                                V
                      +-------------------+
                      |                   |
                      |   Output Devices  |
                      | (Monitor, Printer)|
                      |                   |
                      +---------+---------+
                                |
                                V
                      +-------------------+
                      |                   |
                      | Storage Devices   |
                      | (HDD, SSD, USB)   |
                      |                   |
                      +-------------------+

Functional Units in Detail
The main functional units of a computer system are:

Input Unit:

Purpose: To accept data and instructions from the user or external sources and convert them into a machine-readable format (binary).

Components: Devices like a keyboard, mouse, scanner, microphone, and webcam.

Functionality: It acts as an interface between the user and the computer, allowing data entry and commands to be transformed into digital signals for processing.

Central Processing Unit (CPU):

Purpose: Often called the "brain" of the computer, it executes instructions, performs calculations, and manages all other components.

Sub-units:

Arithmetic Logic Unit (ALU): Performs all arithmetic operations (addition, subtraction, etc.) and logical operations (comparisons like AND, OR).

Control Unit (CU): Directs and coordinates all operations within the computer. It fetches instructions, decodes them, and directs other units to perform tasks.

Registers: Small, high-speed storage locations within the CPU that temporarily hold data and instructions during immediate processing.

Memory Unit:

Purpose: To store data and instructions for the CPU to access quickly.

Types:

Random Access Memory (RAM): Volatile memory used for temporary storage of programs and data currently being executed. Its contents are lost when power is off.

Read-Only Memory (ROM): Non-volatile memory that stores permanent instructions, such as the BIOS, essential for booting the computer.

Cache Memory: A small, very fast memory between the CPU and RAM, storing frequently accessed data to speed up processing.

Output Unit:

Purpose: To present the processed data from the computer to the user in a human-understandable form.

Components: Devices such as a monitor, printer, and speakers.

Functionality: It converts digital information back into visual, audio, or tactile output.

Storage Unit (Secondary Storage):

Purpose: To provide long-term, non-volatile storage for programs and data, retaining information even when the computer is off.

Components: Hard Disk Drives (HDD), Solid State Drives (SSD), and USB flash drives.

Functionality: This unit stores the operating system, applications, and user files permanently.

Together, these units enable the computer to perform complex tasks efficiently, from data input to final output, making it an indispensable tool in modern technology.

Q9. What is the difference between algorithm, pseudocode, and flow chart? Draw a flow chart to check if a number is prime or not. (15 Marks)
An algorithm, pseudocode, and flowchart are all essential tools in problem-solving and programming, each serving a distinct purpose in the design phase.

Differences:

Feature

Algorithm

Pseudocode

Flowchart

Purpose

Defines the core logical steps to solve a problem.

Refines algorithm logic into a code-like, human-readable format.

Provides a visual representation of the algorithm's flow.

Format

Text-based, sequential steps (e.g., numbered list).

Text-based, informal syntax mixing natural language with programming constructs.

Graphical, using standard symbols (shapes) and connecting arrows.

Level of Detail

Abstract, conceptual; focuses on "what to do."

More specific than an algorithm; closer to actual code but without strict syntax.

Visually detailed, clearly showing sequence, decisions, and loops.

Executable?

No.

No.

No (but can be easily converted to code).

Best Used For

Initial problem analysis and logical sequencing.

Planning code logic, communication between programmers.

Visualizing logic, debugging, documentation, presenting to non-technical users.

Flowchart to Check if a Number is Prime or Not
A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself.

graph TD
    A[Start] --> B(Input N);

    B --> C{Is N <= 1?};
    C -- Yes --> D[Print "N is not prime"];
    D --> E[End];

    C -- No --> F{Is N == 2?};
    F -- Yes --> G[Print "N is prime"];
    G --> E;

    F -- No --> H{Initialize i = 2, isPrime = True};

    H --> I{Is i * i <= N?};
    I -- Yes --> J{Is N % i == 0?};
    J -- Yes --> K[Set isPrime = False];
    K --> L[Break loop, set i = N + 1]; // Simulate break
    L --> M{Is isPrime == True?};

    J -- No --> N[Increment i];
    N --> I;

    I -- No --> M; // Loop finished without finding a divisor

    M -- Yes --> O[Print "N is prime"];
    O --> E;

    M -- No --> P[Print "N is not prime"];
    P --> E;

Explanation of Flowchart Symbols:

Oval: Marks the Start and End of the process.

Parallelogram: Indicates Input or Output operations.

Rectangle: Represents a Process or an action (e.g., initialization, assignment).

Diamond: Denotes a Decision point where a condition is evaluated, leading to different paths.

Arrows: Show the flow of control between steps.

Q10. Define Function. Explain user defined and built-in functions with example. Also, differentiate between call by value and call by reference with suitable example. (15 Marks)
Definition of Function
A function in C is a self-contained block of code designed to perform a specific task. It enhances code reusability, modularity, and makes programs easier to understand, debug, and maintain. Functions typically take input (arguments), perform operations, and may return a value.

Types of Functions in C
1. User-Defined Functions
Definition: These are functions created by the programmer to perform specific tasks tailored to the application's needs. They encapsulate particular logic and can be called multiple times.

Example:

#include <stdio.h>

// User-defined function to add two integers
int add(int num1, int num2) {
    int sum;
    sum = num1 + num2;
    return sum; // Returns the calculated sum
}

int main() {
    int a = 5, b = 3;
    int result;
    result = add(a, b); // Calling the user-defined 'add' function
    printf("The sum of %d and %d is: %d\n", a, b, result);
    return 0;
}

Here, add is a user-defined function that calculates the sum of two numbers.

2. Built-in Functions (Library Functions)
Definition: These are pre-defined functions that are part of the C standard library. They provide common functionalities and are ready to use by simply including the appropriate header file.

Example:

#include <stdio.h>  // For printf()
#include <string.h> // For strlen()

int main() {
    char myString[] = "hello";
    // strlen() is a built-in function from <string.h>
    printf("Length of string \"%s\": %zu\n", myString, strlen(myString));
    // printf() is a built-in function from <stdio.h>
    return 0;
}
```strlen` and `printf` are examples of built-in functions.


Call by Value vs. Call by Reference
These are two different methods for passing arguments to a function, affecting how changes inside the function impact the original variables.

1. Call by Value
Mechanism: A copy of the argument's value is passed to the function's formal parameters.

Effect: Changes made to the formal parameters inside the function do not affect the original variables in the calling function, as the function operates on a separate copy.

Use Case: When you want the function to work with data without altering the original values.

Example (Call by Value):

#include <stdio.h>

void modifyValue(int x) {
    x = 20; // This changes only the local copy of x
    printf("Inside modifyValue (local x): %d\n", x);
}

int main() {
    int a = 10;
    printf("Before calling modifyValue: a = %d\n", a);
    modifyValue(a); // Pass the value of 'a' (a copy)
    printf("After calling modifyValue: a = %d\n", a); // 'a' remains 10
    return 0;
}

2. Call by Reference
Mechanism: The memory address (or reference) of the argument is passed to the function. The formal parameter becomes a pointer that points to the original variable.

Effect: Changes made to the variable through the pointer inside the function directly affect the original variable in the calling function.

Use Case: When you need a function to modify the original variables or when passing large data structures to avoid copying overhead.

Example (Call by Reference):

#include <stdio.h>

void modifyReference(int *ptr) { // 'ptr' receives the address of 'a'
    *ptr = 20; // Dereference 'ptr' to change the value at 'a's address
    printf("Inside modifyReference (value via ptr): %d\n", *ptr);
}

int main() {
    int a = 10;
    printf("Before calling modifyReference: a = %d\n", a);
    modifyReference(&a); // Pass the address of 'a'
    printf("After calling modifyReference: a = %d\n", a); // 'a' is now 20
    return 0;
}

The key difference lies in whether the function operates on a copy of the data or directly on the original data in memory.

Q11. What is a pointer? Write a C program to read a set of strings and sort them in alphabetical order. Explain declaration and initialization of array of strings. (15 Marks)
A pointer in C is a variable that stores the memory address of another variable. Instead of holding a data value directly, it holds the location where a data value of a specific type is stored. Pointers are powerful for dynamic memory allocation, efficient function argument passing, and flexible array manipulation.

Program to Read a Set of Strings and Sort Them in Alphabetical Order
This program uses a 2D character array to store strings and then employs the Bubble Sort algorithm with strcmp (for comparison) and strcpy (for swapping) to sort them alphabetically.

#include <stdio.h>
#include <string.h> // Required for strcmp() and strcpy()

int main() {
    int n; // Number of strings
    int i, j; // Loop counters

    printf("Enter the number of strings you want to sort: ");
    scanf("%d", &n);

    // Declare a 2D array to hold strings:
    // 100 rows (max 100 strings), 50 columns (max 49 chars + null terminator per string)
    char str[100][50];
    char temp[50]; // Temporary array for swapping strings

    // Consume the newline character left by previous scanf
    // This is important before reading strings with fgets() in a loop
    while (getchar() != '\n'); 

    printf("Enter %d strings (each max 49 characters):\n", n);
    for (i = 0; i < n; i++) {
        printf("String %d: ", i + 1);
        // Using fgets for safer string input (prevents buffer overflow)
        fgets(str[i], sizeof(str[i]), stdin);
        str[i][strcspn(str[i], "\n")] = 0; // Remove trailing newline from fgets
    }

    // --- Bubble Sort for Strings ---
    // Outer loop for passes
    for (i = 0; i < n - 1; i++) {
        // Inner loop for comparisons in each pass
        for (j = 0; j < n - i - 1; j++) {
            // strcmp returns > 0 if str[j] is lexicographically greater than str[j+1]
            if (strcmp(str[j], str[j + 1]) > 0) {
                // Swap strings using strcpy
                strcpy(temp, str[j]);
                strcpy(str[j], str[j + 1]);
                strcpy(str[j + 1], temp);
            }
        }
    }

    printf("\nSorted strings in alphabetical order:\n");
    for (i = 0; i < n; i++) {
        printf("%s\n", str[i]);
    }

    return 0;
}

Explanation of Declaration and Initialization of Array of Strings
An array of strings is essentially a two-dimensional array of characters where each row represents a string, and the string itself is terminated by a null character (\0).

1. Declaration:
You declare an array of strings by specifying the number of strings (rows) and the maximum length of each string (columns, including the null terminator).

Syntax:
char arrayName[number_of_strings][max_length_of_each_string + 1];

Example:

char names[5][20];

This declares an array called names that can store 5 strings. Each of these 5 strings can have a maximum length of 19 characters (plus 1 character for the null terminator \0).

2. Initialization:
You can initialize an array of strings at the time of declaration or at runtime.

Direct Initialization (at Declaration Time):
You provide a list of string literals enclosed in curly braces. The compiler automatically adds the null terminators.

char colors[3][10] = {"Red", "Green", "Blue"};
// This creates:
// colors[0] = "Red\0"
// colors[1] = "Green\0"
// colors[2] = "Blue\0"

You can also omit the number of strings, and the compiler will deduce it from the initializers:

char cities[][15] = {"Delhi", "Mumbai", "Kolkata"}; // Number of strings (rows) will be 3

Initialization at Runtime (User Input):
You read strings from the user, typically using a loop with scanf() or fgets(). It's crucial to use strcpy() when assigning a new string value to an array element after declaration, as direct assignment (str[i] = "new string";) is not allowed for character arrays.

#include <stdio.h>
#include <string.h> // For strcpy

int main() {
    char names[2][20]; // Declare an array for 2 names, each up to 19 chars

    printf("Enter first name: ");
    scanf("%s", names[0]); // Read into the first string (row 0)

    printf("Enter second name: ");
    scanf("%s", names[1]); // Read into the second string (row 1)

    printf("Names: %s, %s\n", names[0], names[1]);

    // To assign a new value to an existing string in the array:
    strcpy(names[0], "UpdatedName");
    printf("Updated first name: %s\n", names[0]);

    return 0;
}

It's generally safer to use fgets() for input to prevent buffer overflows, as shown in the sorting program example, and then remove the trailing newline character fgets often includes.
