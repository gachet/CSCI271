# HW 3

---

## Guidelines

- Please follow the assignment grading criteria so that you will not lose points.
- All homework should be sent through Blackboard.
- Add a comment as a first line to your source file that should be: **YourLastName_YourFirstName_CSCI271_HW#**
- The `cpp` source file name of homework should be - **HW#Q#.cpp** or **HW#.cpp** - depending on number of assigned questions, e.g. HW1Q1.cpp, HW2.cpp
- All homework should be submitted in text file format in an organized and well-formatted fashion. **!!!No other formats are accepted!!!**.

---

## Problem

Write a program that inputs the starting balance, the amount deposited, the number of checks, and the total value of all of the checks, and computes the monthly service fee for a checking account according to the following schedule:

- &#36;15 if the balance at the start of the month is less than &#36;400
- &#36;15 if the balance at the end of the month is less than &#36;400
- &#36;25 if the average check value is more than &#36;500
- &#36;50 if the balance at the end of the month is negative

In addition, there is a per-check fee which is computed as follows:

- checks 1 - 19 in any given month cost &#36;0.10 each
- checks 20 - 39 in any given month cost &#36;0.08 each
- checks 40 - 59 in any given month cost &#36;0.06 each
- additional checks cost &#36;0.04 each

If the starting balance is negative, the program should exit with the statement that the account has been closed.

The program should be designed for clarity and testing -- using carefully chosen variable names and displaying fees as they are incurred (along with the reason for the fee) will go most of the way to accomplishing this.

**Answer:**

```c++
#include <iostream>
using namespace std;
int main()
{
    double start_balance, end_balance, deposited, num_of_checks, val_of_checks;
    cout << "Enter the starting balance:" << endl;
    cin >> start_balance;
    cout << "Enter the deposited amount:" << endl;
    cin >> deposited;
    cout << "Enter the number of checks:" << endl;
    cin >> num_of_checks;
    cout << "Enter the the total value of checks:" << endl;
    cin >> val_of_checks;

    if (start_balance < 0) {
        cout << "The account has been closed" << endl;
        return 0;
    }

    double checkfee;
    if (num_of_checks >= 1 && num_of_checks <= 19)
        checkfee = num_of_checks*0.1;
    else if (num_of_checks >= 20 && num_of_checks <= 39)
        checkfee = num_of_checks*0.8;
    else if (num_of_checks >= 40 && num_of_checks <= 59)
        checkfee = num_of_checks*0.6;
    else
        checkfee = 59*0.6+(num_of_checks-59)*0.4;
    cout << "Check fees are " << checkfee << endl;

    // calculate and balance before applying fees
    end_balance = start_balance + deposited - val_of_checks;
    cout << "The the end of the month balance before fees " << end_balance << endl;

    double fee = 0;
    if (start_balance < 400) fee += 15;
    if (end_balance < 400) fee += 15;
    if (val_of_checks/num_of_checks > 500) fee += 25;
    if (end_balance < 0) fee += 50;
    cout << "Account fees are " << fee << endl;

    end_balance = end_balance - fee - checkfee;
    cout << "The account balance is " << end_balance << endl;
    
    return 0;
}
```