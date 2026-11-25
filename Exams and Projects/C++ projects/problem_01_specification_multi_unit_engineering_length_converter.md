# Problem 01: Multi-Unit Engineering Length Converter

## Problem Specification

Write a complete C++ program that reads a structural measurement from standard input consisting of two integers: **feet** (`feet`) and **inches** (`inches`). The program must convert and display the total length in **inches**, followed by its metric equivalents in **centimeters** and **millimeters**.

## Physical Constants

* $1\text{ foot} = 12\text{ inches}$

* $1\text{ inch} = 2.54\text{ centimeters}$

* $1\text{ centimeter} = 10.0\text{ millimeters}$

## Engineering Requirements

1. **Named Constants (`UPPER_SNAKE_CASE`):** Declare all conversion factors as global `const` identifiers above `int main()` to eliminate magic numbers.

2. **Clear Prompt Line:** Output an explicit user prompt specifying the expected input format before calling `cin`.

3. **Input Echoing:** Echo the exact values read for `feet` and `inches` back to standard output immediately after extraction for auditability.

4. **Safe Mixed-Type Arithmetic:** Compute and print `totalInches` (`int`), `centimeters` (`double`), and `millimeters` (`double`), ensuring implicit widening from `int` to `double` occurs cleanly without unintended truncation.

5. **Code Hygiene:** Use self-documenting `camelCase` variable names, one declaration per line, consistent 4-space indentation, and `return 0;` to signal normal termination.

## Sample Test Case (Manual Verification)

* **Input:**

  ```
  6 5
  ```

* **Expected Output:**

  ```
  Enter structural length as two integers (feet inches): 6 5

  Input Received : 6 ft, 5 in
  Total Inches   : 77 in
  Metric (cm)    : 195.58 cm
  Metric (mm)    : 1955.8 mm
  ```

---

## Page 2 — Submitted Code

```cpp
#include <iostream>

using namespace std;


//Constants

const int FOOT = 12;//12 inches
const float INCH = 2.54f ; //2.54 cm
const int CM = 10.0; //10 mm

int main() {

	int feet = 0, inches = 0 , totaLInches = 0;
	
	
	cout << "Enter structural length as two integers (feet inches) :";
	cin >> feet >> inches;
	
	
	totaLInches = (feet * FOOT) + inches ;

	cout << "input received :" << feet << " ft, " << inches << " in" << endl;
	cout << "Total Inches :" << totaLInches << " in"<<endl;
	cout << "Metric (cm)" << totaLInches * INCH <<" cm"<< endl;
	cout << "Metric (cm)" << totaLInches * INCH * CM<<" mm"<<endl;
	 




	return 0; 
}
```