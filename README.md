# IT101-Final-Project-Pascua
**Janreuben Bernasor & Winston Pascua**
-No flowchart yet

## Known Issues & Bugs

* **Uninitialized Menu Input (`number`):** On the main menu, entering a non-numeric character causes `scanf` to fail without assigning a value to `number`, resulting in undefined behavior during the `do-while` condition check.
* **Console Pause Workaround:** The program uses consecutive `getchar();` calls to pause execution before returning or exiting, which can behave inconsistently depending on leftover newline characters in the input buffer.
* **Typo in Menu Output:** `"Isoceles Triangle Pattern Generator (3)"` contains a minor spelling error (*Isosceles*).
* **Code Structure & Duplication:** All menu logic, input validation loops, and pattern generation routines are contained inside `main()` with repeated code blocks rather than modular functions.
