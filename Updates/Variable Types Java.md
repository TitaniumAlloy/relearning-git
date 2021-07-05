    byte: size 8 bits (1 byte), range from -128 to 127
    short: size 16 bits (2 bytes), range from -32768 to 32767
    int: size 32 bits (4 bytes), range from −(231) to (231)−1
    long: size 64 bits (8 bytes), range from −(263) to (263)−1
size are the same no matter what OS.

Floating-point types represent numbers with fractional parts. 
Java has two such types: double (64 bits) and float (32 bits). 
These types can store only a limited number of significant decimal digits (~6-7 for float and ~14-16 for double). Usually, you will use the double type in practice.
Syntax: double pi, float e;

Java has a type named char to represent letters (uppercase and lowercase), digits, and other symbols. Each character is just a single letter enclosed in single quotes. 
This type has the same size as the short type (2 bytes = 16 bits).
Syntax: char a;

Java provides a type called boolean, which can store only two values: true and false. It represents only one bit of information, but its size is not precisely defined.
Syntax: boolean a;

Calculation:
2^(n−1) − 1, where n is the number of bits - Choose the correct formula for calculating the upper (max) possible value of an int variable.
