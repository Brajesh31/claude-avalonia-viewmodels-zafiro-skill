# Wizards and Multi-step Flows

Use a wizard for a genuinely sequential task where users benefit from focused steps and progress feedback.

## Design
- Model each step's data and validation explicitly.
- Define forward, back, cancel, and completion behavior.
- Preserve entered data when navigating backward.
- Prevent progression when required validation fails.
- Handle asynchronous validation and loading states.
- Support resuming only when persistence and privacy requirements are defined.

## SlimWizard
When using the project's `SlimWizard`, follow its established step and navigation API rather than inventing a parallel state machine. Keep business validation in the ViewModel or domain layer.

## Test cases
Test valid progression, invalid input, cancellation, back navigation, and failures during final submission.
