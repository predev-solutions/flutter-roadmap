# Phase 2 tasks (weeks 7 to 12)

These tasks break each week of [phase 2](../roadmap/02-production.md) into steps. Do them in order and tick each one when it works. A week is finished when every box is ticked and you pass the "Done when" check in the roadmap.

## Week 7: architecture

- [ ] 7.1 Draw the layers you are aiming for: UI, view models or blocs, repositories and services. Keep the drawing for the README.
- [ ] 7.2 Move the code into feature folders: catalogue, cart, favourites, auth and account.
- [ ] 7.3 Write a `ProductService` that owns the HTTP calls and returns raw data.
- [ ] 7.4 Write a `ProductRepository` interface and an implementation that turns raw data into models.
- [ ] 7.5 Give each screen a view model or bloc. Widgets only read state and send events.
- [ ] 7.6 Make the models immutable, with `freezed` or with hand-written `copyWith` and equality.
- [ ] 7.7 Provide the repositories through your state library or through constructors. Nothing creates its own dependencies.
- [ ] 7.8 Write a fake product repository that returns fixed data. Switch to it by changing one line.
- [ ] 7.9 Search the widget files for imports of your HTTP package. Remove every one.

## Week 8: state management in depth

- [ ] 8.1 Represent each async screen state with one type that covers loading, data, error and refreshing.
- [ ] 8.2 Add pull to refresh on the catalogue. The old data stays on screen while the new data loads.
- [ ] 8.3 Compute the cart total, the item count and the delivery fee from the cart items. Do not store them separately.
- [ ] 8.4 Build the address step of checkout with validation.
- [ ] 8.5 Build the delivery option step and the order summary.
- [ ] 8.6 Build the confirmation screen. Show it from a state change, not from the button handler.
- [ ] 8.7 Show a snackbar on a failed request once, even if the widget rebuilds.
- [ ] 8.8 Make cart changes optimistic: update the screen at once, send the request, and restore the previous cart if the request fails.
- [ ] 8.9 Keep the checkout input when the device rotates and when the user leaves checkout and comes back.
- [ ] 8.10 Check that each view model or bloc is disposed when its screen closes.

## Week 9: testing

- [ ] 9.1 Write unit tests for the product repository with a fake service.
- [ ] 9.2 Write unit tests for the cart logic: add, remove, change quantity, totals, and rollback after a failed request.
- [ ] 9.3 Write unit tests for the checkout view model, including the validation rules.
- [ ] 9.4 Write widget tests for the cart screen: empty, one item and many items.
- [ ] 9.5 Write widget tests for checkout: invalid input shows errors, and valid input reaches the summary.
- [ ] 9.6 Add golden tests for the catalogue and product details in light and dark themes.
- [ ] 9.7 Write one integration test: open the app, search, add to cart, check out and reach the confirmation screen.
- [ ] 9.8 Measure coverage with `flutter test --coverage` and raise the logic layer to 80% of lines.
- [ ] 9.9 Run the suite with the network off. Replace every real call with a fake.
- [ ] 9.10 Time the whole suite and bring it under two minutes.

## Week 10: offline and persistence

- [ ] 10.1 Add drift and define tables for products, favourites and orders.
- [ ] 10.2 Save the products you fetch to the database. The catalogue reads from the database.
- [ ] 10.3 Choose a cache strategy for the catalogue and one for product details. Write down why in a code comment or in your notes.
- [ ] 10.4 Show stale data at once and refresh it in the background.
- [ ] 10.5 Move favourites from `shared_preferences` to the database, with a migration that keeps the user's existing favourites.
- [ ] 10.6 Add a column to an existing table, write the schema migration and test it against the old schema.
- [ ] 10.7 Add a table for pending orders. An order placed offline goes there with a unique id generated on the device.
- [ ] 10.8 Send the pending orders when the connection returns. Use the unique id so an order that is retried is never created twice.
- [ ] 10.9 Show the user which orders are still waiting to be sent.
- [ ] 10.10 Add `flutter_secure_storage`. You store the auth tokens in it next week.

## Week 11: real backend and authentication

- [ ] 11.1 Choose Supabase, Firebase or your own API. Create products and orders in it.
- [ ] 11.2 Write new service classes for the backend. The repositories and everything above them stay unchanged.
- [ ] 11.3 Connect login, register and logout to the backend.
- [ ] 11.4 Store the access and refresh tokens in secure storage.
- [ ] 11.5 Add an interceptor that attaches the token to each request.
- [ ] 11.6 Refresh an expired token and repeat the failed request. Several requests that fail together must cause one refresh only.
- [ ] 11.7 Send the user to login when the refresh fails or the session is revoked. Clear their local data.
- [ ] 11.8 Add timeouts, retries with backoff for safe requests, and cancel a request when its screen closes.
- [ ] 11.9 Map server errors to a small set of app errors. The UI never shows a raw exception.
- [ ] 11.10 Add dev and production flavors with different app ids, names and API URLs. Install both on one phone.

## Week 12: tooling and CI

- [ ] 12.1 Add `flutter_lints` or `very_good_analysis` and stricter analysis options. Fix every warning.
- [ ] 12.2 Run `dart format` and `dart fix --apply` on the whole project and commit the result on its own.
- [ ] 12.3 Add a CI workflow that runs format check, analyze and tests on every pull request.
- [ ] 12.4 Cache the Flutter SDK and pub packages in CI to shorten each run.
- [ ] 12.5 Protect the main branch, so nothing merges while CI is red.
- [ ] 12.6 Add a pull request template with three questions: what changed, why, and how you tested it.
- [ ] 12.7 Make your next three changes as pull requests of under 300 changed lines each.
- [ ] 12.8 Review your own diff on GitHub before you merge. Leave comments on anything you would question in someone else's code.

## Milestone 2

- [ ] Add the CI badge to the README, and it is green.
- [ ] Add an architecture section to the README with the diagram of the layers.
- [ ] Pick one open source Flutter app and read one feature from the widget to the network call.
- [ ] Write one page that compares its structure with yours.
