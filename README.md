# IT102A-Final-Project-Pascua
## Terminal Nexus `
**Janreuben Bernasor & Winston Pascua**

This console-based menu program built in C language for IT102A final project. It contains four working module that user can select from main menu: Pattern Generator, Pascal's Triangle, Grade Calculator & Evaluator, and Palindrome Checker. When the user enter 0 from the menu, the program ends.

The program has include input validation that checks if the user typed a a valid number, and clears left over input character to prevent unexpected infinite loop. If the user enters invalid input such as letter, emoji or even out of range that is not being showed in the display, the program refreshes the display, and ask the user to input again.

**Pattern Generator**
- Allow the user to select from 1 to 5 such as right triangle, square, isosceles triangle, inverted triangle, and christmas tree. The user will input the rows.

**Pascal's Triangle**
- Generates a number in triangle form base on the user rows inputted.

**Grade Calculator & Evaluator**
- Accept prelim, midterm, semi-finals, and final grade, compute the average and evaluate whether the result is pass or fail.

**Palindrome Checker**
- Read a word and compare its first-half character to the reversed second-half , and tells the user if the word is palindrome or not.


## Known Issues & Bugs

* **Uninitialized Menu Input (`number`):** On the main menu, entering a non-numeric character causes `scanf` to fail without assigning a value to `number`, resulting in undefined behavior during the `do-while` condition check.
* **Console Pause Workaround:** The program uses consecutive `getchar();` calls to pause execution before returning or exiting, which can behave inconsistently depending on leftover newline characters in the input buffer.
* **Typo in Menu Output:** `"Isoceles Triangle Pattern Generator (3)"` contains a minor spelling error (*Isosceles*).
* **Code Structure & Duplication:** All menu logic, input validation loops, and pattern generation routines are contained inside `main()` with repeated code blocks rather than modular functions.
