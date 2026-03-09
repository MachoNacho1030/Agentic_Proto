# Repository Map

This document describes the structure and operational workflow of the Antigravity prototype repository.

The goal of this repository is to support an **agent-assisted prototyping workflow** for the **Agentic Coding Maturity Intelligence Dashboard** project. The repository is structured so that both humans and agents can easily understand the system context, track activity, follow operational guidelines, and execute structured tasks.

---

# Project Purpose

This repository contains the documentation, guidelines, and operational structure for experimenting with an agent-driven workflow that analyzes literature related to **agentic coding ecosystems**.

The goal of the project is to explore how an AI agent can assist in building a research intelligence system that tracks the maturity of programming languages and frameworks used for agent-based development.

The resulting system will help generate structured insights such as:

- language ecosystem maturity comparisons
- framework evolution tracking
- benchmark analysis
- quarterly research briefings for leadership

---

# Repository Structure

The repository is organized into several key folders that represent different layers of the agent environment.

```
Readme.md
repo_map.md
.gitignore

prototype_context/
antigravity_timeline/
antigravity_guidelines/
skills/
tasks/
```

Each folder serves a specific purpose in the agent workflow.

---

# prototype_context/

This folder contains the **core documentation describing the prototype system**.

These documents provide the foundational context the agent needs to understand the project.

Typical files include:

- **Agentic Prototyping Story**  
  Describes how the idea originated and how the prototype workflow was developed.

- **Prototype Brief**  
  A detailed specification of the Agentic Coding Maturity Intelligence Dashboard.

- **CTO Brief**  
  A condensed version of the prototype brief designed for leadership review.

Agents should read this folder to understand:

- the problem being solved
- the system architecture
- the intended outcomes of the project

---

# antigravity_timeline/

This folder acts as the **agent memory layer**.

It records actions, requests, and analyses performed by the agent over time.

Entries typically include:

- the request made to the agent
- actions performed
- the agent’s reasoning or conclusions

This provides traceability and allows the agent to understand how the project has evolved.

---

# antigravity_guidelines/

This folder contains **operational best practices for interacting with the Antigravity environment**.

These guidelines help ensure consistent and efficient agent behavior.

Current guideline documents include:

- **prompting_best_practices.md**  
  Describes how prompts should be structured when interacting with the agent.

- **token_efficiency.md**  
  Provides strategies for minimizing unnecessary token usage.

- **context_engineering.md**  
  Explains how project context should be structured and accessed by the agent.

Agents should reference these documents to follow best practices during analysis and execution.

---

# skills/

This folder defines **reusable agent capabilities**.

A skill describes how to perform a specific type of analysis or workflow.

Examples of skills used in this project may include:

- literature analysis
- benchmark extraction
- ecosystem comparison
- framework tracking
- report generation

Each skill document describes:

- when the skill should be used
- the steps required to perform the analysis
- the expected output format

Skills allow the agent to perform tasks consistently without reinventing methods each time.

---

# tasks/

This folder contains **discrete work items for the agent to complete**.

Each task represents a specific objective related to the project.

Tasks typically define:

- the goal of the task
- the relevant inputs
- the expected output
- the current status

Examples may include:

- identifying relevant literature sources
- analyzing benchmark results
- extracting ecosystem maturity signals

Agents should select tasks from this folder and use the appropriate skills to complete them.

---

# Readme.md

The root-level **README.md** is the main entry point for anyone (human or agent) encountering this repository for the first time.

It provides:

- a high-level description of the project and its motivation
- a summary of the repository structure
- the recommended agent workflow
- the current project status
- a note on the experimental nature of the work

Agents should read this file first to understand the purpose and scope of the project before diving into specific folders.

---

# .gitignore

Standard Git ignore rules for the repository. Excludes OS-generated files, editor settings, log files, temporary files, Python cache, virtual environments, Node modules, Jupyter checkpoints, and temporary data outputs.

This file does not affect agent behavior but ensures the repository stays clean when tracked via Git.

---

# Agent Workflow

Agents operating in this repository should follow the workflow below:

1. Read **repo_map.md** to understand the repository structure.
2. Review **prototype_context/** to understand the system and project goals.
3. Check **antigravity_timeline/** to understand previous activity.
4. Identify the next item in **tasks/**.
5. Use relevant capabilities from **skills/** to complete the task.
6. Record results in **antigravity_timeline/**.

This workflow ensures that the agent operates in a structured and traceable manner.

---

# Summary

The repository structure separates several important concerns:

```
prototype_context   → system knowledge
antigravity_timeline → agent memory
antigravity_guidelines → operational rules
skills → reusable capabilities
tasks → work assignments
```

This design allows the project to function as a structured **agentic prototyping environment**, supporting both experimentation and reproducible analysis.