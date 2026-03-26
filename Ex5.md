# Ex.No:5
# Ex.Name: Write a C++ program to perform bitwise | operation using  derived constructor (declare two input variable as protected in base class and read one value in base class constructor and read another value its derived class constructor  and do the  operation in its another derived class constructor ).

## Date:

## Aim:
To write a C++ program to perform a bitwise OR (|) operation using derived class constructors, where the two input variables are protected in the base class and initialized in constructors of base and derived classes.

## Algorithm:
STEP 1: Start the program.

STEP 2: Create a base class Base with two protected integer members.

STEP 3: In the Base class constructor, read the first integer from the user.

STEP 4: Create a first derived class Derived1 that inherits from Base.

STEP 5: In Derived1 constructor, read the second integer from the user.

STEP 6: Create a second derived class Derived2 that inherits from Derived1.

STEP 7: In Derived2 constructor, perform the bitwise OR (|) operation on the two integers.

STEP 8: Store the result in a local variable.

STEP 9: Display the result of the bitwise OR operation.

STEP 10: End the program.




## Program:
```
#include <iostream>

using namespace std;

class Base
{
protected:
    int x;

public:
    Base(int a) : x(a) {}
};

class Derived1 : public Base
{
protected:
    int y;

public:
    Derived1(int a, int b) : Base(a), y(b) {}
};

class Derived2 : public Derived1 
{
public:
    Derived2(int a, int b) : Derived1(a, b) 
    {
        int result = x | y;
        cout << "The Result is:" << result << endl;
    }
};

int main()
{
    int num1;
    cin >> num1;

    int num2;
    cin >> num2;

    Derived2 obj(num1, num2);

    return 0;
}

```


## Output:
<img width="574" height="299" alt="{614EB2C1-C5F1-4C5A-A11E-B57BE07C0CCE}" src="https://github.com/user-attachments/assets/b63317dd-48b3-407d-8de8-4a7b26bf4955" />




## Result:
Thus, the program successfully demonstrates bitwise OR operation using derived class constructors and accessing protected members from the base class.

