Implicit casting flow chart below:

byte -> short -> int -> long -> float -> double
                  ^
                 char

Implicit casting example:
int num = 100;
long bigNum = num; // 100L

long bigNum = 100_000_000L;
double bigFraction = bigNum; // 100000000.0

short shortNum = 100;
int num = shortNum; // 100

char ch = '?';
int code = ch; // 63

In some cases, implicit type casting may be a bit lossy. When we convert an int to float, or a long to float or to double, we may lose some less significant bits of the value, which will result in a loss of precision. However, the result of this conversion will be a correctly rounded version of the integer value, which will be in the overall range of the target type. To understand that, check out the example:

long bigLong =  1_200_000_002L;
float bigFloat = bigLong; // 1.2E9 (= 1_200_000_000)

When we convert a char to an int in Java we actually get the ASCII value for a given character. ASCII value is an integer representation of English alphabet letters (both uppercase and lowercase), digits, and other symbols. Here you can find some of the standard symbols in ASCII.

char character = 'a';
char upperCase = 'A';

int ascii1 = character; // this is 97
int ascii2 = upperCase; // this is 65

Explicit type of casting:
double d = 2.00003;

// it loses the fractional part
long l =  (long) d; // 2

// requires explicit casting because long is wider than int
int i = (int) l; // 2 

// requires explicit casting because the result is long (indicated by L)
int val = (int) (3 + 2L); // 5

// casting from a long literal to char
char ch = (char) 55L; // '7'

However, the explicit casting may truncate the value, because long and double can store a much larger number than int.

long bigNum = 100_000_000_000_000L;
int n = (int) bigNum; // 276447232

Known as type overflow.

As you remember, in Java long is a 64-bit number, while int is 32-bit. When converting long to int the program just takes the last 32 bits to represent the new number. If the long contains a number less than or equal to Integer.MAX_VALUE you can convert it by casting without losing information. Otherwise, the result will be quite meaningless, although determined. That is why you shouldn't perform casting from a larger type to a smaller type unless you are absolutely sure that it is necessary, and that truncation will not interfere with your program.
