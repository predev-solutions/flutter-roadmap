<h1 align="center">Flutter roadmap: junior to senior in 24 weeks</h1>

<p align="center">
  A week-by-week plan for Flutter developers who want senior-level skills<br />
  and are willing to build a real app to get them.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-stable-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter stable" />
  <img src="https://img.shields.io/badge/Dart-3-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart 3" />
  <img src="https://img.shields.io/badge/duration-24%20weeks-7F75E8?style=for-the-badge" alt="24 weeks" />
  <img src="https://img.shields.io/badge/license-CC%20BY%204.0-0A0A0A?style=for-the-badge" alt="CC BY 4.0" />
</p>

Most Flutter roadmaps are a long list of topics with no order and no finish line. This one has both. It runs for 24 weeks, and every week ends with something you built and a check you can pass or fail.

We wrote it at [predev. Solutions](https://predevsolutions.com), a software house in Cairo that ships Flutter apps for clients and for our own products. The order of the weeks is the order we would want a new hire to learn things in.

## Who this is for

You can already program in some language, and you may have finished a Flutter tutorial or two. You want to reach the point where you can design an app, build it, release it, and help other developers do the same.

A senior title also takes years of shipped work, and no plan replaces that. What 24 weeks can give you is the full set of skills, each one practised at least once on a real project.

## How it works

Plan for 15 to 20 hours a week. With less time, stretch each week to two and keep the order.

Every week has three parts:

- Topics: what to study, with links to the official docs.
- Build: the work for that week, always on the same app.
- Done when: a check you can verify yourself. If you cannot pass it, repeat the week.

Each phase also has a task list in the [tasks](tasks) folder. It breaks every week into small steps you can tick off, and from phase 3 on each step is one pull request in your own repository.

Each phase ends with a milestone that you publish on your own GitHub.

## The four phases

| Phase | Weeks | Level you reach | You finish with |
|---|---|---|---|
| [1. Foundations](roadmap/01-foundations.md) | 1 to 6 | Junior | A working app installed on a real phone |
| [2. Production](roadmap/02-production.md) | 7 to 12 | Mid-level | A tested, offline-capable app with CI |
| [3. Depth](roadmap/03-depth.md) | 13 to 18 | Strong mid-level | A fast, accessible app in store testing |
| [4. Senior](roadmap/04-senior.md) | 19 to 24 | Senior skills | A design doc, a modular codebase and a published package |

## One app for all 24 weeks

You build a single shop app from week 2 to week 24: a product catalogue, search, a cart, checkout, order history and a user account. Each week adds a feature or forces you to rework something you wrote earlier.

Reworking old code is deliberate. A senior developer spends more time changing existing code than writing new code, and a fresh tutorial project every week never teaches that.

Phase 1 uses the free [DummyJSON](https://dummyjson.com) API, so you need no backend. From week 11 you connect a real one. Supabase, Firebase or your own API all work.

## Rules that make the plan work

1. Type the code yourself. Use AI tools to explain and review, and write the first version of everything by hand until phase 3.
2. Commit every day you work, with messages that say what changed.
3. Read the official docs first. Watch videos only when the docs leave you stuck.
4. Pick one state management library in week 4 and keep it. Switching libraries feels like progress and teaches little.
5. Test on a real device every week, and on a cheap Android phone if you can get one.
6. Write a short note at the end of each week: what you built, what confused you, what you would do differently.

## Main references

- [Dart language tour](https://dart.dev/language)
- [Effective Dart](https://dart.dev/effective-dart)
- [Flutter documentation](https://docs.flutter.dev)
- [Flutter app architecture guide](https://docs.flutter.dev/app-architecture)
- [Flutter testing overview](https://docs.flutter.dev/testing/overview)
- [Flutter performance](https://docs.flutter.dev/perf)
- [pub.dev](https://pub.dev)

## Contributing

Open an issue if a link is dead, a week is unclear, or the order is wrong for a reason you can explain. Pull requests are welcome for corrections. For a new topic, open an issue first so we can decide which week it replaces. The plan stays at 24 weeks.

## License

The text is licensed under [CC BY 4.0](LICENSE). You can copy, translate and adapt it, including for paid courses, as long as you credit predev. Solutions and link back to this repository.

<p align="center">
  Made in Cairo by <a href="https://predevsolutions.com">predev. Solutions</a>
</p>
