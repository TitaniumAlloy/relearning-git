interfacing a common method.

class Pencil {
    ...
    public void draw(Curve curve) {...}
}

class Brush {
    ...
    public void draw(Curve curve) {...}
}

//interfacing right here;
interface DrawingTool {
    void draw(Curve curve);
}

class Pencil implements DrawingTool {
    ...
    public void draw(Curve curve) {...}
}

class Brush implements DrawingTool {
    ...
    public void draw(Curve curve) {...}
}

Another important profit of introducing interfaces is that you can use them as a type:

DrawingTool pencil = new Pencil();
DrawingTool brush = new Brush();

Now both a pencil and a brush objects have the same type. It means that both classes can be treated in a similar way as a DrawingTool. This is another way of supporting polymorphism, which helps to design reusable drawing function of the graphical editor program.

void drawCurve(DrawingTool tool, Curve curve) {
    System.out.println("Drawing a curve " + curve + " using a " + tool);
    tool.draw(curve);
}


Interface is the super/parent class blue print. Decompose meaning you can put it clean in a private method




An interface can contain:

    public constants;
    abstract methods without an implementation (the keyword abstract is not required here);
    default methods with implementation (the keyword default is required);
    static methods with implementation (the keyword static is required);
    private methods with implementation.




interface Interface {
        
    int INT_CONSTANT = 0; // it's a constant, the same as public static final int INT_FIELD = 0
        
    void instanceMethod1();
        
    void instanceMethod2();
        
    static void staticMethod() {
        System.out.println("Interface: static method");
    }
        
    default void defaultMethod() {
        System.out.println("Interface: default method. It can be overridden");
    }

    private void privateMethod() {
        System.out.println("Interface: private methods in interfaces are acceptable but should have a body");
    }
}
