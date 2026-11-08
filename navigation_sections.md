# Navigation and Sections

Navigation should express user intent and preserve a predictable application state.

## Guidelines
- Centralize route or section identifiers.
- Define whether navigation creates, reuses, or restores a ViewModel.
- Guard navigation when unsaved changes exist.
- Keep authorization checks outside visual-only visibility rules.
- Support deep links only when route state can be validated safely.

## Sections
Use sections to group related capabilities. Keep selection state synchronized with navigation and ensure keyboard users can reach every section.
