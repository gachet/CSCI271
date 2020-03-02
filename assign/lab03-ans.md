# Lab 3

---

## Guidelines

- Please follow the assignment grading criteria so that you will not lose points.
- All lab work should be sent through Blackboard.
- Add comment as a first line to your source file that should be: **YourLastName_YourFirstName_CSCI271_LAB#**
- The `cpp` source file name of homework should be - **LAB#Q#.cpp** or **LAB#.cpp** - depending on number of assigned questions, e.g. LAB1Q1.cpp, LAB2.cpp
- All homework should be submitted in text file format in an organized and well-formatted fashion. **!!!No other formats are accepted!!!**.

---

## Problems

This lab contains three questions.

**Q1.** Predict the outputs of the following program.(Before running it). Then run the code and check if your answers are correct.

```c++
#include <iostream>
using namespace std;

int main() {
   if (12 == 11 || 8 == 8)
      cout << "condition is true" << endl;
   else
      cout << "condition is false" << endl;

   if (!false && true)
      cout << "aaa" << endl;

   if (9 < 12)
      cout << "bbb" << endl;
   else if (9 > 12)
      cout << "ccc" << endl;
   else
      cout << "ddd" << endl;

   if (9 > 12) {
      if (9 < 17)
         cout << "eee" << endl;
   }
   else
      cout << "fff" << endl;
}
```

**Answer:**
```
condition is true
aaa
bbb
fff
```

---

**Q2.** Write a program to do the following:

- ask the user to enter his/her salary.
- if the salary is less than 5, print "I do not believe you." and exit the program.
- if the salary is between 1000 and 2000, print "We are almost the same."
- if the salary is even number, print "That is an even salary."

**Answer:**
```c++
#include <iostream>
using namespace std;
int main()
{
    int salary;
    cout << "Enter the salary:";
    cin >> salary;

    if (salary <  5) {
        cout << "I do not believe you." << endl;
    }
    else {
        if ((salary >= 1000) && (salary <=2000))
            cout << "We are almost the same." << endl;
        if (salary % 2 == 0)
            cout << "That is an even salary." << endl;
    }
    return 0;
}
```

---

**Bonus.** Write a program to do the following:

- ask the user "Can you guess my age? You have 3 chances."(you may hardcode an age of your choice into your program).
- if the user guesses correctly, print "Congratulations!" and exit the program.
- if the user runs out of guesses, print "You failed.