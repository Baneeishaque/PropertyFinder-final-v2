```markdown
# PropertyFinder-final-v2 Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the PropertyFinder-final-v2 repository, a TypeScript React project. You'll learn about file naming, import/export styles, commit message patterns, and testing conventions, enabling you to contribute code that fits seamlessly with the existing codebase.

## Coding Conventions

### File Naming
- **Style:** camelCase
- **Example:**  
  - `propertyList.tsx`
  - `searchBar.tsx`

### Import Style
- **Style:** Relative imports
- **Example:**
  ```typescript
  import { PropertyCard } from './propertyCard';
  import { useSearch } from '../hooks/useSearch';
  ```

### Export Style
- **Style:** Named exports
- **Example:**
  ```typescript
  // In propertyCard.tsx
  export const PropertyCard = () => { ... };
  ```

### Commit Patterns
- **Type:** Freeform (no enforced structure)
- **Prefixes:** None required
- **Average length:** 41 characters
- **Example:**
  ```
  Fix bug in property filtering logic
  Add loading spinner to search results
  ```

## Workflows

### Adding a New Component
**Trigger:** When you need to add a new UI or logic component.
**Command:** `/add-component`

1. Create a new file using camelCase (e.g., `myComponent.tsx`).
2. Use relative imports for dependencies.
3. Export your component using a named export.
4. Write a corresponding test file if applicable (e.g., `myComponent.test.tsx`).
5. Commit your changes with a concise, descriptive message.

### Modifying Existing Logic
**Trigger:** When updating or fixing code in existing files.
**Command:** `/modify-logic`

1. Locate the relevant file using camelCase naming.
2. Make your changes, maintaining the relative import and named export conventions.
3. Update or add tests if necessary.
4. Commit your changes with a clear, descriptive message.

### Writing Tests
**Trigger:** When adding or updating tests for components or logic.
**Command:** `/write-test`

1. Create or update a test file matching the pattern `*.test.*` (e.g., `propertyList.test.tsx`).
2. Use the project's preferred testing framework (framework not specified).
3. Ensure tests cover the main functionality and edge cases.
4. Commit your test changes with a descriptive message.

## Testing Patterns

- **File Pattern:** All test files follow the `*.test.*` naming convention (e.g., `searchBar.test.tsx`).
- **Framework:** Not explicitly specified; follow standard React/TypeScript testing practices.
- **Example:**
  ```typescript
  // searchBar.test.tsx
  import { render, screen } from '@testing-library/react';
  import { SearchBar } from './searchBar';

  test('renders search input', () => {
    render(<SearchBar />);
    expect(screen.getByPlaceholderText(/search/i)).toBeInTheDocument();
  });
  ```

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /add-component  | Add a new component following conventions    |
| /modify-logic   | Update or fix logic in existing files        |
| /write-test     | Add or update tests for components or logic  |
```
