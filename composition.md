# Composition and Mapping

Composition connects Views, ViewModels, services, and dependency injection.

## Guidelines
- Register dependencies at the application composition root.
- Prefer constructor injection for required dependencies.
- Keep View-to-ViewModel wiring consistent with the app's established conventions.
- Use explicit mapping between transport/persistence models and domain or presentation models.
- Avoid reflection-heavy mapping where simple, visible mapping is clearer.

## Testing
Unit-test ViewModel behavior with service fakes. Test composition separately to catch missing or incorrectly scoped registrations. Document singleton, scoped, and transient lifetimes and avoid capturing short-lived objects in long-lived services.
