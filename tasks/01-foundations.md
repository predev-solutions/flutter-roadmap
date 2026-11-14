# Phase 1 tasks (weeks 1 to 6)

These tasks break each week of [phase 1](../roadmap/01-foundations.md) into steps. Do them in order and tick each one when it works on a real device. A week is finished when every box is ticked and you pass the "Done when" check in the roadmap.

## Week 1: Dart

- [ ] 1.1 Create a Dart console project with `dart create` and turn on strict analysis in `analysis_options.yaml`.
- [ ] 1.2 Write a `products.json` file with at least 20 products: id, title, price, category, rating and stock.
- [ ] 1.3 Model a product as an immutable class with a `fromJson` factory. Throw a clear error when a field is missing or has the wrong type.
- [ ] 1.4 Read the file path from the command-line arguments, load the file with `async` and `await`, and print a helpful message when the file does not exist.
- [ ] 1.5 Add `--category`, `--min-price` and `--max-price` filters.
- [ ] 1.6 Add `--sort` with the values `price`, `rating` and `title`, and a `--desc` flag.
- [ ] 1.7 Add a `--total` flag that prints the stock value (price times stock) for each category, returned from a function as a record.
- [ ] 1.8 Model the parsed command as a sealed class and handle it with a `switch` expression, so the compiler tells you when a case is missing.
- [ ] 1.9 Remove every `dynamic` and every `!` from the code. Run `dart analyze` until it reports nothing.
- [ ] 1.10 Write five lines in your notes on the difference between `final` and `const`, with one example of each from your own code.

## Week 2: widgets and layout

- [ ] 2.1 Create the shop app with `flutter create` and run it on a real phone.
- [ ] 2.2 Define a `ThemeData` with a `ColorScheme` built from one seed colour and a text theme. Use Material 3.
- [ ] 2.3 Add a hard-coded list of 20 products in its own file.
- [ ] 2.4 Build a product card as a `StatelessWidget`: image, title, price and rating.
- [ ] 2.5 Build the catalogue screen with `GridView.builder`. Show two columns on a phone and more on a wider screen.
- [ ] 2.6 Build the product details screen: large image, title, price, description and an "Add to cart" button that does nothing yet.
- [ ] 2.7 Open the details screen when a card is tapped. Plain `Navigator.push` is enough this week.
- [ ] 2.8 Test at 320 px wide and on a tablet size. Fix every overflow warning.
- [ ] 2.9 Search the code for `Color(`, `Colors.` and `TextStyle(`. Replace each one with a value from the theme.

## Week 3: navigation and forms

- [ ] 3.1 Add `go_router` and define routes for catalogue, product details, cart and account.
- [ ] 3.2 Pass the product id as a path parameter, so `/product/7` opens product 7.
- [ ] 3.3 Add a bottom navigation bar with nested navigation. Each tab keeps its own stack and scroll position.
- [ ] 3.4 Build the login form with email and password fields, validators and an error message under each field.
- [ ] 3.5 Build the register form with name, email, password and password confirmation. The two passwords must match.
- [ ] 3.6 Set the keyboard action on every field. "Next" moves the focus to the following field, and "Done" submits the form.
- [ ] 3.7 Make both forms scroll, so the keyboard never covers the field in focus.
- [ ] 3.8 Add a redirect that sends a logged-out user from the account tab to login. A boolean in memory is enough for the logged-in state.
- [ ] 3.9 Press the Android back button on every screen and inside every tab. Fix each case that closes the app or lands on the wrong screen.

## Week 4: state

- [ ] 4.1 Add a quantity selector to the details screen with `setState`.
- [ ] 4.2 Write a `CartModel` that extends `ChangeNotifier` with add, remove, change quantity and a total.
- [ ] 4.3 Share the cart with the widget tree through an `InheritedNotifier` that you write yourself, without a package.
- [ ] 4.4 Build the cart screen: the list of items, quantity controls, the total and an empty state.
- [ ] 4.5 Show a badge with the item count on the cart tab. It updates from every screen.
- [ ] 4.6 Choose Riverpod or Bloc. Write down in two sentences why you chose it.
- [ ] 4.7 Rebuild the cart with the library on a new branch. Delete the `ChangeNotifier` version when the new one behaves the same.
- [ ] 4.8 Add a `debugPrint` to the `build` method of the card, the badge and the cart screen. Add an item, then write down which widgets rebuilt and why.
- [ ] 4.9 Reduce the rebuilds, so adding an item no longer rebuilds the whole catalogue.

## Week 5: networking and data

- [ ] 5.1 Add `http` or `dio` and fetch the first page of products from DummyJSON.
- [ ] 5.2 Generate the JSON code for the product model with `json_serializable`.
- [ ] 5.3 Show a loading state, an empty state and an error state with a retry button on the catalogue.
- [ ] 5.4 Add infinite scroll with the `limit` and `skip` parameters. Show a loader at the end of the list and stop when no products are left.
- [ ] 5.5 Add a search field that waits 400 ms after the last key press before it sends a request.
- [ ] 5.6 Ignore the response of an old search when a newer search has already started.
- [ ] 5.7 Load the product details by id, so a link to `/product/7` works without visiting the catalogue first.
- [ ] 5.8 Add a favourite button and a favourites screen. Store the ids with `shared_preferences`.
- [ ] 5.9 Turn on airplane mode and open every screen. Each one must show a message and a retry button.

## Week 6: polish and first release

- [ ] 6.1 Add an app icon and a splash screen.
- [ ] 6.2 Add a custom font and declare your assets in `pubspec.yaml`.
- [ ] 6.3 Add a dark theme and a setting to switch between light, dark and system.
- [ ] 6.4 Check every screen in dark mode. Fix text that is hard to read and images that look wrong.
- [ ] 6.5 Open DevTools. Use the inspector to find one layout problem and fix it.
- [ ] 6.6 Run the app in profile mode and in release mode. Note what is different from debug mode.
- [ ] 6.7 Create an upload keystore, configure signing and build a signed Android release. Keep the keystore and its passwords out of git.
- [ ] 6.8 Build for iOS too, if you have a Mac.
- [ ] 6.9 Write the README: what the app does, screenshots in light and dark, and setup steps that work on a clean machine.

## Milestone 1

- [ ] Install the release build on a real phone.
- [ ] Push the code to a public repository on your GitHub.
- [ ] Watch someone who is not a developer use the app for five minutes without helping them.
- [ ] Write down everything that confused them, then fix the top three problems.
