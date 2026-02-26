# Iterative Numeral System Transformation Blueprint

## Project Overview
This tool performs a specific mathematical iteration on a 10-digit natural number $N$. The process involves calculating the sum of decimal digits of $N$ to determine a new base $b$, converting $N$ to base $b$, and then re-interpreting the resulting string as a decimal integer for the next iteration.

## Core Logic (Iteration Steps)
1.  **Input**: A decimal natural number $N$ (using `BigInt`).
2.  **Step (1)**: Calculate the sum of the digits of $N$ in base 10. Let this be $b$.
3.  **Step (2)**: Convert $N$ to base $b$. Each "digit" in base $b$ is treated as its decimal string representation and concatenated.
    *   *Example*: If remainders are 3, 12, 1 in base $b$, the string becomes "1123" (assembled from 1, 12, 3).
4.  **Step (3)**: Interpret the resulting string as a new decimal integer $N_{next}$.
5.  **Step (4)**: Repeat for a user-defined number of steps.

## Features & UI
- **BigInt Support**: All calculations use `BigInt` to handle potentially massive numbers.
- **Table Output**: Displays Step #, $N$, $b$, Base-$b$ String, and Next $N$ for each iteration.
- **Controls**:
    - Input for $N$.
    - Input for the number of iterations.
    - Run button to start the process.
- **Error Handling**:
    - Stop if $b \le 1$ (base 1 is not defined for standard conversion).
    - Handle cases where $N$ grows beyond reasonable display limits.

## Implementation Details
- **Sum of Digits**: Convert `BigInt` to string, split, and sum.
- **Base Conversion**: Manual division/modulo loop to get remainders, then string concatenation.
- **Re-interpretation**: Use `BigInt(string)` to convert the base-$b$ string back to a decimal number.
- **No External Libraries**: Pure HTML/CSS/Vanilla JS.

## Implementation Steps
- [ ] Update `index.html` with the new logic and UI.
- [ ] Implement `toBaseString(n, b)` to handle arbitrary bases $b > 1$.
- [ ] Add basic styling for readability.
