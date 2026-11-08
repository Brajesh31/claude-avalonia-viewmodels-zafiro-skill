# ViewModels and Commands

A ViewModel exposes presentation state and user actions without owning visual controls.

## State
- Expose observable properties with clear defaults.
- Keep derived state derived rather than maintaining duplicate mutable values.
- Represent loading, empty, success, and error states explicitly.
- Keep domain entities and persistence concerns out of view-specific state where possible.

## Commands
- Use asynchronous commands for I/O and long-running work.
- Disable or guard commands while an operation is already running when re-entry is unsafe.
- Surface cancellation and errors in a user-understandable state.
- Keep command methods thin and delegate business workflows to application services.

## Lifetime
Dispose subscriptions and owned resources. Avoid retaining views through event handlers or long-lived services.
