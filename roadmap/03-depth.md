# Phase 3: depth (weeks 13 to 18)

Mid-level developers can use Flutter. In this phase you learn how it works underneath, which is what you need when a screen is slow, a design has no ready-made widget, or a feature needs native code.

Each week below has a matching task list in [tasks/03-depth.md](../tasks/03-depth.md) that breaks the build into small steps.

## Week 13: rendering and performance

Topics

- The widget, element and render object trees
- Build, layout and paint, and what triggers each
- Keys, `const` constructors and `RepaintBoundary`
- The [performance docs](https://docs.flutter.dev/perf) and the DevTools performance and memory views
- Impeller, shader jank, app size and startup time

Build: profile the shop app in profile mode on a low-end Android phone. Find the three worst frames and fix their causes. Measure app size and startup time before and after.

Done when: the catalogue scrolls without dropped frames on that phone, and you have written down numbers for size and startup that you can defend.

## Week 14: advanced UI and animation

Topics

- Slivers and `CustomScrollView`
- `CustomPainter` and custom layout with `CustomMultiChildLayout` or a `RenderObject`
- [Animations](https://docs.flutter.dev/ui/animations): implicit, explicit, `Hero` and staggered
- Adaptive layouts for tablets, foldables and the web

Build: a collapsing product header with slivers, a hand-drawn chart of order history with `CustomPainter`, and an add-to-cart animation.

Done when: every animation holds a steady frame rate in profile mode, and the layout uses the extra space on a tablet instead of stretching the phone layout.

## Week 15: async and concurrency

Topics

- The event loop, microtasks and why a long sync loop freezes the UI
- [Isolates](https://dart.dev/language/isolates) and `Isolate.run`
- Streams in depth: controllers, broadcast streams, transformers, cancellation
- Background work on Android and iOS and its limits

Build: move JSON parsing of the full catalogue and image processing for the profile photo to isolates. Add a background sync for the offline order queue.

Done when: the UI stays responsive while 10,000 products are parsed, and every stream subscription in the app is cancelled when its owner is disposed.

## Week 16: platform integration

Topics

- [Platform channels](https://docs.flutter.dev/platform-integration/platform-channels) and type-safe channels with Pigeon
- Calling C code through `dart:ffi`
- Writing a plugin package
- Permissions, push notifications and deep links

Build: write a small plugin of your own that exposes one native API on Android and iOS. Add push notifications for order status and a deep link that opens a product.

Done when: a link tapped in another app opens the right product whether your app was closed, in the background or open, and your plugin has an example app and tests.

## Week 17: localization, RTL and accessibility

Topics

- [Internationalization](https://docs.flutter.dev/ui/internationalization) with ARB files, plurals and date and number formats
- Right-to-left layout: `Directionality`, `EdgeInsetsDirectional`, `AlignmentDirectional` and mirrored icons
- [Accessibility](https://docs.flutter.dev/ui/accessibility): semantics, screen readers, text scaling, contrast and tap target size

Build: add Arabic next to English, with language switching inside the app. Then use the whole app with TalkBack or VoiceOver and with the largest system font.

Done when: no screen breaks in Arabic or at the largest font size, and you can complete a purchase with the screen reader on and your eyes closed.

## Week 18: security and release

Topics

- Where secrets can and cannot live in a mobile app
- Secure storage, certificate pinning and code obfuscation
- Signing, versioning and build numbers
- Automated releases with Fastlane, Codemagic or GitHub Actions
- Crash reporting with Sentry or Firebase Crashlytics
- Store listings, review rules and privacy forms

Build: a release pipeline that turns a git tag into a build in Play internal testing, and in TestFlight if you have an Apple developer account.

## Milestone 3

A tagged release reaches testers without any manual step on your laptop. At least three people install it from the store's testing channel, and a crash you trigger on purpose shows up in your crash dashboard with a readable stack trace.
