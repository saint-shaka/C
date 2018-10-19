###### 1.1
Because C is a hardware-independent, widely available language, applications written in C often can run with little or no modification on a wide range of computer systems.
###### 1.2
Using C Standard Library functions instead of writing your own comparable versions can improve program portability, because these functions are used in virtually all Standard C implementations.
###### 4.1
The keystroke combinations for entering EOF (end of file) are system dependent.
###### 4.2
Testing for the symbolic constant EOF (rather than –1) makes programs more portable. The C standard states that EOF is a negative integral value (but not necessarily –1). Thus, EOF could have different values on different systems.
###### 5.1
Using the functions in the C standard library helps make programs more portable.
###### 5.2
Programs that depend on the order of evaluation of the operands of operators other than &&, ||, ?:, and the comma (,) operator can function differently on different compilers.
###### 6.1
Not all compilers support the C11 standard’s Annex K functions. For programs that must compile on multiple platforms and compilers, you might have to edit your code to use the versions of scanf_s or scanf available on each platform. Your compiler might also re- quire a specific setting to enable you to use the Annex K functions.
###### 7.1
The number of bytes used to store a particular data type may vary between systems. When writing programs that depend on data type sizes and that will run on several computer systems, use sizeof to determine the number of bytes used to store the data types.
###### 7.2
Because the results of pointer arithmetic depend on the size of the objects a pointer points to, pointer arithmetic is machine and compiler dependent.
###### 8.1
The C standard indicates that a a string literal is immutable (i.e., not modifiable), but some compilers do not enforce this. If you might need to modify a string literal, it must be stored in a character array.
###### 9.1
With some compilers, the exponent in the outputs will be shown with two digits to the right of the + sign.
###### 9.2
The conversion specifier p displays an address in an implementation-defined manner (on many systems, hexadecimal notation is used rather than decimal notation).
###### 10.1
Because the size of data items of a particular type is machine dependent and because storage alignment considerations are machine dependent, so too is the representation of a structure.
###### 10.2
Use typedef to help make a program more portable.
###### 10.3
If data is stored in a union as one type and referenced as another type, the results are im- plementation dependent.
###### 10.4
The amount of storage required to store a union is implementation dependent but will always be at least as large as the largest member of the union.
###### 10.5
Some unions may not port easily among computer systems. Whether a union is portable or not often depends on the storage alignment requirements for the union member data types on a given system.
###### 10.6
Bitwise data manipulations are machine dependent.
###### 10.7
Enter a nonnegative int: 65000
65000 = 00000000 00000000 11111101 11101000
Fig. 10.7 | Displaying an unsigned int in bits. (Part 2 of 2.)

Figure 10.7 can be made more generic and portable by replacing the integers 31 (line 21) and 32 (line 26) with expressions that calculate these integers, based on the size of an unsigned int for the platform on which the program executes. The symbolic constant CHAR_BIT (defined in <limits.h>) represents the number of bits in a byte (normally 8). Recall sizeof determines the number of bytes used to store an object or type. The expres- sion sizeof(unsigned int) evaluates to 4 for 32-bit unsigned ints and 8 for 64-bit un- signed ints. You can replace 31 with CHAR_BIT * sizeof(unsigned int) - 1 and replace 32 with CHAR_BIT * sizeof(unsigned int). For 32-bit unsigned ints, these expressions evaluate to 31 and 32, respectively. For 64-bit unsigned ints, they evaluate to 63 and 64.
###### 10.8
The result of right shifting a negative number is implementation defined.
###### 10.9
Bit-field manipulations are machine dependent.
###### 12.1
A structure’s size is not necessarily the sum of the sizes of its members. This is so because of various machine-dependent boundary alignment requirements (see Chapter 10).
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
