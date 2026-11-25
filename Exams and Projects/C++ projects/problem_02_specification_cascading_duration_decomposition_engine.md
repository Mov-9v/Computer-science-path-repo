# Problem 02: Cascading Duration Decomposition Engine

## Problem Specification

Write a complete C++ program that reads a server's total uptime from standard input as a single non-negative integer representing **total seconds**. The program must decompose this duration hierarchically in descending order and display the equivalent **Days**, **Hours**, **Minutes**, and remaining **Seconds**.

## Physical Constants

* $1\text{ Day} = 86,400\text{ seconds}$ ($24 \times 60 \times 60$)

* $1\text{ Hour} = 3,600\text{ seconds}$ ($60 \times 60$)

* $1\text{ Minute} = 60\text{ seconds}$

## Engineering Requirements

1. **Named Constants (`UPPER_SNAKE_CASE`):** Declare all time-unit conversion factors (`SECONDS_PER_DAY`, `SECONDS_PER_HOUR`, `SECONDS_PER_MINUTE`) as global `const int` identifiers above `int main()`.

2. **Single-Variable Memory Constraint:** Allocate **only one mutable variable** (`int remainingSeconds`) inside `main()`. Do not declare extra variables to store days, hours, or minutes.

3. **Pre-Mutation Input Echo:** Echo the original value of `remainingSeconds` back to standard output **before** performing any destructive modulo updates (`%=`).

4. **Cascading Division & Modulo Order:** For each hierarchical unit (Days $\rightarrow$ Hours $\rightarrow$ Minutes), compute and print the whole unit count using integer division (`/`) **before** reducing `remainingSeconds` via compound modulo assignment (`%=`).

5. **Code Hygiene:** Include a clear user prompt line before `cin`, maintain consistent 4-space indentation, and end `main()` with `return 0;`.

## Sample Test Cases (Manual Verification)

### Test Case 1

* **Input:**

  ```
  5485
  ```

* **Expected Output:**

  ```
  Enter total server uptime in seconds (integer): 5485

  Original duration entered : 5485 seconds
  --- Hierarchical Breakdown ---
  Days    : 0
  Hours   : 1
  Minutes : 31
  Seconds : 25
  ```

### Test Case 2

* **Input:**

  ```
  93784
  ```

* **Expected Output:**

  ```
  Enter total server uptime in seconds (integer): 93784

  Original duration entered : 93784 seconds
  --- Hierarchical Breakdown ---
  Days    : 1
  Hours   : 2
  Minutes : 3
  Seconds : 4
  ```

## Page 2 — Submitted Code

```cpp
#include <iostream>
#include <string>

using namespace std;

const int SECONDS_PER_DAY = 86400;
const int SECONDS_PER_HOUR = 3600;
const int SECONDS_PER_MINUTE = 60;

int main() {

	

	
	int remainingSeconds = 0;

	cout << "Enter total server uptime in seconds (integer) :";
	cin >> remainingSeconds; 

	cout << "Original duration entered :" << remainingSeconds << " seconds"<< endl;
	cout << "------------- Hierarchical Breakdown -------------" << endl;

	cout << "Days	  : " << remainingSeconds / SECONDS_PER_DAY << endl;
	remainingSeconds %= SECONDS_PER_DAY;

	cout << "Hour	  : " << remainingSeconds / SECONDS_PER_HOUR << endl; 
	remainingSeconds %= SECONDS_PER_HOUR; 

	cout << "Minutes   : " << remainingSeconds / SECONDS_PER_MINUTE << endl;
	remainingSeconds %= SECONDS_PER_MINUTE; 

	cout << "Seconds   : " << remainingSeconds << endl; 


	return 0; 


}
```