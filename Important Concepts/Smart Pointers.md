# Smart Pointers

It is used for managing dynamic memory automatically,helping to prevent memory leaks and dangling pointers.
The provide a way to manage the lifetime of dynamically allocated objects in a safe and efficient manner.
Here are the main types of smart pointers available in c++.

**Smart Pointers in C++**

1)std::unique_ptr

2)std::shared_ptr

3)std::weak_ptr

# 1.std::unique_ptr

A unique_ptr is a smart pointer that owns and manages another object through a pointer and disposes of that object when the unique_ptr goes out of scope.

**Ownership:** It holds exclusive ownership of dynamically allocated object. Only one unique_ptr can own an object at a time.

**Copy Semantics:** unique_ptr cannot be copied, but it can be moved to transfer ownership.

**Use Case:** Ideal for managing resources that should not be shared among multiple owners.

#include <iostream>
#include <memory>

class Resource{
public:

Resource(){std::cout<<"Resource acquired\n";}

~Resource(){std::cout<<"Resource destroyed\n"};

};

int main(){

std::unique_ptr<Resource> ptr1(new Resource());

//std::unique_ptr<Resource> ptr2=ptr1; //Error: cannot copy unique_ptr

std::unique_ptr<Resource> ptr2=std::move(ptr1); //Move Ownership

//At this point, ptr1 is nullptr

return 0;

}





