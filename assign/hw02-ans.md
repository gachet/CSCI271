# HW 2

---

## Guidelines

- Please follow the assignment grading criteria so that you will not lose points.
- All homework should be sent through Blackboard.
- Add a comment as a first line to your source file that should be: **YourLastName_YourFirstName_CSCI271_HW#**
- The `cpp` source file name of homework should be - **HW#Q#.cpp** or **HW#.cpp** - depending on number of assigned questions, e.g. HW1Q1.cpp, HW2.cpp
- All homework should be submitted in text file format in an organized and well-formatted fashion. **!!!No other formats are accepted!!!**.

---

## Problem

Write a program such that:

1. Ask the user to enter the price of a product A and product B. Store them as doubles.
2. Print the total cost, including sales tax. Assume the tax rate is 8.875%.
3. If the total cost is more than 20 dollars, print "It's expensive!" (Try this even though you have not learned if statements.)

**Answer:**

```c++
#include <iostream>
using namespace std;
int main()
{
    double A, B, cost;
    const double tax = 8.875;
    
    cout << "Enter the price of product A: ";
    cin >> A;
    cout << "Enter the price of product B: ";
    cin >> B;
    cost = (A+B)*(1+tax/100);
    cout << "Total cost is " << cost << endl;
    if (cost > 20.0)
        cout << "It's expensive!" << endl;
    return 0;
}
```