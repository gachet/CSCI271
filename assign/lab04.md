# Lab 4

---

## Guidelines

- Please follow the assignment grading criteria so that you will not lose points.
- All lab work should be sent through Blackboard.
- Add comment as a first line to your source file that should be: **YourLastName_YourFirstName_CSCI271_LAB#**
- The `cpp` source file name of homework should be - **LAB#Q#.cpp** or **LAB#.cpp** - depending on number of assigned questions, e.g. LAB1Q1.cpp, LAB2.cpp
- All homework should be submitted in text file format in an organized and well-formatted fashion. **!!!No other formats are accepted!!!**.

---

## Problems

In this lab you will be writing a menu based program that will determine the area of a shape based on user's choice. For each menu option, the program will ask for positive dimensions for the shape, then display the area.

- You will also be using two new libraries, `cmath` for the `pow` function and `iomanip` for `setprecision` in conjunction with `iostream` fixed. Also `#defined` constants for your menu options and PI.

- You will define 6 constant values: SQUARE as 1, RECTANGLE as 2, TRIANGLE as 3, CIRCLE as 4, EXIT as 0, and PI as 3.14159

- Declare three float variables (base, height, and area) and one int variable (choice).

- Display the menu and prompt for user's choice. Based off user's choice, branch to the corresponding case. Prompt for dimensions, calculate the area, and break out of the switch statement. If the user does not enter a valid menu choice, alert the user that the choice was an invalid option and exit the program.

- Area Formulas:
    - square: length_of_side^2
    - rectangle: base * height
    - triangle: 1/2 * base * height
    - circle: π * radius^2

- Use the `cmath`'s `pow(b,e)` function discussed earlier for any exponent arithmetic. If the dimensions are positive values, display the calculated area with precision up to 2 decimal places. Otherwise, alert the user that there was invalid inputed values. 

- Use following code as a starting point for this lab, however you may start from scratch if you choose to do so.

```c++
#include <iostream>
#include <iomanip>
#include <cmath>
using namespace std;

// preprocessor constant expressions
#define SQUARE 1
// define more macros here

// put your program in the main function
int main() {

    return 0;
}
```
