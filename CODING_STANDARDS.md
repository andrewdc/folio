# Coding Standards

Four principles, in priority order: **Readability → Simplicity → Modularity → Testability**

---

## Readability

- Name things for what they *are*, not how they *work*. (`getUserById`, not `fetchData2`)
- Avoid abbreviations unless universally understood (`id`, `url`, `ctx` — fine; `usrMgr` — no)
- One idea per line; one responsibility per function
- Prefer explicit over clever; never sacrifice clarity for brevity
- Comments explain *why*, not *what*. Delete comments that restate the code.

## Simplicity

- Solve the problem in front of you. Don't abstract until you have 3 real use cases.
- Prefer flat over nested; early returns over deep conditionals
- No premature optimization. Profile before you tune.
- If a solution feels complex, that's a signal to rethink the problem, not add more code.
- Delete code that isn't used. Dead code is a lie.

## Modularity

- A module (function, class, file, service) does one thing and does it well
- Modules depend on interfaces, not implementations
- File/directory structure mirrors domain structure, not framework structure
- Co-locate related things; separate things that change for different reasons
- Keep files under ~200 lines. If it's growing, it's splitting.

## Testability

- Pure functions by default — side effects at the edges
- Inject dependencies; don't reach for globals or singletons from inside logic
- Tests live next to the code they test (`foo.js` → `foo.test.js`)
- Test behavior, not implementation. Tests should survive a refactor.
- A test that's hard to write is feedback: the code needs to change, not the test.

---

## Language-Agnostic Conventions

- Consistent formatting is non-negotiable — use the project's linter/formatter, no exceptions
- Commits are atomic and descriptive (`fix: null check in getUserById`, not `stuff`)
- Environment-specific config lives in env vars, never in code
- Errors are explicit. Never silently swallow exceptions.

## File & Directory Layout

```
/src
  /domain-or-feature/
    index.{ext}         ← public interface
    module.{ext}        ← implementation
    module.test.{ext}   ← tests alongside code
/docs                   ← expanded specs, ADRs, diagrams
```

See [`/docs/patterns.md`](./docs/patterns.md) for language-specific examples and preferred patterns.
