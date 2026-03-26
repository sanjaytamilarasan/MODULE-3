# Ex.No:4
# Ex.Name: Write a C++ program to pass a character to the parameterized constructor of the base class through derived class constructor.
## Date:
## Aim:
To write a C++ program to pass a character to a parameterized constructor of a base class through the derived class constructor.

## Algorithm:
STEP 1: Start the program.

STEP 2: Create a base class Base with a private or protected character data member.

STEP 3: Define a parameterized constructor in the base class to initialize the character.

STEP 4: Create a derived class Derived that inherits publicly from Base.

STEP 5: Define a parameterized constructor in the derived class.

STEP 6: In the derived class constructor, use constructor initialization list to pass the character to the base class constructor.

STEP 7: Define a member function in the base class to display the character.

STEP 8: Create an object of the derived class in the main() function, passing the character as an argument.

STEP 9: Call the display function to show the character.

STEP 10: End the program.




## Program:
```
#include <iostream>
#include <string>
using namespace std;

class Base {
    char ch;
public:
    // Parameterized constructor in the base class
    Base(char c) : ch(c) {
        cout << " The value passed to the base class is " << ch << endl;
    }
};

class Derived : public Base {
public:
    // Derived class constructor that passes a character to the base class constructor
    Derived(char c) : Base(c) {
        cout << "The value " << c << " is passed through the derived class constructor" << endl;
    }
};

int main() {
    char input;
    cin >> input;

    // Creating a Derived class object and passing a character to it
    Derived obj(input);

    return 0;
}

```


## Output:
<img width="1162" height="377" alt="{A0ECB87D-6B4C-4C7D-9ECD-5F2A5BE9A4A5}" src="https://github.com/user-attachments/assets/021ae570-d270-436d-ba7f-c8ae0ce9d9ef" />




## Result:
Thus, the program successfully demonstrates passing a character from the derived class constructor to the parameterized constructor of the base class.

