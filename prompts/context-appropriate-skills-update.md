# Context appropriate skills update prompt

## Prompt

```
Can you update llm context.md/appropriate skills to:

- leave minimal comments when writing code; only describe why, and only when necessary. We should rely on descriptive names and obvious call patterns.
- Utilize modern software principles, like SOLID, DRY, clean architecture, and design patterns.
- Try to utilize the available tooling, patterns, and techniques - if there are common, repetitive patterns, build leightweight (ideally value-typed, or function-based, with minimal or no allocation) common abstractions so the entire codebase can benefit
- If we have to use "#defines", they should be within the namespace, consistently
- Try to consolidate/architect/abstract common code - we should rarely, if ever, duplicate code, unless absolutely necessary.

This applies for all code - production, editor, inspector, test, etc
```

## Prompt

```
Can you update llm context.md/appropriate skills to:

- leave minimal comments when writing code; only describe why, and only when necessary. We should rely on descriptive names and obvious call patterns.
- Utilize modern software principles, like SOLID, DRY, clean architecture, and design patterns.
- Try to utilize the available tooling, patterns, and techniques - if there are common, repetitive patterns, build leightweight (ideally value-typed, or function-based, with minimal or no allocation) common abstractions so the entire codebase can benefit
- If we have to use "#defines", they should be within the namespace, consistently
- Try to consolidate/architect/abstract common code - we should rarely, if ever, duplicate code, unless absolutely necessary.

This applies for all code - production, editor, inspector, test, etc
```

## Comments

-
