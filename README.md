1.	Encapsulation is the bundling of data and methods that operate on the data into a single unit, called a class. It hides the internal state of an object from the outside world and only exposes the necessary functionality through well-defined interfaces. 
Create an Employee class having data members' Name, Eid, and Basic_Salary, to calculate the HRA is 20% of Basic Salary and DA is 25% of Basic salary and MA is 300 rupee. implement the following queries:
  a) Display the name and gross salary of an employee whose name starts With 'n'
  b).Display the Eid and gross salary whose Eid is equal to 107.
  c)  Count the total number of employees whose salary more than 20000/-

Answer :-
1. Super Keyword:
   - The super keyword in Java is used to refer to immediate parent class members (fields and methods). It is especially useful in cases of method overriding to differentiate between superclass and subclass methods.
   
 Accessing superclass members and invoking superclass constructor in a subclass.

java
class Vehicle {
    int Speed;

    Vehicle(int Speed) {
        this.Speed = Speed;
    }

    void displaySpeed() {
        System.out.println("Speed: " +Speed);
    }
}

class Car extends Vehicle {
    int doors;

    Car(int Speed, int doors) {
        super(Speed);          this.doors = doors;
    }

    void displayDetails() {
        super.displaySpeed(); 
        System.out.println("Number of Doors: " + doors);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car(200, 4);
        myCar.displayDetails();
    }
}


2. This Keyword:
   - The this keyword refers to the current instance of the class and is used to differentiate between instance variables/methods and local variables with the same name. It's also used to invoke current class constructors from other constructors (constructor chaining).
   - Example: Using this to refer to instance variables and methods within the same class.

java
class Example {
    int x;

    Example(int x) {
        this.x = x;  
    }

    void display() {
        System.out.println("Value of x: " + this.x);  
    }

    void update(int x) {
        this.x = x;  
    }
}


### Task 2: Exception Handling and Interface Implementation

a. Exception Handling:
   - In Java, exception handling is done using try-catch blocks. Checked exceptions must be handled explicitly using try-catch or specifying them in the method signature with throws.
   - Example:

java
public class Example {
    public static void main(String[] args) {
int a=20;
        try {
           
           int data =a/0;
       } 
catch (Exception e) {
            System.out.println("Exception is : " + e);
        }
System.out.println("exception caught and rest of the code will be proceeded");
    }
}


b. Interface and Multiple Interface Implementation:
   - An interface in Java is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.
   - Multiple interfaces can be implemented in a class using the implements keyword.
   - Example:

java
interface Interface1 {
    void method1();
}

interface Interface2 {
    void method2();
}

class MyClass implements Interface1, Interface2 {
    public void method1() {
        System.out.println("Implementation of method1");
    }

    public void method2() {
        System.out.println("Implementation of method2");
    }
}

public class Main {
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.method1();
        obj.method2();
    }
}
