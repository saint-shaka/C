###### 2.1
Avoid starting identifiers with the underscore character (_) to prevent conflicts with com- piler-generated identifiers and standard library identifiers.
###### 3.1
Use expressions of the same type for the second and third operands of the conditional operator (?:) to avoid subtle errors.
###### 3.2
Always include your control statements’ bodies in braces ({ and }), even if those bodies contain only a single statement. This solves the "dangling-else" problem, which we dis- cuss in Exercises 3.30–3.31.
###### 3.3
Typing the beginning and ending braces of compound statements before typing the indi- vidual statements within the braces helps avoid omitting one or both of the braces, pre- venting syntax errors and logic errors (where both braces are indeed required).
###### 3.4
Initialize all counters and totals.
###### 3.5
In a sentinel-controlled loop, explicitly remind the user what the sentinel value is in prompts requesting data entry.
###### 3.6
Do not compare floating-point values for equality.
###### 3.7
C generally does not specify the order in which an operator’s operands will be evaluated (although we’ll see exceptions to this for a few operators in Chapter 4). Therefore you should use increment or decrement operators only in statements in which one variable is incremented or decremented by itself.
###### 4.1
Control counting loops with integer values.
###### 4.2
Using the final value in the condition of a while or for statement and using the <= re- lational operator can help avoid off-by-one errors. For a loop used to print the values 1 to 10, for example, the loop-continuation condition should be counter <= 10 rather than counter < 11 or counter < 10.
###### 4.3
Infinite loops are caused when the loop-continuation condition in an iteration statement never becomes false. To prevent infinite loops, ensure that you do not place a semicolon immediately after a while statement’s header. In a counter-controlled loop, make sure the control variable is incremented (or decremented) in the loop. In a sentinel-controlled loop, make sure the sentinel value is eventually input.
###### 4.4
Although the value of the control variable can be changed in the body of a for loop, this can lead to subtle errors. It’s best not to change it.
###### 4.5
Do not use variables of type float or double to perform monetary calculations. The im- preciseness of floating-point numbers can cause errors that will result in incorrect mone- tary values. [In Exercise 4.23, we explore the use of integer numbers of pennies to perform precise monetary calculations.]
###### 4.6
Provide a default case in switch statements. Values not explicitly tested in a switch would normally be ignored. The default case helps prevent this by focusing you on the need to process exceptional conditions. Sometimes no default processing is needed.
###### 4.7
Remember to provide processing capabilities for newline (and possibly other white-space) characters in the input when processing characters one at a time.
###### 4.8
When an equality expression has a variable and a constant, as in x == 1, you may prefer to write it with the constant on the left and the variable name on the right (i.e., 1 == x) as protection against the logic error that occurs when you accidentally replace operator == with =.
###### 4.9
After you write a program, text search it for every = and check that it’s used properly. This can help you prevent subtle bugs.
###### 4.10
To make your input processing more robust, check scanf’s return value to ensure that the number of inputs read matches the number of inputs expected. Otherwise, your program will use the values of the variables as if scanf completed successfully. This could lead to logic errors, program crashes or even attacks.
###### 5.1
Include the math header by using the preprocessor directive #include <math.h> when using functions in the math library.
###### 5.2
Check that your functions that are supposed to return values do so. Check that your func- tions that are not supposed to return values do not.
###### 5.3
Always include function prototypes for the functions you define or use in your program to help prevent compilation errors and warnings.
###### 5.4
Avoid variable names that hide names in outer scopes.
###### 6.1
When looping through an array, the array index should never go below 0 and should al- ways be less than the total number of elements in the array (size – 1). Make sure the loop- continuation condition prevents accessing elements outside this range.
###### 6.2
Programs should validate the correctness of all input values to prevent erroneous infor- mation from affecting a program’s calculations.
###### 7.1
Initialize pointers to prevent unexpected results.
###### 7.2
Use pass-by-value to pass arguments to a function unless the caller explicitly requires the called function to modify the value of the argument variable in the caller’s environment. This prevents accidental modification of the caller’s arguments and is another example of the principle of least privilege.
###### 7.3
If a variable does not (or should not) change in the body of a function to which it’s passed, the variable should be declared const to ensure that it’s not accidentally modified.
###### 8.1
When storing a string of characters in a character array, be sure that the array is large enough to hold the largest string that will be stored. C allows strings of any length to be stored. If a string is longer than the character array in which it’s to be stored, characters beyond the end of the array will overwrite data in memory following the array.
###### 9.1
When outputting data, be sure that the user is aware of situations in which data may be imprecise due to formatting (e.g., rounding errors from specifying precisions).
###### 11.1
Open a file only for reading (and not updating) if its contents should not be modified. This prevents unintentional modification of the file’s contents. This is another example of the principle of least privilege.
###### 12.1
When using malloc, test for a NULL pointer return value, which indicates that the mem- ory was not allocated.
###### 12.2
When memory that was dynamically allocated is no longer needed, use free to return the memory to the system immediately. Then set the pointer to NULL to eliminate the possibility that the program could refer to memory that’s been reclaimed and which may have already been allocated for another purpose.
###### 12.3
Assign NULL to a new node’s link member. Pointers should be initialized before they’re used.
###### 13.1
Everything to the right of the symbolic constant name replaces the symbolic constant. For example, #define PI = 3.14159 causes the preprocessor to replace every occurrence of the identifier PI with = 3.14159. This is the cause of many subtle logic and syntax errors. For this reason, you may prefer to use const variable declarations, such as const double PI = 3.14159; in preference to the preceding #define.
###### 13.2
Enclose macro arguments in parentheses in the replacement-text to prevent logic errors.
###### 13.3
When inserting conditionally compiled printf statements in locations where C expects a single statement (e.g., the body of a control statement), ensure that the conditionally com- piled statements are enclosed in blocks.
###### 14.1
Avoid zero-sized allocations in calls to malloc, calloc and realloc.
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
