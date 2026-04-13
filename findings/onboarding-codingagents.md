# CodingAgents Onboarding

## 1. Repository Purpose
This repository contains a beginner-friendly, single-page web calculator.
It demonstrates core front-end concepts in one file: HTML structure, CSS styling, and JavaScript behavior.

## 2. Structure Summary
- `index.html`: Entire app implementation.
- `AGENTS.md`: Instructions for repo analysis behavior.
- `findings/`: Generated markdown findings and onboarding notes.
- `.codex/`: Project-local Codex skill configuration.

## 3. Quick Start
### Prerequisites
- Any modern browser (Chrome, Edge, Firefox, Safari).

### Run
1. Open `index.html` in a browser.
2. Enter two numbers.
3. Pick an operation.
4. Click **Calculate**.

No install, build, or server step is required.

## 4. Beginner-Friendly Example
### Example Chosen
Calculator execution flow in `index.html` from button click to displayed result.

### Why this is a good first example
- All logic is in one place.
- The behavior is immediately visible in the browser.
- It teaches DOM access, event handling, input validation, and function dispatch.

## 5. Step-by-Step Walkthrough
1. Enter values in the `num1` and `num2` inputs.
2. Click **Calculate**, triggering the `click` event listener on `calculateBtn`.
3. The handler reads values with `document.getElementById(...).value` and converts them using `parseFloat`.
4. The code validates input with `Number.isNaN`; invalid inputs show: `Result: Please enter valid numbers`.
5. The selected operation (`add`, `subtract`, `multiply`, `divide`) is read from the `operation` `<select>`.
6. The handler dispatches to the corresponding arithmetic function.
7. If dividing by zero, `divide` returns `Cannot divide by zero`.
8. The app sets `resultElement.textContent` to show the final result in the UI.

## 6. Mermaid Diagram
```mermaid
flowchart TD
  A[User enters num1 and num2] --> B[User clicks Calculate]
  B --> C[Read and parse input values]
  C --> D{Inputs valid?}
  D -- No --> E[Show validation message]
  D -- Yes --> F[Read selected operation]
  F --> G{Operation}
  G -- add --> H[add(a,b)]
  G -- subtract --> I[substract(a,b)]
  G -- multiply --> J[multiply(a,b)]
  G -- divide --> K[divide(a,b)]
  K --> L{b == 0?}
  L -- Yes --> M[Cannot divide by zero]
  L -- No --> N[a / b]
  H --> O[Render Result]
  I --> O
  J --> O
  M --> O
  N --> O
```

## 7. Next Learning Steps
1. Move JavaScript into `script.js` to separate concerns.
2. Add unit tests for arithmetic functions.
3. Add keyboard support (Enter key to calculate).
4. Add formatting for decimal precision.
