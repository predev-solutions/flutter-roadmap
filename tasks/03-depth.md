# Phase 3 tasks (weeks 13 to 18)

These tasks break each week of [phase 3](../roadmap/03-depth.md) into steps. From this phase on, every task is one pull request in your own repository, with CI green before you merge. A week is finished when every box is ticked and you pass the "Done when" check in the roadmap.

## Week 13: rendering and performance

- [ ] 13.1 Run the app in profile mode on a low-end Android phone. Record a scroll of the catalogue with the DevTools performance view.
- [ ] 13.2 Write down the starting numbers: release app size, startup time and the three slowest frames.
- [ ] 13.3 Find the cause of each slow frame in the timeline: build, layout, paint or raster.
- [ ] 13.4 Fix the first cause and record the scroll again. Repeat for the second and the third.
- [ ] 13.5 Add `const` constructors where the analyzer allows them, and stable keys to list items that move or get removed.
- [ ] 13.6 Wrap one widget that repaints often in a `RepaintBoundary`. Confirm the effect with the repaint rainbow.
- [ ] 13.7 Resize images to the size they are displayed at. Check the memory view before and after.
- [ ] 13.8 Run `flutter build apk --analyze-size` and remove the largest thing you do not need.
- [ ] 13.9 Measure the time to the first frame and remove work from startup that can wait.
- [ ] 13.10 Add a performance section to the README with the numbers before and after.

## Week 14: advanced UI and animation

- [ ] 14.1 Rebuild the product details screen with `CustomScrollView` and a collapsing header that shows the product image.
- [ ] 14.2 Add a pinned header for the category filters on the catalogue.
- [ ] 14.3 Draw the order history chart with `CustomPainter`: axes, bars or a line, and labels.
- [ ] 14.4 Make the chart respond to a tap by showing the value of that point.
- [ ] 14.5 Build one custom layout with `CustomMultiChildLayout` or a `RenderObject`, for example a badge placed relative to a child of unknown size.
- [ ] 14.6 Add a `Hero` animation from the product card to the details image.
- [ ] 14.7 Build the add-to-cart animation with an explicit `AnimationController`. The product flies to the cart icon and the badge bumps.
- [ ] 14.8 Add a staggered entrance animation to the confirmation screen.
- [ ] 14.9 Build a tablet layout with the catalogue and the details side by side.
- [ ] 14.10 Check each animation in profile mode and fix any that drops frames.

## Week 15: async and concurrency

- [ ] 15.1 Generate a JSON file with 10,000 products. Parse it on the main isolate and measure how long the UI freezes.
- [ ] 15.2 Move the parsing to `Isolate.run` and measure again.
- [ ] 15.3 Let the user choose a profile photo. Resize and compress it in an isolate before upload.
- [ ] 15.4 Write a small demo that prints the order of a sync call, a microtask, a `Future` and a timer. Predict the output before you run it.
- [ ] 15.5 Expose the connection status as a broadcast stream, with a transformer that ignores quick changes.
- [ ] 15.6 List every stream subscription and controller in the app. Cancel or close each one when its owner is disposed.
- [ ] 15.7 Add background sync for the offline order queue with a package such as `workmanager`.
- [ ] 15.8 Test the background sync with the app closed, on Android and on iOS. Write down what each platform allows and how long it waits.

## Week 16: platform integration

- [ ] 16.1 Create a plugin package for one native API, such as battery level or device storage.
- [ ] 16.2 Define the plugin's interface with Pigeon and generate the code.
- [ ] 16.3 Implement the Android side in Kotlin.
- [ ] 16.4 Implement the iOS side in Swift.
- [ ] 16.5 Add an example app to the plugin, and tests for the Dart side.
- [ ] 16.6 Call one C function from Dart with `dart:ffi`. A function from the C standard library is enough.
- [ ] 16.7 Request the notification permission at a moment that makes sense to the user, and handle a refusal.
- [ ] 16.8 Add push notifications for order status changes. Tapping one opens that order.
- [ ] 16.9 Add deep links for products with Android App Links and iOS Universal Links.
- [ ] 16.10 Test a product link in three cases: app closed, app in the background and app open.

## Week 17: localization, RTL and accessibility

- [ ] 17.1 Set up `flutter_localizations` and ARB files. Move every string in the app into them.
- [ ] 17.2 Add the Arabic translation.
- [ ] 17.3 Add plurals for item counts, and format prices and dates for each locale.
- [ ] 17.4 Add a language switch inside the app that works without a restart and is remembered.
- [ ] 17.5 Replace `EdgeInsets` with `EdgeInsetsDirectional` and `Alignment` with `AlignmentDirectional` wherever left and right matter.
- [ ] 17.6 Mirror the icons that point in a direction, such as back arrows. Leave the others as they are.
- [ ] 17.7 Open every screen in Arabic and fix what breaks, including the chart and the animations.
- [ ] 17.8 Add semantic labels to icon buttons and images. Hide decorative elements from the screen reader.
- [ ] 17.9 Set the largest system font and fix every screen that overflows or cuts text.
- [ ] 17.10 Check contrast and tap target sizes with the accessibility guideline tests in a widget test.
- [ ] 17.11 Complete a purchase with TalkBack or VoiceOver on and your eyes closed. Fix each point where you got stuck.

## Week 18: security and release

- [ ] 18.1 List every secret the app uses. Move out of the app any secret that must not ship in a client.
- [ ] 18.2 Add certificate pinning for your API, and write down how you will rotate the certificate.
- [ ] 18.3 Build the release with obfuscation and keep the symbol files.
- [ ] 18.4 Add Sentry or Firebase Crashlytics and upload the symbol files, so stack traces are readable.
- [ ] 18.5 Take the version name and build number from the git tag.
- [ ] 18.6 Store the signing keys as CI secrets.
- [ ] 18.7 Write a release workflow that starts on a git tag, builds the signed app and uploads it to Play internal testing.
- [ ] 18.8 Add TestFlight to the workflow, if you have an Apple developer account.
- [ ] 18.9 Fill in the store listing, the privacy forms and the data safety section.

## Milestone 3

- [ ] Push a tag and watch the build reach testers without a manual step on your laptop.
- [ ] Get at least three people to install the app from the store's testing channel.
- [ ] Trigger a crash on purpose and find it in your crash dashboard with a readable stack trace.
