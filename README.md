# CSS `calc()` Gotcha: Percentages and Unit Conversion Issues

This repository demonstrates a common, yet subtle, bug that can occur when using the `calc()` function in CSS, specifically when dealing with percentages and other units. The issue stems from how `calc()` handles unit conversions and the order of operations, especially when parent element dimensions aren't fully determined yet.

The `bug.css` file showcases the problematic CSS code. The `bugSolution.css` provides a potential fix.  Please refer to the comments in the code for further explanations.

## How to Reproduce

1. Clone the repository.
2. Open `index.html` (you may need to create a simple HTML file to test).
3. Observe the unexpected width of the element in the buggy example.
4. Compare it with the corrected example.

## Solution

Avoid complex expressions within `calc()`.  Where possible, ensure that the values are fully resolved and of the same unit (e.g., convert percentages to pixels if possible) before using the `calc()` function. Alternative approaches might include using JavaScript to dynamically compute values or restructuring CSS to use simpler calculations.
