---
name: repo-onboarding-obsidian
description: Analyze a code repository and produce beginner onboarding documentation with a project structure summary, one beginner-friendly example explained step by step, and at least one Mermaid diagram. Use when asked to create onboarding docs, repo walkthroughs, newcomer guides, or architecture explainers, and publish the final markdown to Obsidian via MCP tools.
---

# Repo Onboarding Obsidian

## Overview
Produce a practical onboarding document for a repository and publish it to Obsidian.
Persist every requested finding as a Markdown file in `./findings` with a meaningful filename.

## Repository Resolution
Resolve the repository path before analyzing files.
If the user says "repo" without explicitly naming another one, treat it as `./CodingAgents`.

## Required Outputs
Include all of the following in the onboarding document:
1. Repository analysis summary.
2. Concise structure overview (major directories/files and purpose).
3. One beginner-friendly example from the repository.
4. Step-by-step explanation of that example.
5. At least one Mermaid diagram.
6. Final onboarding markdown saved in the repo and published to Obsidian.

## Workflow
1. Analyze repository contents using fast local inspection (`rg --files`, focused file reads, and config discovery).
2. Identify key areas: entry points, scripts, dependencies, build/run/test commands, and docs.
3. Select one beginner-friendly example using these criteria:
- Small surface area.
- Minimal prerequisites.
- Demonstrates a core repo concept.
- Runnable or understandable in isolation.
4. Draft onboarding markdown using `references/onboarding-template.md`.
5. Add at least one Mermaid diagram, such as:
- Folder map.
- Request-to-execution flow.
- Data flow for the chosen example.
6. Save findings and onboarding artifacts under `./findings` with meaningful names.
7. Publish to Obsidian via MCP.

## File Naming Rules
Use descriptive file names in `./findings`, for example:
- `repo-structure-summary.md`
- `beginner-example-<feature-name>.md`
- `onboarding-<repo-name>.md`

Avoid generic names like `notes.md` or `output.md`.

## Obsidian Publishing Procedure
1. Ensure the final onboarding markdown is complete locally.
2. Publish with MCP Obsidian tools.
3. Prefer writing to an explicit path such as `Onboarding/<repo-name>-onboarding.md`.
4. If re-running and the target note must be replaced, delete then re-create to avoid duplicate appended content.

## Quality Checklist
Before finishing, verify:
- The structure summary matches actual files.
- The beginner example exists and is accurate.
- The step-by-step walkthrough is actionable for a newcomer.
- Mermaid syntax is valid.
- A Markdown finding exists in `./findings` with a meaningful name.
- The onboarding document is published to Obsidian.
