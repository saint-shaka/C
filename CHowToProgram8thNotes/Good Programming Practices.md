###### 2.1
Every function should be preceded by a comment describing the function’s purpose.
###### 2.2
Add a comment to the line containing the right brace, }, that closes every function, including main.
###### 2.3
Indent the entire body of each function one level of indentation (we recommend three spaces) within the braces that define the body of the function. This indentation emphasizes the functional structure of programs and helps make them easier to read.
###### 2.4
Set a convention for the indent size you prefer and then uniformly apply that convention. The tab key may be used to create indents, but tab stops can vary. Professional style guides often recommend using spaces rather than tabs.
###### 2.5
Choosing meaningful variable names helps make a program self-documenting—that is, fewer comments are needed.
###### 2.6
The first letter of an identifier used as a simple variable name should be a lowercase letter. Later in the text we’ll assign special significance to identifiers that begin with a capital letter and to identifiers that use all capital letters.
###### 2.7
Multiple-word variable names can help make a program more readable. Separate the words with underscores as in total_commissions, or, if you run the words together, begin each word after the first with a capital letter as in totalCommissions. The latter style—often called camel casing because the pattern of uppercase and lowercase letters resembles the sil- houette of a camel—is preferred.
###### 2.8
Place a space after each comma (,) to make programs more readable.
###### 2.9
Place spaces on either side of a binary operator. This makes the operator stand out and makes the program more readable.
###### 2.10
Although it’s allowed, there should be no more than one statement per line in a program.
###### 2.11
A lengthy statement may be spread over several lines. If a statement must be split across lines, choose breaking points that make sense (such as after a comma in a comma-separated list). If a statement is split across two or more lines, indent all subsequent lines. It’s not correct to split identifiers.
###### 2.12
Refer to the operator precedence chart when writing expressions containing many opera- tors. Confirm that the operators in the expression are applied in the proper order. If you’re uncertain about the order of evaluation in a complex expression, use parentheses to group expressions or break the statement into several simpler statements. Be sure to observe that some of C’s operators such as the assignment operator (=) associate from right to left rather than from left to right.
###### 3.1
Indent both body statements of an if...else statement (in both pseudocode and C).
###### 3.2
If there are several levels of indentation, each level should be indented the same additional amount of space.
###### 3.3
When performing division by an expression whose value could be zero, explicitly test for this case and handle it appropriately in your program (such as by printing an error message) rather than allowing the fatal error to occur.
###### 3.4
Unary operators should be placed directly next to their operands with no intervening spaces.
###### 4.1
Too many levels of nesting can make a program difficult to understand. As a rule, try to avoid using more than three levels of nesting.
###### 4.2
The combination of vertical spacing before and after control statements and indentation of the bodies of control statements within the control-statement headers gives programs a two-dimensional appearance that greatly improves program readability.
###### 4.3
Limit the size of control-statement headers to a single line if possible.
###### 4.4
Although the case clauses and the default case clause in a switch statement can occur in any order, it’s common to place the default clause last.
###### 4.5
In a switch statement, when the default clause is last, the break statement isn’t required. You may prefer to include this break for clarity and symmetry with other cases.
###### 5.1
Familiarize yourself with the rich collection of functions in the C standard library.
###### 5.2
Although it’s not incorrect to do so, do not use the same names for a function’s arguments and the corresponding parameters in the function definition. This helps avoid ambiguity.
###### 5.3
Choosing meaningful function names and meaningful parameter names makes programs more readable and helps avoid excessive use of comments.
###### 5.4
Include function prototypes for all functions to take advantage of C’s type-checking capabilities. Use #include preprocessor directives to obtain function prototypes for the standard library functions from the headers for the appropriate libraries, or to obtain headers containing function prototypes for functions developed by you and/or your group members.
###### 5.5
Include parameter names in function prototypes for documentation purposes. The compiler ignores these names, so the prototype int maximum(int, int, int); is valid.
###### 5.6
Use only uppercase letters in the names of enumeration constants to make these constants stand out in a program and to indicate that enumeration constants are not variables.
###### 6.1
Use only uppercase letters for symbolic constant names. This makes these constants stand out in a program and reminds you that symbolic constants are not variables.
###### 6.2
In multiword symbolic constant names, separate the words with underscores for readability.
###### 6.3
Strive for program clarity. Sometimes it may be worthwhile to trade off the most efficient use of memory or processor time in favor of writing clearer programs.
###### 7.1
We prefer to include the letters Ptr in pointer variable names to make it clear that these variables are pointers and need to be handled appropriately.
###### 9.1
When inputting data, prompt the user for one data item or a few data items at a time. Avoid asking the user to enter many data items in response to a single prompt.
###### 9.2
Always consider what the user and your program will do when (not if) incorrect data is entered—for example, a value for an integer that’s nonsensical in a program’s context, or a string with missing punctuation or spaces.
###### 10.1
Always provide a structure tag name when creating a structure type. The structure tag name is required for declaring new variables of the structure type later in the program.
###### 10.2
Do not put spaces around the -> and . operators. Omitting spaces helps emphasize that the expressions the operators are contained in are essentially single variable names.
###### 10.3
Capitalize the first letter of typedef names to emphasize that they’re synonyms for other type names.
###### 10.4
Using typedefs can help make a program more readable and maintainable.
###### 10.5
Use only uppercase letters in enumeration constant names. This makes these constants stand out in a program and reminds you that enumeration constants are not variables.
###### 13.1
Using meaningful names for symbolic constants helps make programs self-documenting.
###### 13.2
By convention, symbolic constants are defined using only uppercase letters and underscores.
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
###### 
###### 
###### 
###### 
###### 
###### 
###### 
