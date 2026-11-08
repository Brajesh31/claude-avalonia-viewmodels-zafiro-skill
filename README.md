# claude-avalonia-viewmodels-zafiro-skill

A Claude Code skill for building maintainable Avalonia ViewModels and multi-step workflows using ReactiveUI and Zafiro patterns.

## Overview

This skill focuses on the ViewModel layer of Avalonia applications. It covers reactive state, command design, wizard flows, section-based navigation, and composition between Views and ViewModels.

The goal is to keep UI-independent logic testable and avoid duplicating functionality already provided by the project's libraries.

## Main Capabilities

- Design ViewModels with ReactiveUI.
- Manage reactive state and property changes.
- Create commands with progress and status information.
- Build multi-step wizard workflows.
- Organize navigation and UI sections.
- Map Views to ViewModels.
- Configure composition and dependency injection.
- Keep application logic separate from visual controls.

## Core Principles

- Use a functional-reactive approach where appropriate.
- Keep ViewModels independent of Avalonia-specific visual types.
- Prefer existing Zafiro abstractions over custom duplication.
- Use explicit result and error handling.
- Keep commands focused and observable.
- Compose complex workflows from smaller units.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-avalonia-viewmodels-zafiro-skill.git ~/.claude/skills/avalonia-viewmodels-zafiro
```

## Usage

Invoke the skill for ViewModel, wizard, or navigation work:

```text
/avalonia-viewmodels-zafiro
```

Provide the Avalonia version, .NET version, ReactiveUI and Zafiro package versions, existing project conventions, and desired UI behavior.

## Reference Guide

| File | Focus |
|---|---|
| `viewmodels.md` | ViewModels and commands |
| `wizards.md` | Multi-step wizard flows |
| `navigation_sections.md` | Navigation and section-based UI |
| `composition.md` | View/ViewModel mapping and dependency injection |

## Recommended Workflow

1. Inspect the existing ViewModel and composition patterns.
2. Search for existing Zafiro helpers before writing new abstractions.
3. Define the state and operations the ViewModel owns.
4. Keep UI rendering concerns in Views.
5. Use commands for user-triggered operations.
6. Model wizard steps and validation explicitly.
7. Configure navigation and section discovery consistently.
8. Add tests for important state transitions.
9. Verify the UI behavior in the target application.

## Quality Checklist

- ViewModels do not depend on concrete visual controls.
- Reactive state has clear ownership.
- Commands expose appropriate execution state.
- Errors are represented consistently.
- Wizard steps have explicit validation and navigation rules.
- View and ViewModel mapping is predictable.
- Dependency injection is configured deliberately.
- Tests cover state transitions and failure cases.

## Repository Contents

- `SKILL.md`: Main ViewModel and workflow instructions.
- `viewmodels.md`, `wizards.md`, `navigation_sections.md`, `composition.md`: Focused implementation guides.
- `README.md`: Installation and usage guidance.

## Practical Principle

Do not create a new framework inside the ViewModel layer. Reuse established project abstractions and add custom code only when it solves a specific gap.
