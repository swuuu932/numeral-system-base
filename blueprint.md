# Dynamic Numeral System State Graph Blueprint

## Project Overview
This project visualizes the state transitions of a number system where the next state is determined by re-interpreting the current number's base-$b$ representation as a decimal integer, where $b$ is the sum of the decimal digits of the current number.

## System Definition
For a current integer $N$:
1.  **Calculate Base ($b$)**: Sum of the decimal digits of $N$.
2.  **Convert**: Transform $N$ into a base-$b$ representation.
    *   *Implementation Detail*: Since standard characters (0-9, A-Z) only support up to base 36, and $b$ can be larger, we will represent the base-$b$ value by concatenating the decimal string representation of each "digit" (remainder).
3.  **Re-interpret**: Parse the resulting string as a decimal integer to get the next state.

## Features
-   **Interactive Input**: Users can set the starting number $N$ and the maximum number of iterations.
-   **Graph Visualization**:
    -   **Nodes**: Represent each unique number in the sequence.
    -   **Edges**: Directed arrows showing the transition $N \to N_{next}$.
    -   **Visual Encoding**:
        -   **Fixed Point**: Green (Self-loop).
        -   **Cycle**: Orange (Part of a repeating loop).
        -   **Transient**: Blue (Leading to a cycle/fixed point).
-   **Force-Directed Layout**: Uses a physics-based simulation (custom implementation) to arrange nodes on the HTML5 Canvas.
-   **Interactivity**: Clicking a node displays detailed statistics:
    -   Current Value ($N$)
    -   Digit Sum ($b$)
    -   Base-$b$ String
    -   Next Value
-   **Tech Stack**: Single `index.html` file, no external libraries, `BigInt` for calculation.

## Implementation Steps
1.  **Data Logic**: Implement the transformation function using `BigInt`.
2.  **Simulation Engine**:
    -   Generate the sequence of numbers.
    -   Detect cycles and fixed points.
    -   Construct the graph data structure (nodes and links).
3.  **Visualization Engine**:
    -   Implement a simple force-directed graph layout algorithm.
    -   Render nodes and edges using Canvas API.
    -   Add animation loop for smooth layout adjustment.
4.  **UI & Interaction**:
    -   Add input controls and an info panel.
    -   Implement hit-testing for mouse clicks on canvas nodes.
