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