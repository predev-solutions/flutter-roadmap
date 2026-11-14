# Phase 4: senior (weeks 19 to 24)

The first three phases were about your own code. This one is about decisions that affect a team: how an app is designed before anyone writes it, how a codebase stays healthy as it grows, and how you make other developers better.

Each week below has a matching task list in [tasks/04-senior.md](../tasks/04-senior.md) that breaks the build into small steps.

## Week 19: system design for mobile

Topics

- Turning vague requirements into a written scope with clear limits
- API contracts: pagination, errors, versioning and what the client needs from the backend
- Sync design: conflict resolution, idempotent requests and retries
- Trade-offs you must state openly: cost, time, risk and what you chose to leave out

Build: write a design document for a feature the app lacks, such as multi-vendor orders or live order tracking. Cover the data model, API, offline behaviour, failure cases and a rollout plan. Keep it under six pages.

Done when: another developer can read the document and estimate the work without asking you a question.

## Week 20: scaling the codebase

Topics

- Splitting an app into packages, with [pub workspaces](https://dart.dev/tools/pub/workspaces) or Melos
- Dependency rules between features, and how to enforce them
- A design system package with tokens and shared components
- Choosing third-party packages and planning Flutter upgrades

Build: split the shop app into packages: core, design system and one package per feature. Features must not import each other.

Done when: a change inside one feature rebuilds and retests only that package in CI, and a forbidden import fails the build.

## Week 21: quality at scale

Topics

- A test strategy: what each kind of test is for and what you choose not to test
- Finding and fixing flaky tests
- Performance budgets checked in CI
- Feature flags, staged rollouts and rollback
- Monitoring, alerts and what to do in the first hour of an incident

Build: put one feature behind a remote flag, add an app size check to CI, and write an incident runbook of one page.

Done when: you can turn the feature off for all users without a new release, and CI fails when the app grows past the size you set.

## Week 22: the framework and open source

Topics

- Reading the Flutter source: start with `ListView`, `Navigator` or `InheritedWidget`
- How Flutter issues, pull requests and breaking changes are handled
- [Publishing a package](https://dart.dev/tools/pub/publishing) with docs, an example and a changelog

Build: publish a package to pub.dev, extracted from something you built in phases 2 or 3. Or get a pull request merged in Flutter or in a package you use.

Done when: the package scores well on pub.dev's own checks, or the pull request is merged.

## Week 23: leading

Topics

- Code review that teaches: asking questions, explaining reasons, separating taste from defects
- Estimating work and reporting risk early
- Technical debt: tracking it and deciding when to pay it
- Architecture decision records
- Explaining a technical trade-off to someone who is not an engineer

Build: review three pull requests in open source projects with comments a maintainer would thank you for. Write decision records for the three biggest choices in your app. Teach one topic from this roadmap to a junior developer for an hour.

Done when: the person you taught can do the thing without you.

## Week 24: capstone

Build: a final release of the shop app, and a 20-minute talk or a written post about the hardest problem you solved in these 24 weeks. Then go through the checklist below and be strict with yourself.

## Senior checklist

You are working at a senior level when you can do all of these without help.

- [ ] Start a project from zero and justify its structure in writing
- [ ] Explain why a screen is slow using profiler data, and fix it
- [ ] Design offline behaviour and sync for a feature, including the failure cases
- [ ] Write native code on Android and iOS when a plugin does not exist
- [ ] Ship an app in two languages, one of them right-to-left, that passes an accessibility check
- [ ] Release to both stores from CI, and roll back a bad release
- [ ] Split a codebase into modules and keep the boundaries enforced
- [ ] Write a design document that others can build from
- [ ] Review code in a way that improves the author and the code
- [ ] Say what you would cut when the deadline moves, and what that costs

Any box you cannot tick is your next week of work.
