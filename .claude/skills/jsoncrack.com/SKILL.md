```markdown
# jsoncrack.com Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `jsoncrack.com` codebase, a TypeScript project with no detected framework. You'll learn about file naming, import/export styles, commit patterns, and how to write and run tests in this repository.

## Coding Conventions

### File Naming
- Use **camelCase** for filenames.
  - Example: `jsonParser.ts`, `dataVisualizer.ts`

### Import Style
- Use **relative imports** for modules.
  - Example:
    ```typescript
    import { parseJson } from './jsonParser';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // In jsonParser.ts
    export function parseJson(data: string) { /* ... */ }

    // In another file
    import { parseJson } from './jsonParser';
    ```

### Commit Patterns
- Commit messages are **freeform** with no strict prefixes.
- Average commit message length is short (~11 characters).

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new functionality or feature.
**Command:** `/add-module`

1. Create a new file using camelCase (e.g., `newFeature.ts`).
2. Use relative imports to include dependencies.
3. Export functions or constants using named exports.
4. Write corresponding tests in a `*.test.*` file.
5. Commit with a concise, descriptive message.

### Writing Tests
**Trigger:** When you add or modify code that requires testing.
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.*` (e.g., `jsonParser.test.ts`).
2. Write test cases for your module.
3. Use the project's preferred (unknown) testing framework.
4. Run tests to ensure correctness.

### Refactoring Code
**Trigger:** When you need to improve or restructure existing code.
**Command:** `/refactor`

1. Update code while maintaining camelCase file naming.
2. Keep using relative imports and named exports.
3. Update or add tests as needed.
4. Commit with a clear, concise message.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `dataVisualizer.test.ts`).
- The specific testing framework is unknown, but tests are colocated with source files or in a similar directory structure.
- Example test file:
  ```typescript
  // jsonParser.test.ts
  import { parseJson } from './jsonParser';

  test('parses valid JSON', () => {
    expect(parseJson('{"a":1}')).toEqual({ a: 1 });
  });
  ```

## Commands
| Command       | Purpose                                      |
|---------------|----------------------------------------------|
| /add-module   | Scaffold and implement a new module          |
| /write-test   | Create and run tests for a module            |
| /refactor     | Refactor code following project conventions  |
```