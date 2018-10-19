###### 1.1
Use a building-block approach to creating your programs. Avoid reinventing the wheel— use existing high-quality pieces wherever possible. Such software reuse is a key benefit of object-oriented programming.
###### 3.1
A compound statement can be placed anywhere in a program that a single statement can be placed.
###### 3.2
Each refinement, as well as the top itself, is a complete specification of the algorithm; only the level of detail varies.
###### 3.3
Many programs can be divided logically into three phases: an initialization phase that initializes the program variables; a processing phase that inputs data values and adjusts program variables accordingly; and a termination phase that calculates and prints the final results.
###### 3.4
You terminate the top-down, stepwise refinement process when the pseudocode algorithm is specified in sufficient detail for you to be able to convert the pseudocode to C. Implementing the C program is then normally straightforward.
###### 3.5
Experience has shown that the most difficult part of solving a problem on a computer is developing the algorithm for the solution. Once a correct algorithm has been specified, the process of producing a working C program is normally straightforward.
###### 3.6
Many programmers write programs without ever using program-development tools such as pseudocode. They feel that their ultimate goal is to solve the problem on a computer and that writing pseudocode merely delays the production of final outputs.
###### 4.1
Place only expressions involving the control variables in the initialization and increment sections of a for statement. Manipulations of other variables should appear either before the loop (if they execute only once, like initialization statements) or in the loop body (if they execute once per iteration, like incrementing or decrementing statements).
###### 4.2
Type double is a floating-point type like float, but typically a variable of type double can store a value of much greater magnitude with greater precision than float. Variables of type double occupy more memory than those of type float. For all but the most memory-intensive applications, professional programmers generally prefer double to float.
###### 4.3
Some programmers feel that break and continue violate the norms of structured programming. The effects of these statements can be achieved by structured programming techniques we’ll soon discuss, so these programmers do not use break and continue.
###### 4.4
There’s a tension between achieving quality software engineering and achieving the bestperforming software. Often one of these goals is achieved at the expense of the other. For all but the most performance-intensive situations, apply the following guidelines: First, make your code simple and correct; then make it fast and small, but only if necessary.
###### 5.1
Avoid reinventing the wheel. When possible, use C standard library functions instead of writing new functions. This can reduce program development time. These functions are written by experts, well-tested and efficient.
###### 5.2
In programs containing many functions, main is often implemented as a group of calls to functions that perform the bulk of the program’s work.
###### 5.3
Each function should be limited to performing a single, well-defined task, and the function name should express that task. This facilitates abstraction and promotes software reusability.
###### 5.4
If you cannot choose a concise name that expresses what the function does, it’s possible that your function is attempting to perform too many diverse tasks. It’s usually best to break such a function into smaller functions—this is sometimes called decomposition.
###### 5.5
Small functions promote software reusability.
###### 5.6
Programs should be written as collections of small functions. This makes programs easier to write, debug, maintain and modify.
###### 5.7
A function requiring a large number of parameters may be performing too many tasks. Consider dividing the function into smaller functions that perform the separate tasks. The function header should fit on one line if possible.
###### 5.8
The function prototype, function header and function calls should all agree in the number, type, and order of arguments and parameters, and in the type of return value.
###### 5.9
A function prototype placed outside any function definition applies to all calls to the function appearing after the function prototype in the file. A function prototype placed in a function body applies only to calls made in that function.
###### 5.10
Defining a variable as global rather than local allows unintended side effects to occur when a function that does not need access to the variable accidentally or maliciously modifies it. In general, global variables should be avoided except in certain situations with unique performance requirements (as discussed in Chapter 14).
###### 5.11
Variables used only in a particular function should be defined as local variables in that function rather than as external variables.
###### 5.12
Any problem that can be solved recursively can also be solved iteratively (nonrecursively). A recursive approach is normally chosen in preference to an iterative approach when the recursive approach more naturally mirrors the problem and results in a program that’s easier to understand and debug. Another reason to choose a recursive solution is that an iterative solution may not be apparent.
###### 6.1
Defining the size of each array as a symbolic constant makes programs more modifiable.
###### 6.2
It’s possible to pass an array by value (by placing it in a struct as we explain in Chapter 10, C Structures, Unions, Bit Manipulation and Enumerations).
###### 6.3
The const type qualifier can be applied to an array parameter in a function definition to prevent the original array from being modified in the function body. This is another example of the principle of least privilege. A function should not be given the capability to modify an array in the caller unless it’s absolutely necessary.
###### 7.1
The const qualifier can be used to enforce the principle of least privilege in software design. This can reduce debugging time and prevent unintentional side effects, making a program easier to modify and maintain.
###### 7.2
Placing function prototypes in the definitions of other functions enforces the principle of least privilege by restricting proper function calls to the functions in which the prototypes appear.
###### 7.3
When passing an array to a function, also pass the size of the array. This helps make the function reusable in many programs.
###### 7.4
Global variables usually violate the principle of least privilege and can lead to poor software engineering. Global variables should be used only to represent truly shared resources, such as the time of day.
###### 10.1
As with a struct definition, a union definition simply creates a new type. Placing a union or struct definition outside any function does not create a global variable.
###### 13.1
Using symbolic constants makes programs easier to modify. Rather than search for every occurrence of a value in your code, you modify a symbolic contant once in its #define directive. When the program is recompiled, all occurrences of that constant in the program are modified accordingly.
###### 13.2
Assertions are not meant as a substitute for error handling during normal runtime conditions. Their use should be limited to finding logic errors during program development.
###### 14.1
Global variables should be avoided unless application performance is critical because they violate the principle of least privilege.
###### 14.2
Creating programs in multiple source files facilitates software reusability and good software engineering. Functions may be common to many applications. In such instances, those functions should be stored in their own source files, and each source file should have a corresponding header file containing function prototypes. This enables programmers of different applications to reuse the same code by including the proper header file and compiling their applications with the corresponding source file.
###### 14.3
The goto statement is unstructured and can lead to programs that are more difficult to debug, maintain and modify.
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
###### 
