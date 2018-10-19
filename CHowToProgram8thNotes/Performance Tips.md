###### 1.1
Using C Standard Library functions instead of writing your own versions can improve program performance, because these functions are carefully written to perform efficiently.
###### 4.1
The break and continue statements, when used properly, perform faster than the corresponding structured techniques that we’ll soon learn.
###### 4.2
In expressions using operator &&, make the condition that’s most likely to be false the leftmost condition. In expressions using operator ||, make the condition that’s most likely to be true the leftmost condition. This can reduce a program’s execution time.
###### 5.1
Automatic storage is a means of conserving memory, because automatic variables exist only when they’re needed. They’re created when a function is entered and destroyed when the function is exited.
###### 5.2
Dividing a large program into functions promotes good software engineering. But it has a price. A heavily functionalized program—as compared to a monolithic (i.e., one-piece) program without functions—makes potentially large numbers of function calls, and these consume execution time on a computer’s processor(s). Although monolithic programs may perform better, they’re more difficult to program, test, debug, maintain, and evolve.
###### 5.3
Today’s hardware architectures are tuned to make function calls efficient, C compilers help optimize your code and today’s hardware processors are incredibly fast. For the vast majority of applications and software systems you’ll build, concentrating on good software engineering will be more important than programming for high performance. Nevertheless, in many C applications and systems, such as game programming, real-time systems, operating systems and embedded systems, performance is crucial, so we include performance tips throughout the book.
###### 6.1
Sometimes performance considerations far outweigh clarity considerations.
###### 6.2
In functions that contain automatic arrays where the function is in and out of scope frequently, make the array static so it’s not created each time the function is called.
###### 6.3
Passing arrays by reference makes sense for performance reasons. If arrays were passed by value, a copy of each element would be passed. For large, frequently passed arrays, this would be time consuming and would consume storage for the copies of the arrays.
###### 6.4
Often, the simplest algorithms perform poorly. Their virtue is that they’re easy to write, test and debug. More complex algorithms are often needed to realize maximum performance.
###### 7.1
Passing large objects such as structures by using pointers to constant data obtains the performance benefits of pass-by-reference and the security of pass-by-value.
###### 7.2
sizeof is a compile-time operator, so it does not incur any execution-time overhead.
###### 7.3
Sometimes an algorithm that emerges in a “natural” way can contain subtle performance problems, such as indefinite postponement. Seek algorithms that avoid indefinite postponement.
###### 8.1
memcpy is more efficient than strcpy when you know the size of the string you are copying.
###### 8.2
Use memset to set an array’s elements to 0 rather than looping through them and assigning 0 to each element. For example, Fig. 6.3 could have initialized the five-element array n with memset(n, 0, 5);. Many hardware architectures have a block copy or clear instruction that the compiler can use to optimize memset for high-performance zeroing of memory.
###### 10.1
Passing structures by reference is more efficient than passing structures by value (which requires the entire structure to be copied).
###### 10.2
Bit fields help reduce the amount of memory a program needs.
###### 10.3
Although bit fields save space, using them can cause the compiler to generate slower-executing machine-language code. This occurs because it takes extra machine-language operations to access only portions of an addressable storage unit. This is one of many examples of the kinds of space–time trade-offs that occur in computer science.
###### 11.1
Closing a file can free resources for which other users or programs may be waiting, so you should close each file as soon as it’s no longer needed rather than waiting for the operating system to close it at program termination.
###### 12.1
An array can be declared to contain more elements than the number of data items expected, but this can waste memory. Linked lists can provide better memory utilization in these situations.
###### 12.2
Insertion and deletion in a sorted array can be time consuming—all the elements following the inserted or deleted element must be shifted appropriately.
###### 12.3
The elements of an array are stored contiguously in memory. This allows immediate access to any array element because the address of any element can be calculated directly based on its position relative to the beginning of the array. Linked lists do not afford such immediate access to their elements.
###### 12.4
Using dynamic memory allocation (instead of arrays) for data structures that grow and shrink at execution time can save memory. Keep in mind, however, that the pointers take up space, and that dynamic memory allocation incurs the overhead of function calls.
###### 13.1
In the past, macros were often used to replace function calls with inline code to eliminate the function-call overhead. Today’s optimizing compilers often inline function calls for you, so many programmers no longer use macros for this purpose. You can also use the C standard’s inline keyword (see Appendix E).
###### 14.1
The goto statement can be used to exit from deeply nested control structures efficiently.
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
###### 
###### 
###### 
###### 
