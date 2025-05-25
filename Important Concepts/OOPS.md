**Object Oriented Programming**

It is the programming paradigm which implements the concept of Object in the program.
An object is a collection of data and the methods which operates on that data.
It includes many principles such as inheritance,encapsulation,Polymorphism and so on.
C used procedural-oriented programming.This approch was not effective because it had some limitations such as code that could not be reused in the program.
The core concepts are **abstraction, encapsulation, inheritance, and polymorphism**.

**Class**
A Class is a blueprint that defines the structure and behaviour of objects.
It is a building block of object oriented program.
It is a user-defined data type that contains data members and member functions that operate on the data members.

-------------------------------------------------------**Abstraction**--------------------------------------------------------------------------
Abstraction means hiding internal implementation details and showing only the essential features.

**Abstract class** 
It contains at least one **pure virtual function**.
It is a class that cannot be instantiated by its own.
It is designed to be inherited by other classes.
Abstract classes can have constructors, and they are called when an object of a derived class is created.

**Pure Virtual Function**
Pure Virtual Function is a virtual function which doesn't have body.

**Syntax** virtual void fun()=0;

When you are not giving the body of the function in the base class,it becomes **abstract class**.

**E.g**

class Animal{

public:

  virtual void sound()=0;
  
};

class Dog:public Animal{

public:
 
  void sound() override  {
  
  cout<<"Dog barks";
  
  }

};

int main(){

  Animal* a=new Dog();
  
  a->sound();
  
  delete a;

}

**Error Eg**

class base{

public:

virtual void fun1()=0;

};

class Derived : public base{

public:

//some other functions

};

int main(){

Base b;// gives error

return 0;

}


----------------------------------------------------------**Encapsulation**--------------------------------------------------------------------

It is binding data and the functions into a single unit and restrict direct access to the some components.
Hiding internal and implementation details from outside and exposing only what is necessary through a public interface.

**Example**

class Account{

private:

int balance;

public:

void getBalance(){

return balance;

}

void setbalance(int b){

balance=b;

}};

int main(){

Account acc;

acc.setBalance(1000);

cout<<acc.getbalance();

//acc.balance=-500;    //you can't do this

return 0;
}


---------------------------------------------------------**Inheritance**-----------------------------------------------------------------------

It is fundamental concept in object-oriented programming that allows a **class to inherit attributes and methods from another class**.
This promotes code reusability, establishes a hierarchical relationship between classes, and supports the principles of polymorphism.

**Constructor and Destructor**
Constructors and destructors are not inherited, but they can be called explicitly in the derived class constructor and destructor.


class Base {

public:

    Base() {
    
        std::cout << "Base Constructor" << std::endl;
    
    }
    
    ~Base() {
    
        std::cout << "Base Destructor" << std::endl;
    
    }};

class Derived : public Base {

public:

    Derived() {
    
        std::cout << "Derived Constructor" << std::endl;
    
    }
    
    ~Derived() {
    
        std::cout << "Derived Destructor" << std::endl;
    
    }};

int main() {
  
    Derived d;
    
    return 0;
} 

**Output**

Base constructor

Derived constructor

Derived destructor

Base destructor


When a derived class object is created, the base class constructor is called first,followed by the derived class constructor.

When a derived class object is destroyed, the derived class destructor is called first, followed by the base class destructor.

**Inheritance types**

**Single Inheritance** A derived class inherits from one base class.

**Multiple Inheritance** A derived class inherits from more than one base class.

**Multiple Inheritance** A derived class inherits from another derived class, creating a chain.

**Hierarchical Inheritance** Multiple derived classes inherit from the same base class.

**Hybrid Inheritance** A combination of two or more types of inheritance.

----------------------------------------------------------**Polymorphism**---------------------------------------------------------------------
It allows the same function or operator to be used in different ways.

**Compiletime Polymorphism**
This is typically achieved through function overloading and operator overloading.

**Function Overloading**
Function overloading occurs when multiple functions have the same name but different parameters.
