# Templates

1. Templates in C++ are amechanism that allows functions and classes to operate with generic types.

2. Allows you to write generic, reusable code without the need for repetitive code for different data types.

3. We can pass the data type as a parameter so that we don't need to write a same code for different data types.

# How templates work?

1. Templates are expanded at compile time.

2. This is like macros, difference is compiler does type_checking before template expansion.

# 1.Function Templates

Function templates allow you to create a single function that can operate on different data types.  

**Example**

#include <iostream>

//Function template to find the maximum of two values

template <typename T>

T printMax(T x, T y){

if(x>y)
{

return x;

else

return y;

}

int main(){

std::cout<<"Max of 10 and 20 is "<< printMax(10,20) <<std::endl;

return 0;

}

# 2.Class Template

1. Class templates allow you to define a class that can handle different data types.

2. Useful for creating data structures like linked lists,stacks, etc., that work with any data type.

3. When a class used the concept of template, then it is called as **generic class**.

**Example:**

template <class T>

class A{

public:

T num1 =5;

T num2 =6;

void add(){

num1+num2;

}

int main(){

A <int> d;

d.add();

return 0;

}










