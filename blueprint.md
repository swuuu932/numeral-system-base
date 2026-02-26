# Numeral System Base Simulation Blueprint

## Project Overview
This project is a visual simulation that explores the behavior of natural numbers when their digit sums are iteratively used as bases for their next representation. It aims to classify each number's final state into fixed points, 2-cycles, or 3+ cycles.

## Features & Design
- **Iterative Process**: For each number $N \in [1, 1000]$, the simulation calculates the sum of digits in the current base, then uses that sum as the new base.
- **Classification**:
    - **Fixed Point (Period 1)**: The base stabilizes (e.g., $N=15$ stabilizes at base 3).
    - **2-Cycle (Period 2)**: The base alternates between two values.
    - **3+ Cycle (Period 3+)**: The base cycles through three or more values.
    - **Termination**: If the base reaches 1 or 0, the process stops.
- **Visualization**:
    - A horizontal layout mapping $N$ from 1 to 1000.
    - Color-coded bars/dots based on the period of the final state.
    - Interactive tooltip showing the sequence and period length on hover.
- **Aesthetics**: Modern, clean UI with high-contrast colors for different states and smooth canvas rendering.

## Current Plan
1.  **Logic Implementation**:
    - Function `getSumOfDigits(n, base)` to handle base conversion and summing.
    - Function `analyzeNumber(n)` to iterate and detect cycles using a history array.
2.  **Visualization Implementation**:
    - Use HTML5 Canvas to draw 1000 bars.
    - Implement color mapping: Blue (Fixed), Red (2-cycle), Green (3+ cycle), Gray (Terminated).
3.  **Interactivity**:
    - Add a mousemove listener to detect which number is being hovered.
    - Display details in a floating tooltip or overlay.
4.  **Integration**:
    - Combine HTML, CSS, and JS into `index.html` as requested by the user.

## Implementation Steps
- [ ] Create `index.html` with logic and canvas drawing.
- [ ] Implement hover detection and data display.
- [ ] Style the UI for a polished look.
