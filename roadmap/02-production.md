# Phase 2: production (weeks 7 to 12)

Phase 1 produced an app that works on your phone. In this phase you turn it into an app a team could maintain: layered, tested, usable offline and checked by CI. This is the mid level.

## Week 7: architecture

Topics

- The [Flutter architecture guide](https://docs.flutter.dev/app-architecture): UI layer, data layer, repositories and services
- Feature-first folder structure
- Dependency injection through your state library or through constructors
- Immutable models with `freezed` or plain Dart classes with `copyWith`

Build: restructure the shop app. Widgets stop calling the HTTP client. They talk to view models or blocs, which talk to repositories.

Done when: you can swap the real product repository for a fake one by changing a single line, and no widget file imports your HTTP package.

## Week 8: state management in depth

Topics

- Async state: loading, data, error and refresh
- Derived state and avoiding duplicated sources of truth
- Side effects: navigation, snackbars and dialogs triggered by state changes
- Scoping and disposal
- Optimistic updates and rollback

Build: the checkout flow. Address, delivery option, order summary and confirmation. Cart changes apply at once and roll back if the request fails.

Done when: rotating the device or leaving and reopening checkout never loses the user's input, and a failed request restores the previous cart exactly.

## Week 9: testing

Topics

- The [testing overview](https://docs.flutter.dev/testing/overview): unit, widget and integration tests
- Fakes and mocks, and when each one fits
- Golden tests for important screens
- `integration_test` for one full user journey

Build: unit tests for every repository and view model. Widget tests for cart and checkout. One integration test from opening the app to placing an order.

Done when: the logic layer has at least 80% line coverage, the whole suite runs in under two minutes, and no test depends on the network.

## Week 10: offline and persistence

Topics

- SQLite with [drift](https://pub.dev/packages/drift), including schema migrations
- Cache strategies: cache first, network first, stale while revalidate
- A queue for writes made while offline
- `flutter_secure_storage` for tokens

Build: the catalogue opens offline from the local database. Orders placed offline wait in a queue and send when the connection returns.

Done when: you can browse and place an order in airplane mode, turn the network on, and see the order sent once and only once.

## Week 11: real backend and authentication

Topics

- Token-based auth, refresh tokens and interceptors
- Timeouts, retries with backoff, and cancelling requests
- Mapping server errors to errors your app understands
- [Flavors](https://docs.flutter.dev/deployment/flavors) for dev and production

Build: replace DummyJSON with a real backend. Supabase, Firebase or your own API all work. Add login, register, logout and silent token refresh.

Done when: an expired token refreshes without the user noticing, a revoked session returns the user to login, and the dev and production builds install side by side.

## Week 12: tooling and CI

Topics

- Strict analysis options and a lint set such as `flutter_lints` or `very_good_analysis`
- `dart format` and `dart fix`
- GitHub Actions or another CI that runs format, analyze and test on every pull request
- Small pull requests and useful descriptions
- Reviewing your own diff before anyone else does

Build: add CI to the repository. From this week on, every change goes through a pull request, even though you work alone.

## Milestone 2

The repository has a green CI badge, a test suite and an architecture section in the README with a diagram of the layers. Pick one open source Flutter app, read one feature end to end, and write a page comparing its structure with yours.
