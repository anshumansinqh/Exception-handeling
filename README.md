# Exception Handling

## Aim  
To study Exception Handling.

## Theory  
### Definition  
#### What is Exception Handling?
- Exception handling in C++ is a mechanism to handle runtime errors, allowing the program to continue its execution rather than terminating abruptly.
- Exceptions provide a way to react to exceptional circumstances (like runtime errors) in programs by transferring control to special functions called handlers.
- It involves three main keywords:
  - `try`: Defines a block of code where exceptions can occur.
  - `throw`: Used to throw an exception when a problem arises.
  - `catch`: Used to handle the exception thrown by the `throw` statement.

> For example:
```cpp
#include <iostream>
using namespace std;

int divide(int a, int b) {
    if (b == 0) {
        throw runtime_error("Division by zero error!");
    }
    return a / b;
}

int main() {
    int num1 = 10, num2 = 0;
    try {
        int result = divide(num1, num2);
        cout << "Result: " << result << endl;
    } catch (const runtime_error& e) {
        cout << "Caught an exception: " << e.what() << endl;
    }
    return 0;
}
```

## Algorithm

Exception handling in C++ allows the program to manage runtime errors and maintain the normal flow of execution. It uses `try`, `catch`, and `throw` blocks to handle exceptions.

### Steps:

1. **Throw an Exception:**
   - When an error occurs, throw an exception using the `throw` keyword.
   - The thrown exception must be caught by a `catch` block.

2. **Catch an Exception:**
   - The `catch` block handles the exception thrown in the `try` block.
   - Catch blocks are written to deal with specific types of exceptions.

3. **Try Block:**
   - The `try` block contains the code that might throw an exception.


## Conclusion 
In this experiment we learnt about exception handling.
