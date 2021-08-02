In Java, an array has the following important features:

    an array is a reference type;
    all array elements are stored in the memory sequentially;
    each element of the array is accessed by its numerical index, the first element has the index 0;
    the last element is accessed by the index equal to array size – 1;
    it is possible to create an array to store elements of any type.

Declaration, instantiation, initialization

To create an array filled with elements we should:

    declare a variable of an array type (declaration);
    create an instance of the array object (instantiation);
    initialize the array by some values (initialization).

When we declare a variable, we define its type and name. Instantiation happens when memory is allocated for this object. Initializing the array object means that we put certain values of the array object into the memory of our program.

To declare an array we must use two special characters [ ] after the name of the type of elements in the array:

int[] array; // declaration form 1

or after the name of an array variable:

int array[]; // declaration form 2: less used in practice

The most general way to create an array is to use the special keyword new and specify the necessary number of elements:

int n = ...; // n is a length of an array
int[] numbers = new int[n];

This form is useful when the number of elements is known before starting the program. When we create an instance of the array object with indicated length like [n]. Default everything is zero.

The size of an array cannot be greater than Integer.MAX_VALUE. Actually, it is even slightly smaller than this value.

int[] numbers; // declaration
numbers = new int[n]; // instantiation and initialization with default values

float[] floatNumbers; // declaration 
floatNumbers = new float[] { 1.02f, 0.03f, 4f }; // instantiation and initialization


//array length method
int[] array = { 1, 2, 3, 4 }; // an array of numbers
        
int length = array.length; // number of elements of the array
        
System.out.println(length); // 4

//error
If we try to access a non-existing element by an index then a runtime exception occurs.

The program throws ArrayIndexOutOfBoundsException.

//Array.toString
byte[] famousNumbers = { 0, 1, 2, 4, 8, 16, 32, 64 };
String arrayAsString = Arrays.toString(famousNumbers); // [0, 1, 2, 4, 8, 16, 32, 64]
System.out.println(arrayAsString);

//Array.sort(array)
long[] bigNumbers = { 200000000L, 400000000L, 100000000L, 300000000L }; // it's unsorted
Arrays.sort(bigNumbers); // sorting whole array
System.out.println(Arrays.toString(bigNumbers)); // [100000000, 200000000, 300000000, 400000000]


//Arrays.equals
System.out.println(Arrays.equals(numbers1, numbers2)); // it prints "false"
System.out.println(Arrays.equals(numbers1, numbers3)); // it prints "true"

//Arrays.fill
// It takes an array, start index, end index (exclusive) and the value for filling the array
Arrays.fill(characters, 0, size / 2, 'A'); 
Arrays.fill(characters, size / 2, size, 'B');
