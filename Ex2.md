# Ex.No:2
# Ex.Name: Write a program to implement protected member with fractional values?
## Date:
## Aim:
To write a C++ program that demonstrates the use of protected data members with fractional (float) values using inheritance.

## Algorithm:
STEP 1: Start the program.

STEP 2: Create a base class named Base.

STEP 3: Declare two protected float data members to store fractional values.

STEP 4: Define a public function to read fractional values from the user.

STEP 5: Create a derived class named Derived that inherits publicly from Base.

STEP 6: In the derived class, define a function to perform an operation (e.g., addition of the two fractional values).

STEP 7: Access the protected members directly inside the derived class.

STEP 8: Display the result inside the derived class function.

STEP 9: In the main() function, create an object of the derived class and call required functions.

STEP 10: End the program.


## Program:
```
#include <iostream>
using namespace std;

class MyClass 
{
protected:
    float n;

public:
    MyClass(float value) : n(value) {}

    void displayValue() 
    {
        std::cout << "The value of num is: " << n << std::endl;
    }
};

int main()
{
    float a;
    cin>>a;
    
    MyClass obj(a);

    obj.displayValue();

}

```


## Output:
<img width="859" height="251" alt="{E77C69A9-D6FF-487F-9300-068C8CA7EC80}" src="https://github.com/user-attachments/assets/2b8a3613-e391-4251-87ac-f5fcb74d2d9b" />



## Result:
Thus, the program successfully demonstrates how protected fractional values can be accessed and processed inside a derived class.

