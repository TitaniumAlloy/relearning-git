In most cases, an object of a reference type can be created using the new keyword. When we use the new keyword, the memory is allocated for the object we create. That is called instantiation of the object because we create an instance of it. Then we initialize the variable by assigning some value to it. Often, as in our example, it is done with one line.

String language = new String("java"); 
//instantiation of String and initialization with "java"

You can also use a literal for strings:

String language = "java";

The first approach with the keyword new is common for reference types, while the second is only string-specific. Both approaches give us the same result for strings but they have some technical differences which we will not consider here. 

The basic difference between primitive and reference types is that a variable of a primitive type stores the actual values, whereas a variable of a reference type stores an address in memory (reference) where the data is located. The data can be presented as a complex structure that includes other data types as their parts.

The following picture simply demonstrates this difference. There are two main memory spaces: stack and heap. All values of primitive types are stored in stack memory, but variables of reference types store addresses of objects located in heap memory.


String laanguage = new String("java");
String java = language;

stack b10 1, b10 2 -> heap b10 ("java")
int a and intb 100 = stack a100, and b100;


Every "new" creates a heap so if they don't point to the same heap from the stack it's gonna turn false even if it's the same string
System.out.println(s1 == s2); // false
System.out.println(s2 == s3); // true

Unlike primitive types, a variable of a reference type can refer to a special null value that represents the fact that it is not initialized yet or doesn't have a value.
Null is for reference type only, primitive won't compile.

Unfortunately, the frequent use of the null value can easily lead to errors in the program and complicate the code.
Reference of the address for reference variable
