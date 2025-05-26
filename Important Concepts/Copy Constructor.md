>It is a special object used to create a new object as a copy of an existing object.

>It takes a reference to an object of the same class and copies its values into the new object.

>All class of c++ has default copy constructor.but, default copy constructor do shallow copy of object. it will make problem if our object used dynamically allocated data.

>so, if dynamically allocated data exists we have to do deep copy of the object.


    #include <iostream>
    class BasicNumber{

    public:

    int n;

    BasicNumber(int set_n){

    n = set_n; 
  
    }    

    }

    int main(){

    BasicNumber num1(7);

    cout<<"num1: "<< num1.n <<endl;

    /** copy constructor
    * - here instead of calling num2 default constructor
    * the copy constructor will be called.
    * - all member variables will be copied to new object 
    */
    BasicNumber num2 = num1;
    
    cout<<"num2: "<< num2.n <<endl;

    return 0;
    }
