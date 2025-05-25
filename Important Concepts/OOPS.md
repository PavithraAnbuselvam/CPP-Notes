**Object Oriented Programming **

It is the programming paradigm which implements the concept of Object in the program.
An object is a collection of data and the methods which operates on that data.
It includes many principles such as inheritance,encapsulation,Polymorphism and so on.
C used procedural-oriented programming.This approch was not effective because it had some limitations such as code that could not be reused in the program.
The core concepts are **abstraction, encapsulation, inheritance, and polymorphism**.

**Class**
A Class is a blueprint that defines the structure and behaviour of objects.
It is a building block of object oriented program.
It is a user-defined data type that contains data members and member functions that operate on the data members.

**Abstraction**
Abstraction means hiding internal implementation details and showing only the essential features.

**Abstract class** It contains at least one pure virtual function.It is a class that cannot be instantiated by its own.It is designed to be inherited by other classes.

**E.g**

class Animal
{
public:
  virtual void sound()=0;
};
class Dog:public Animal
{
public:
  void sound() override
  {
  cout<<"Dog barks";
  }
};
int main()
{
  Animal* a=new Dog();
  a->sound();
  delete a;
}




