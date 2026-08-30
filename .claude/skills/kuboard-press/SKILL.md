```markdown
# kuboard-press Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `kuboard-press` JavaScript codebase. You'll learn about file naming, import/export styles, commit message habits, and how to write and run tests. This guide is especially useful for contributors aiming for consistency and maintainability in their code.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myComponent.js`, `userProfile.test.js`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```javascript
    import { fetchData } from './apiUtils';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```javascript
    // In apiUtils.js
    export function fetchData() { ... }
    export const API_URL = '...';

    // In another file
    import { fetchData, API_URL } from './apiUtils';
    ```

### Commit Messages
- Commit messages are **freeform** (no enforced structure).
- Prefixes are not standardized.
- Average commit message length is **8 characters**.

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or utility.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `newFeature.js`).
2. Write your code using named exports.
3. Import dependencies using relative paths.
4. If applicable, create a corresponding test file (e.g., `newFeature.test.js`).
5. Commit your changes with a brief, descriptive message.

### Writing and Running Tests
**Trigger:** When you add or update functionality.
**Command:** `/run-tests`

1. Create a test file matching the pattern `*.test.js` (e.g., `apiUtils.test.js`).
2. Write your tests using the project's preferred testing framework (framework is currently unknown; check existing test files for patterns).
3. Run the tests using the project's test runner (consult project documentation or package.json for the command).

### Importing and Exporting Code
**Trigger:** When sharing code between modules.
**Command:** `/import-export`

1. Use named exports in your module files.
2. Import only the necessary functions or constants using relative paths.
3. Example:
    ```javascript
    // In mathUtils.js
    export function add(a, b) { return a + b; }

    // In another file
    import { add } from './mathUtils';
    ```

## Testing Patterns

- Test files follow the `*.test.js` naming convention.
- The testing framework is **unknown**; refer to existing test files for guidance.
- Place test files alongside the modules they test or in a dedicated test directory.

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-module    | Scaffold a new module with conventions       |
| /run-tests     | Run all project tests                        |
| /import-export | Example for proper importing/exporting       |
```
