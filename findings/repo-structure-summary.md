# Repository Structure Summary

## Repository
`./CodingAgents`

## Top-Level Structure
- `.codex/`: Local Codex project configuration and project-scoped skills.
- `findings/`: Markdown outputs for requested findings and onboarding artifacts.
- `AGENTS.md`: Repository-specific operating rules for analysis and findings output.
- `index.html`: Single-file calculator application (HTML, CSS, JavaScript).

## Runtime and Tooling
- No package manager files (`package.json`, lockfiles) detected.
- No build step required.
- Run by opening `index.html` directly in a browser.

## Entry Point
- Application entry point is `index.html`.
- JavaScript is embedded inline in a `<script>` block.

## Core Functional Units
- Arithmetic functions: `add`, `subtract`, `substract`, `multiply`, `divide`.
- UI bindings: number inputs (`num1`, `num2`), operation select (`operation`), button (`calculateBtn`), and result output (`result`).
- Event flow: button click reads input values, validates numbers, dispatches to selected arithmetic function, and renders result text.
