# Lab 2

---

## Guidelines

- Please follow the assignment grading criteria so that you will not lose points.
- All lab work should be sent through Blackboard.
- Add comment as a first line to your source file that should be: **YourLastName_YourFirstName_CSCI271_LAB#**
- The labwork `cpp` source file name  should be - **LAB#Q#.cpp** or **LAB#.cpp** - depending on number of assigned questions, e.g. LAB1Q1.cpp, LAB2.cpp
- All lab work should be submitted in text file format in an organized and well-formatted fashion. **!!!No other formats are accepted!!!**.

---

## Problems

This lab contains two questions.

**Q1.** Predict the outputs of the following program.(Before running it). Then run the code and check if your answers are correct.

```c++
int main() {
    int x = 6, y = 0, z = 3;
    double a = 5.0, b= 4.0;
    cout << x << x * a << endl;                      // line (a)
    cout << (y / z) << "\nn\n" << z / x << endl;     // line (b)
    cout << sqrt(b) * sqrt(b) / x * z << endl;       // line (c)
    cout << (z % y) / (y % x) << endl;               // line (d)
    cout << x << "%" << y << "=" << "x % y" << "\n"; // line (e)
}
```

- What is the ouput at line (a)?
- What is the ouput at line (b)?
- What is the ouput at line (c)?
- What is the ouput at line (d)?
- What is the ouput at line (e)?

---

**Q2.** Write a complete C++ program that asks the user for a number of gallons and then outputs the equivalent number of liters. There are 3.78533 liters in a gallon. Use a declared constant. Since this is just an exercise, you need not have any comments in your program.
