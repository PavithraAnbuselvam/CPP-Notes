# raw pointers con's
**.** raw pointers allow sharing but, it is allow room for errors (forgetting to deallocate)

**.** ownership of pointers (deallocate pointer from some where and using it from other place without knowing)

**.** smart pointers are addressing these issues

# Smart Pointers

It is used for managing dynamic memory automatically,helping to prevent memory leaks and dangling pointers.
The provide a way to manage the lifetime of dynamically allocated objects in a safe and efficient manner.
Here are the main types of smart pointers available in c++.

**Smart Pointers in C++**

1)std::unique_ptr

2)std::shared_ptr

3)std::weak_ptr

# 1.std::unique_ptr

A unique_ptr is a smart pointer **that owns and manages another object through a pointer** and disposes of that object when the unique_ptr goes out of scope.

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

# 2.std::shared_ptr

A std::shared_ptr is a smart pointer that retains **shared ownership of a dynamically allocated object through a pointer**. Several shared_ptr objects may own the same object.

**Reference Counting:** It uses reference counting to keep track of how many shared_ptr objects are pointing to the managed object.

The object is destroyed when the last shared_ptr pointing to it is destroyed or reset.

**Copy Semantics:** shared_ptr can be copied, and each copy increases the reference count.

**Use Case:** Suitable for scenarios where multiple parts of a program need to share a ownership of a resource.

#include <iostream>
#include <memory>

class Resource{
public:

Resource(){std::cout<<"Resource acquired\n";}

~Resource(){std::cout<<"Resource destroyed\n"};

};

void useResource(const std::shared_ptr<Resource>& res){

std::cout<<"Using resource\n";

}

int main(){

std::shared_ptr<Resource> ptr1(new Resource());

{

std::shared_ptr<Resource> ptr2=ptr1;//Reference count is now 2 

useResource(ptr2);//Reference count is still 2

//ptr2 goes out of scope, reference count is now 1

}
//ptr1 goes out of scope, reference count is now 0, and the resource is destroyed

return 0;

}


# 3.std::weak_ptr

A std::weak_ptr is a smart pointer that **holds a non-owning reference to an object** that is mentioned by **std::shared_ptr**.

**No Ownership:** It does not affect the reference count of **the managed object**. The object can be destroyed even if there are weak_ptr instances pointing to it.

**Use Case:** Useful for breaking **circular references** between **shared_ptr instances** or for **observing an object without affecting its lifetime.**











