There is an important concept in programming called immutability. Immutability means that an object always stores the same values. If we need to modify these values, we should create a new object. The common example is the standard String class. Strings are immutable objects so all string operations produce a new string. Immutable types allow you to write programs with fewer errors.

Patient patient = new Patient();

patient.name = "Mary";
patient.name = "Alice";

Reference share of objects:

Patient patient = new Patient();

patient.name = "Mary";
patient.age = 24;

System.out.println(patient.name + " " + patient.age); // Mary 24

Patient p = patient;

System.out.println(p.name + " " + p.age); // Mary 24

It is important to understand that two variables refer to the same data in memory rather than two independent copies. Since our class is mutable, we can modify the object using both references.

patient.age = 25;
System.out.println(p.age); // 25

Keep in mind, that classes defined by programmers are reference types. When objects are created by the new operator it returns reference in memory where the created objects are located. By this reference, we can get access to its fields and change them. Several variables can refer to the same object through a reference. It is also possible to create two independent objects with the same field's content. It's important to understand that references to such objects are different. However, not all objects allow changing its state after creation. Such a feature is called immutability.
