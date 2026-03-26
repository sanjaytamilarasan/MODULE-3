# Ex.No:1
# Ex.Name:Write a c++ program to find difference & quotient  of two numbers using Hierarchical inheritance?
## Date:
## Aim:
To write a C++ program using Hierarchical Inheritance to find the difference and quotient of two numbers.


## Algorithm:
STEP 1: Start the program.

STEP 2: Create a base class named Base with two protected integer members.

STEP 3: Define a member function to read the two numbers from the user.

STEP 4: Create a derived class Difference that inherits from Base.

STEP 5: In Difference, define a function to calculate the difference of the two numbers.

STEP 6: Create another derived class Quotient that inherits from Base.

STEP 7: In Quotient, define a function to calculate the quotient of the two numbers.

STEP 8: In the main() function, create objects for Difference and Quotient.

STEP 9: Use the objects to read values and call the respective functions.

STEP 10: Display the results and end the program.




## Program:
```
#include <iostream>
using namespace std;

// Base class
class Numbers {
protected:
    int a, b;
public:
    void setNumbers(int x, int y) {
        a = x;
        b = y;
    }
};

// Derived class to find the difference
class Difference : public Numbers {
public:
    int findDifference() {
        return a - b;
    }
};

// Derived class to find the quotient
class Quotient : public Numbers {
public:
    int findQuotient() {
        if (b != 0) {
            return a / b;
        } else {
            cout << "Error: Division by zero." << endl;
            return 0;
        }
    }
};

int main() {
    Difference diff;
    Quotient quot;
    int x1, y1, x2, y2;

    cin >> x1 >> y1;
    diff.setNumbers(x1, y1);
    cout << "Difference=" << diff.findDifference() << endl;

    cin >> x2 >> y2;
    quot.setNumbers(x2, y2);
    if (y2 != 0) {
        cout << "Quotient=" << quot.findQuotient() << endl;
    }

    return 0;
}

```


## Output:
<img width="723" height="327" alt="{68860C7B-3113-4948-9C45-5F4D2A3B9A96}" src="https://github.com/user-attachments/assets/78e6925f-e035-4759-bddb-771c93dc0652" />



## Result:
Thus, the program successfully demonstrates Hierarchical Inheritance where two derived classes compute difference and quotient separately using the same base class values.
