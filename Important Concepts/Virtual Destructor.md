# Destructor

A member function of a class that is automatically called when an object of a class goes out of scope or is explicitly deleted.

Used to release any resources allocated by the class.

# Virtual Destructors

When you have a base class and a derived class, and you want to delete an object of the derived class through a pointer or reference of base class, **destructor of the derived class will not be called if the base destructor is not declared as virtual**.

**Example 1: Normal**

class Base{

public:

Base(){ "B Constructor";}

~Base(){ "B Destructor";}

void start1(){"Start1";}

};

class Derived: public Base{

public:

Derived(){ "D Constructor";}

~Derived(){"D destructor";}

void start2(){ "Start 2";}

};

int main(){

Base *b=new base();

b.start1(); //b.start2()->Can't call

delete b;

Derived * d= new Derived();

d.start1();// d.start2()->Can call both base and derived class functions

delete d;

Base * bptr= new Derived();

bptr.start1(); //bptr.start2()->not able to call

delete bptr;

}

**Output:**       

B Constructor

B Destructor


B Constructor

D Constructor

D Destructor

B Destructor


B Constructor

D Constructor

B Destructor

---------------------------------------------------------------------------------------------------------------------------------

B Constructor

start1

B Destructor


B Constructor

D Constructor

start1

D Destructor

B Destructor


B Constructor

D Constructor

start1

B Destructor

**Example 2: Virtual Destructor**

class Base{

public:

Base(){ "B Constructor";}

virtual ~Base(){ "B Destructor";}

void start1(){"Start1";}

};

class Derived: public Base{

public:

Derived(){ "D Constructor";}

~Derived(){"D destructor";}

void start2(){ "Start 2";}

};

int main(){

Base *b=new base();

b.start1(); 

delete b;

Derived * d= new Derived();

d.start1();// d.start2()->Can call both base and derived class functions

delete d;

Base * bptr= new Derived();

bptr.start1(); //bptr.start2()->not able to call

delete bptr;

}

**output:**

B Constructor

B Destructor


B Constructor

D Constructor

D Destructor

B Destructor


B Constructor

D Constructor

D Destructor

B Destructor 

# Notes:

**Derived * derived = new Base(); // invalid conversion from base to derived**

**E.g:**

main(){

**Derived * derived= static_cast<Derived*> (new Base());**

derived.start1(); //base member function

derived.start2(); //Derived member function

delete derived;

}







