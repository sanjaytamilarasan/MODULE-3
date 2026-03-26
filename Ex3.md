# Ex.No:3
# Ex.Name: Write a C++ program to get two numbers from two base classes and display the quotient in the derived class.
(Illustrate multiple Inheritance and use appropriate access specifier)
## Date:
## Aim:
To write a C++ program using multiple inheritance where two base classes provide two numbers, and the derived class computes and displays the quotient.

## Algorithm:
STEP 1: Start the program.

STEP 2: Create the first base class Base1 with one protected integer variable.

STEP 3: Create a member function in Base1 to read the first number.

STEP 4: Create the second base class Base2 with one protected integer variable.

STEP 5: Create a member function in Base2 to read the second number.

STEP 6: Create a derived class Result that inherits from both Base1 and Base2.

STEP 7: Inside the derived class, define a function to compute the quotient of the two numbers.

STEP 8: Ensure division by zero is checked before calculating.

STEP 9: Display the quotient in the derived class function.

STEP 10: Create an object of the derived class in main(), call input functions, compute and display results, and then end the program.




## Program:
```
#include <iostream>
using namespace std;

class A 
{
protected:
    int x;

public:
    void getX() 
    {
        cin >> x;
    }
};

class B
{
protected:
    int y;

public:
    void getY()
    {
        cin >> y;
    }
};

class C : public A, public B 
{
public:
    void show()
    {
        int res = x / y;
        cout << "Product of two numbers = " << res << endl;
    }
};

int main()
{
    C obj;

    obj.getX();
    obj.getY();

    obj.show();

    return 0;
}
```


## Output:
<img width="807" height="322" alt="{B1BCFE65-6645-487D-9599-FFC651F66687}" src="https://github.com/user-attachments/assets/fba43ac6-0ab1-480b-a242-9d8597c381e8" />



## Result:
Thus, the program successfully obtains two numbers from two base classes via multiple inheritance and displays their quotient in the derived class.

