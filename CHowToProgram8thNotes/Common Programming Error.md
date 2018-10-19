###### 1.1
Errors such as division-by-zero occur as a program runs, so they are called runtime errors or execution-time errors. Divide-by-zero is generally a fatal error, i.e., one that causes the program to terminate immediately without successfully performing its job. Nonfatal errors allow programs to run to completion, often producing incorrect results.
###### 2.1
Mistyping the name of the output function printf as print in a program.
###### 2.2
Using a capital letter where a lowercase letter should be used (for example, typing Main instead of main).
###### 2.3
A calculation in an assignment statement must be on the right side of the = operator. It’s a compilation error to place a calculation on the left side of an assignment operator.
###### 2.4
Forgetting to precede a variable in a scanf statement with an ampersand (&) when that variable should, in fact, be preceded by an ampersand results in an execution-time error. On many systems, this causes a “segmentation fault” or “access violation.” Such an error occurs when a user’s program attempts to access a part of the computer’s memory to which it does not have access privileges. The precise cause of this error will be explained in Chapter 7.
###### 2.5
Preceding a variable included in a printf statement with an ampersand when, in fact, that variable should not be preceded by an ampersand.
###### 2.6
An attempt to divide by zero is normally undefined on computer systems and generally re- sults in a fatal error that causes the program to terminate immediately without having successfully performed its job. Nonfatal errors allow programs to run to completion, often producing incorrect results.
###### 2.7
A syntax error occurs if the two symbols in any of the operators ==, !=, >= and <= are sep- arated by spaces.
###### 2.8
Confusing the equality operator == with the assignment operator. To avoid this confusion, the equality operator should be read “double equals” and the assignment operator should be read “gets” or “is assigned the value of.” As you’ll see, confusing these operators may not cause an easy-to-recognize compilation error, but may cause extremely subtle logic errors.
###### 2.9
Placing commas (when none are needed) between conversion specifiers in the format con- trol string of a scanf statement.
###### 2.10
Placing a semicolon immediately to the right of the right parenthesis after the condition in an if statement.
###### 3.1
Placing a semicolon after the condition in an if statement as in if ( grade >= 60 ); leads to a logic error in single-selection if statements and a syntax error in double-selection if statements.
######  3.2
Not providing in the body of a while statement an action that eventually causes the con- dition in the while to become false. Normally, such an iteration structure will never ter- minate—an error called an “infinite loop.”
######  3.3
Spelling a keyword (such as while or if) with any uppercases letters (as in, While or If) is a compilation error. Remember C is case sensitive and keywords contain only lowercase letters.
###### 3.4
If a counter or total isn’t initialized, the results of your program will probably be incorrect. This is an example of a logic error.
###### 3.5
An attempt to divide by zero causes a fatal error.
###### 3.6
Using precision in a conversion specification in the format control string of a scanf state- ment is an error. Precisions are used only in printf conversion specifications.
###### 3.7
Using floating-point numbers in a manner that assumes they’re represented precisely can lead to incorrect results. Floating-point numbers are represented only approximately by most computers.
###### 3.8
Attempting to use the increment or decrement operator on an expression other than a sim- ple variable name is a syntax error, e.g., writing ++(x + 1).
###### 4.1
Floating-point values may be approximate, so controlling counting loops with floating- point variables may result in imprecise counter values and inaccurate termination tests.
###### 4.2
For a control variable defined in a for statement’s header, attempting to access the control variable after the for statement’s closing right brace (}) is a compilation error.
###### 4.3
Using commas instead of semicolons in a for header is a syntax error.
###### 4.4
Forgetting a break statement when one is needed in a switch statement is a logic error.
###### 4.5
Using operator == for assignment or using operator = for equality is a logic error.
###### 5.1
Specifying function parameters of the same type as double x, y instead of double x, dou- ble y results in a compilation error.
###### 5.2
Placing a semicolon after the right parenthesis enclosing the parameter list of a function definition is a syntax error.
###### 5.3
Redefining a parameter as a local variable in a function is a compilation error.
###### 5.4
Defining a function inside another function is a syntax error.
###### 5.5
Forgetting the semicolon at the end of a function prototype is a syntax error.
###### 5.6
Converting from a higher data type in the promotion hierarchy to a lower type can change the data value. Many compilers issue warnings in such cases.
###### 5.7
Assigning a value to an enumeration constant after it has been defined is a syntax error.
###### 5.8
Accidentally using the same name for an identifier in an inner block as is used for an iden- tifier in an outer block, when in fact you want the identifier in the outer block to be active for the duration of the inner block.
###### 5.9
Forgetting to return a value from a recursive function when one is needed.
###### 5.10
Either omitting the base case, or writing the recursion step incorrectly so that it does not converge on the base case, will cause infinite recursion, eventually exhausting memory. This is analogous to the problem of an infinite loop in an iterative (nonrecursive) solution.
###### 5.11
Writing programs that depend on the order of evaluation of the operands of operators oth- er than &&, ||, ?:, and the comma (,) operator can lead to errors because compilers may not necessarily evaluate the operands in the order you expect.
###### 6.1
Forgetting to initialize the elements of an array.
###### 6.2
It’s a syntax error to provide more initializers in an array initializer list than there are elements in the array—for example, int n[3] = {32, 27, 64, 18}; is a syntax error, because there are four initializers but only three array elements.
###### 6.3
Ending a #define or #include preprocessor directive with a semicolon. Remember that preprocessor directives are not C statements.
###### 6.4
Assigning a value to a symbolic constant in an executable statement is a syntax error. The compiler does not reserve space for symbolic constants as it does for variables that hold val- ues at execution time.
###### 6.5
Referring to an element outside the array bounds.
###### 6.6
Assuming that elements of a local static array are initialized to zero every time the func- tion in which the array is defined is called.
###### 6.7
Referencing a two-dimensional array element as a[x, y] instead of a[x][y] is a logic error. C interprets a[x, y] as a[y] (because the comma in this context is treated as a comma operator), so this programmer error is not a syntax error.
###### 7.1
The asterisk (*) notation used to declare pointer variables does not distribute to all vari- able names in a declaration. Each pointer must be declared with the * prefixed to the name; e.g., if you wish to declare xPtr and yPtr as int pointers, use int *xPtr, *yPtr;.
###### 7.2
Dereferencing a pointer that has not been properly initialized or that has not been assigned to point to a specific location in memory is an error. This could cause a fatal execution- time error, or it could accidentally modify important data and allow the program to run to completion with incorrect results.
###### 7.3
Being unaware that a function is expecting pointers as arguments for pass-by-reference and passing arguments by value. Some compilers take the values assuming they’re pointers and dereference the values as pointers. At runtime, memory-access violations or segmen- tation faults are often generated. Other compilers catch the mismatch in types between arguments and parameters and generate error messages.
###### 7.4
Using pointer arithmetic on a pointer that does not refer to an element in an array.
###### 7.5
Running off either end of an array when using pointer arithmetic.
###### 7.6
Subtracting two pointers that do not refer to elements in the same array.
###### 7.7
Assigning a pointer of one type to a pointer of another type if neither is of type void * is a syntax error.
###### 7.8
Dereferencing a void * pointer is a syntax error.
###### 7.9
Comparing two pointers that do not refer to elements in the same array.
###### 7.10
Attempting to modify the value of an array name with pointer arithmetic is a compilation error.
###### 8.1
Not allocating sufficient space in a character array to store the null character that termi- nates a string is an error.
###### 8.2
Printing a “string” that does not contain a terminating null character is an error. Printing will continue past the end of the “string” until a null character is encountered.
###### 8.3
Processing a single character as a string. A string is a pointer—probably a respectably large integer. However, a character is a small integer (ASCII values range 0–255). On many systems this causes an error, because low memory addresses are reserved for special purposes such as operating-system interrupt handlers—so “access violations” occur.
###### 8.4
Passing a character as an argument to a function when a string is expected (and vice versa) is a compilation error.
###### 8.5
Not appending a terminating null character to the first argument of a strncpy when the third argument is less than or equal to the length of the string in the second argument.
###### 8.6
Assuming that strcmp and strncmp return 1 when their arguments are equal is a logic error. Both functions return 0 (strangely, the equivalent of C's false value) for equality. Therefore, when comparing two strings for equality, the result of function strcmp or strncmp should be compared with 0 to determine whether the strings are equal.
###### 8.7
String-manipulation functions other than memmove that copy characters have undefined results when copying takes place between parts of the same string.
###### 9.1
Forgetting to enclose a format-control-string in quotation marks is a syntax error.
###### 9.2
Printing a negative value with a conversion specifier that expects an unsigned value.
###### 9.3
Using %c to print a string is an error. The conversion specifier %c expects a char argument. A string is a pointer to char (i.e., a char *).
###### 9.4
Using %s to print a char argument often causes a fatal execution-time error called an ac- cess violation. The conversion specifier %s expects an argument of type pointer to char.
###### 9.5
Using single quotes around the characters you want to form into a string is a syntax error. Character strings must be enclosed in double quotes.
###### 9.6
Using double quotes around a character constant creates a pointer to a string consisting of two characters, the second of which is the terminating null.
###### 9.7
Trying to print a literal percent character using % rather than %% in the format control string—when % appears in a format control string, it must be followed by a conversion specifier.
###### 9.8
Not providing a sufficiently large field width to handle a value to be printed can offset other data being printed, producing confusing outputs. Know your data!
###### 10.1
Forgetting the semicolon that terminates a structure definition is a syntax error.
###### 10.2
A structure cannot contain an instance of itself.
###### 10.3
Assigning a structure of one type to a structure of a different type is a compilation error.
###### 10.4
Inserting space between the - and > components of the structure pointer operator or be- tween the components of any other multiple-keystroke operator except ?: is a syntax error.
###### 10.5
Attempting to refer to a structure member by using only the member’s name is a syntax error.
###### 10.6
Not using parentheses when referring to a structure member that uses a pointer and the structure member operator (e.g., *cardPtr.suit) is a syntax error. To prevent this prob- lem use the arrow (->) operator instead.
###### 10.7
Assuming that structures, like arrays, are automatically passed by reference and trying to modify the caller’s structure values in the called function is a logic error.
###### 10.8
Forgetting to include the array index when referring to individual structures in an array of structures is a syntax error.
###### 10.9
Referencing data in a union with a variable of the wrong type is a logic error.
###### 10.10
Using the logical AND operator (&&) for the bitwise AND operator (&)—and vice versa— is an error.
###### 10.11
The result of right or left shifting a value is undefined if the right operand is negative or if the right operand is larger than the number of bits in which the left operand is stored.
###### 10.12
Attempting to access individual bits of a bit field as if they were elements of an array is a syntax error. Bit fields are not “arrays of bits.”
###### 10.13
Attempting to take the address of a bit field (the & operator may not be used with bit fields because they do not have addresses).
###### 10.14
Assigning a value to an enumeration constant after it’s been defined is a syntax error.
###### 11.1
Opening an existing file for writing ("w") when, in fact, the user wants to preserve the file, discards the contents of the file without warning.
###### 11.2
Forgetting to open a file before attempting to reference it in a program is a logic error.
###### 11.3
Opening a nonexistent file for reading is an error.
###### 11.4
Opening a file for reading or writing without having been granted the appropriate access rights to the file (this is operating-system dependent) is an error.
###### 11.5
Opening a file for writing when no space is available is a runtime error.
###### 11.6
Opening a file in write mode ("w") when it should be opened in update mode ("r+") causes the contents of the file to be discarded.
###### 12.1
Not setting the link in the last node of a list to NULL can lead to runtime errors.
###### 12.2
Not freeing dynamically allocated memory when it’s no longer needed can cause the sys- tem to run out of memory prematurely. This is sometimes called a “memory leak.”
###### 12.3
Freeing memory not allocated dynamically with malloc is an error.
###### 12.4
Referring to memory that has been freed is an error that typically results in the program crashing.
###### 12.5
Not setting the link in the bottom node of a stack to NULL can lead to runtime errors.
###### 12.6
Not setting the link in the last node of a queue to NULL can lead to runtime errors.
###### 12.7
Not setting to NULL the links in leaf nodes of a tree can lead to runtime errors.
###### 13.1
Attempting to redefine a symbolic constant with a new value is an error.
###### 14.1
Placing an ellipsis in the middle of a function parameter list is a syntax error—an ellipsis may be placed only at the end of the parameter list.
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

