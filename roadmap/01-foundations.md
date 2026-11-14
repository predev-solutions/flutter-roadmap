# Phase 1: foundations (weeks 1 to 6)

By the end of this phase you can build a small app on your own, from an empty folder to a release build on your phone. This is the junior level.

## Week 1: Dart

Topics

- Types, null safety, `final` and `const`
- Collections, collection `if` and `for`, spread
- Functions, closures, named and optional parameters
- Classes, constructors, mixins, extensions, enums
- Records, patterns and sealed classes
- `Future`, `async` and `await`, and a first look at `Stream`

Read the [language tour](https://dart.dev/language) from start to finish. It takes about two days and saves you weeks later.

Build: a command-line tool in plain Dart. It reads a JSON file of products, then filters, sorts and totals them based on arguments.

Done when: `dart analyze` reports nothing, the code has no `dynamic` and no `!` operator, and you can explain the difference between `final` and `const`.

## Week 2: widgets and layout

Topics

- `StatelessWidget`, `StatefulWidget` and `BuildContext`
- How layout works: [constraints go down, sizes go up, the parent sets the position](https://docs.flutter.dev/ui/layout/constraints)
- `Row`, `Column`, `Stack`, `Expanded`, `Flexible`, `Padding`, `SizedBox`
- `ListView.builder` and `GridView.builder`
- `ThemeData`, `ColorScheme` and Material 3

Build: start the shop app. Make a catalogue screen and a product details screen with hard-coded data.

Done when: nothing overflows on a 320 px wide screen or on a tablet, and every colour and text style comes from the theme.

## Week 3: navigation and forms

Topics

- [Navigation and routing](https://docs.flutter.dev/ui/navigation) with `go_router`
- Path parameters, redirects, nested navigation with a bottom bar
- `Form`, `TextFormField`, validators, `TextEditingController`
- Focus, keyboard actions and keyboard insets

Build: routes for catalogue, details, cart and account. Add login and register forms with validation. They do not call a server yet.

Done when: the Android back button behaves correctly on every screen, and the keyboard never covers the field you are typing in.

## Week 4: state

Topics

- `setState` and lifting state up
- `InheritedWidget`, `ValueNotifier` and `ChangeNotifier`, so you know what the libraries are built on
- One library: [Riverpod](https://riverpod.dev) or [Bloc](https://bloclibrary.dev)

Build: the cart. First build it with `ChangeNotifier` only. Then rebuild it with the library you chose.

Done when: adding an item updates the cart badge on every screen, and you can say which widgets rebuild when the cart changes and why.

## Week 5: networking and data

Topics

- [Fetching data](https://docs.flutter.dev/cookbook/networking/fetch-data) with `http` or `dio`
- JSON parsing with `json_serializable`
- Loading, empty and error states for every request
- Pagination and search with debounce
- Simple local storage with `shared_preferences`

Build: load products from [DummyJSON](https://dummyjson.com). Add infinite scroll, search and a favourites list that survives a restart.

Done when: the app shows a clear message and a retry button in airplane mode, and it never shows a blank screen or an endless spinner.

## Week 6: polish and first release

Topics

- Assets, fonts, app icon and splash screen
- Light and dark themes
- [Flutter DevTools](https://docs.flutter.dev/tools/devtools): the inspector and the logging view
- Debug, profile and release modes
- Building a signed release for Android, and for iOS if you have a Mac

Build: fix everything that feels rough. Write a README with screenshots and setup steps.

## Milestone 1

The app is installed on a real phone as a release build, and the code is public on your GitHub. Ask someone who is not a developer to use it for five minutes while you watch in silence. Write down everything that confused them and fix the top three.
