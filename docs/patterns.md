# Patterns & Language Notes

Companion to `CODING_STANDARDS.md`. Remove sections irrelevant to your stack.
Expand with project-specific conventions as they emerge.

---

## JavaScript / TypeScript

- Prefer `const`; use `let` only when mutation is necessary; never `var`
- Explicit return types on exported functions
- Avoid `any` — use `unknown` + narrowing if the type is genuinely unknown
- Async: `async/await` over raw Promises; always handle rejection
- Prefer named exports over default exports (easier to grep, rename-safe)

```ts
// ✅
export async function getUserById(id: string): Promise<User | null> {
  const row = await db.users.findOne({ id });
  return row ?? null;
}

// ❌ — implicit return type, default export, swallowed error
export default async (id) => {
  try { return await db.users.findOne({ id }); } catch {}
}
```

## Python

- Type hints on all function signatures
- Dataclasses or Pydantic for data shapes — no raw dicts as function contracts
- Raise specific exceptions; never `except Exception: pass`
- One module = one cohesive responsibility; `__init__.py` re-exports public API only

```python
# ✅
def get_user_by_id(user_id: str) -> User | None:
    return db.users.get(user_id)

# ❌ — no type hints, swallowed exception
def get_user(id):
    try:
        return db.users.get(id)
    except:
        pass
```

## CSS / Styling

- Utility-first (Tailwind) or CSS Modules — no global class name soup
- Design tokens for color, spacing, type — no raw hex values in components
- Mobile-first breakpoints

---

## Testing Patterns

### Unit tests
Test one function in isolation. Mock I/O at the boundary, not inside logic.

### Integration tests
Test that modules compose correctly. Use real implementations where cheap;
mocks where slow or flaky (network, DB).

### What NOT to test
- Framework boilerplate
- Private implementation details
- Anything that would break on a pure refactor without changing behavior

---

## Architecture Decision Records (ADRs)

When a significant technical decision is made, add an ADR:

```
/docs/adr/
  001-use-postgres-over-sqlite.md
  002-adopt-tailwind.md
```

Template:
```md
# ADR-NNN: [Decision]
**Status:** Accepted | Superseded by ADR-NNN
**Context:** What problem are we solving?
**Decision:** What did we choose and why?
**Consequences:** What tradeoffs does this create?
```
