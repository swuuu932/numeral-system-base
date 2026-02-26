# Numeral System Base Simulation (Point Plot) Blueprint

## Project Overview
This tool focuses on the iterative transformation of a single input $N$. The core logic involves using the sum of digits of $N$ in its current base as the new base for the next step. The goal is to visualize the trajectory of these bases using a scatter plot of $(b_n, b_{n+1})$.

## Features & Design
- **Single Input $N$**: Users can input any natural number $N$.
- **Iterative Process**: 
    - Start with base 10 (or user-defined initial base).
    - Calculate $b_{n+1} = \text{sum of digits of } N \text{ in base } b_n$.
    - Maximum 50 steps.
    - Termination: $b \le 1$ or cycle detection.
- **Visualization (Chart.js)**:
    - **Scatter Plot**: X-axis represents $b_n$, Y-axis represents $b_{n+1}$.
    - **Color Coding**: Normal steps are blue; points within a detected cycle are highlighted in red.
    - **Line Tracing**: Optional line connecting points to show the sequence.
- **UI/UX**:
    - Input field for $N$.
    - "Simulate" button to trigger calculation.
    - Results table/summary showing the sequence.

## Implementation Steps
- [ ] Clean up existing `index.html` and implement the new single-input logic.
- [ ] Integrate Chart.js via CDN.
- [ ] Implement the $(b_n, b_{n+1})$ mapping and cycle detection.
- [ ] Add input controls and responsive styling.
