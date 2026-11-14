# Phase 4 tasks (weeks 19 to 24)

These tasks break each week of [phase 4](../roadmap/04-senior.md) into steps. Code tasks are pull requests in your own repository, as in phase 3. Documents live in a `docs` folder in the same repository and go through pull requests too. A week is finished when every box is ticked and you pass the "Done when" check in the roadmap.

## Week 19: system design for mobile

- [ ] 19.1 Choose the feature: multi-vendor orders, live order tracking or one of your own of similar size.
- [ ] 19.2 Write the scope: what the feature does, what it does not do, and the questions you would ask a product owner.
- [ ] 19.3 Design the data model on the server and on the device.
- [ ] 19.4 Write the API contract: endpoints, pagination, error format and versioning.
- [ ] 19.5 Describe the offline behaviour and the sync: what works offline, how conflicts are resolved, and which requests are idempotent.
- [ ] 19.6 List the failure cases and what the user sees in each one.
- [ ] 19.7 Write the rollout plan: feature flag, staged rollout, and how you would roll back.
- [ ] 19.8 State the trade-offs: what you left out, what it saves in time and cost, and what risk it adds.
- [ ] 19.9 Cut the document to under six pages.
- [ ] 19.10 Give it to another developer and ask for an estimate. Each question they ask is a gap in the document, so fix it.

## Week 20: scaling the codebase

- [ ] 20.1 Set up a pub workspace or Melos at the root of the repository.
- [ ] 20.2 Extract a `core` package: networking, storage, error types and shared utilities.
- [ ] 20.3 Extract a design system package with colour, spacing and type tokens, and the shared components.
- [ ] 20.4 Move the catalogue feature into its own package.
- [ ] 20.5 Move the cart and checkout features into their own packages.
- [ ] 20.6 Move the auth and account features into their own packages.
- [ ] 20.7 Remove every import from one feature to another. Features communicate through interfaces in `core` or through the app that composes them.
- [ ] 20.8 Add a check that fails the build on a forbidden import.
- [ ] 20.9 Change CI so a change in one package analyzes and tests only that package and the packages that depend on it.
- [ ] 20.10 Write a one-page guide for upgrading Flutter and for adding a third-party package, with the checks you run before you accept one.

## Week 21: quality at scale

- [ ] 21.1 Write a one-page test strategy: what unit, widget, golden and integration tests are for in this app, and what you choose not to test.
- [ ] 21.2 Run the test suite 20 times in CI. Fix every test that failed at least once.
- [ ] 21.3 Add a remote feature flag service and put one feature behind a flag.
- [ ] 21.4 Turn the feature off remotely and confirm it disappears without a new release.
- [ ] 21.5 Add an app size check to CI that fails when the release build passes the limit you set.
- [ ] 21.6 Add a startup time or frame time check to CI, if your setup allows it.
- [ ] 21.7 Set up alerts for a jump in the crash rate.
- [ ] 21.8 Practise a staged rollout and a rollback on the testing channel.
- [ ] 21.9 Write a one-page incident runbook: who decides, how to turn a feature off, how to roll back, and what to tell users.

## Week 22: the framework and open source

- [ ] 22.1 Read the source of `InheritedWidget`, `Navigator` or `ListView`. Write half a page on how it works.
- [ ] 22.2 Read three merged pull requests in the Flutter repository, and its contributing guide.
- [ ] 22.3 Choose one path: publish your own package, or contribute to Flutter or to a package you use.
- [ ] 22.4 Package path: extract the code into a package with a small, documented public API.
- [ ] 22.5 Package path: add an example, tests, a README, a changelog and a license.
- [ ] 22.6 Package path: run `dart pub publish --dry-run`, fix what it reports, then publish.
- [ ] 22.7 Package path: check the score on pub.dev and fix what lowers it.
- [ ] 22.8 Contribution path: find an issue the maintainers have accepted, and say in the issue that you are working on it.
- [ ] 22.9 Contribution path: open the pull request with tests, and answer the review until it is merged.

## Week 23: leading

- [ ] 23.1 Review a pull request in an open source project. Ask questions, give the reason behind each suggestion, and say which comments are only taste.
- [ ] 23.2 Review a second pull request in a different project.
- [ ] 23.3 Review a third.
- [ ] 23.4 Write an architecture decision record for your state management choice.
- [ ] 23.5 Write a decision record for your offline and sync design.
- [ ] 23.6 Write a decision record for how you split the app into packages.
- [ ] 23.7 List the technical debt in the app. For each item, write its cost today and what would make you pay it off.
- [ ] 23.8 Estimate the feature from your week 19 design document in days, with the three biggest risks.
- [ ] 23.9 Explain one technical trade-off from your app in writing for a reader who is not an engineer, in under 200 words.
- [ ] 23.10 Teach one topic from this roadmap to a junior developer for an hour. A week later, check that they can do it without you.

## Week 24: capstone

- [ ] 24.1 Close or deliberately defer every open issue in your repository.
- [ ] 24.2 Ship a final release through your pipeline.
- [ ] 24.3 Update the README, so a new developer can run and understand the project in 30 minutes.
- [ ] 24.4 Choose the hardest problem you solved in these 24 weeks.
- [ ] 24.5 Prepare a 20-minute talk or a written post about it: the problem, what you tried, what worked and what you would do differently.
- [ ] 24.6 Give the talk to at least one other developer, or publish the post.
- [ ] 24.7 Go through the [senior checklist](../roadmap/04-senior.md#senior-checklist). For each box you cannot tick, write the task that would let you tick it.
