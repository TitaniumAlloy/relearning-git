User define:

A method contains a set of modifiers, a type of the return value, a name, a list of parameters in parentheses () , and a body in curly brackets {}. The combination of the name of the method and the list of its parameters is known as a method signature. In our example, the signature is countSeeds(int, int).

Some methods also have a list of exceptions – they define its behavior in case of some mistake in the program. For now, we'll consider simple methods without exceptions.

Let's focus on the main components that we need to write simple methods from scratch. 

Remember, that if you try to return a value from a method with a void return type, a compile error will be thrown.

The first words are so-called modifiers. There are two types of modifiers in Java: access modifiers and non-access modifiers.

Access modifiers define the visibility of the method. For now, we're using a public access modifier, which means there are no restrictions for invoking the method even from other classes.

Non-access modifiers provide information about the behavior of methods to JVM. The modifier static means that the method belongs to the class and it can be accessed without creating any object. This type of method is called a static method.

If the method is declared without the static modifier, it means that the method can be invoked only through or with an object or instance of this class. Such methods are called instance methods. 


