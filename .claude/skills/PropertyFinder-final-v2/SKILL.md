# PropertyFinder-final-v2 Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the development patterns and workflows used in the PropertyFinder-final-v2 React application. The project follows modern JavaScript development practices with React as the primary framework, emphasizing clean code organization, dependency management, and documentation maintenance.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names
- Example: `propertyCard.js`, `searchFilters.js`, `userProfile.js`

### Import Style
- Use **relative imports** for local modules
```javascript
import PropertyCard from './components/propertyCard';
import { searchProperties } from '../utils/searchHelpers';
import config from '../../config/appConfig';
```

### Export Style
- Use **default exports** as the primary export pattern
```javascript
// Component example
const PropertyFinder = () => {
  // component logic
};

export default PropertyFinder;
```

### Commit Messages
- Use freeform commit messages
- Keep messages concise (average 35 characters)
- Focus on clear, descriptive actions

## Workflows

### Dependency Management Update
**Trigger:** When dependencies need to be updated or installed
**Command:** `/update-deps`

1. Review current dependencies in `package.json`
2. Update dependency versions to latest stable releases
3. Run `npm install` to update `package-lock.json`
4. If using Yarn, run `yarn install` to update `yarn.lock`
5. Test the application to ensure compatibility
6. Commit all three files together

```bash
# Example workflow
npm outdated
npm update
# Test the application
git add package.json package-lock.json yarn.lock
git commit -m "Update project dependencies"
```

### External Tool Integration
**Trigger:** When adding automated tools like Renovate, WhiteSource, etc.
**Command:** `/add-tool`

1. Research the tool's configuration requirements
2. Create appropriate configuration file (e.g., `renovate.json`, `.whitesource`)
3. Configure tool settings for the project's needs
4. Submit pull request with the configuration
5. Review and test the integration
6. Merge configuration into main branch

```json
// Example renovate.json
{
  "extends": [
    "config:base"
  ],
  "schedule": [
    "before 4am on Monday"
  ]
}
```

### Documentation Maintenance
**Trigger:** When documentation needs updates or during branch merges
**Command:** `/update-docs`

1. Identify outdated sections in `README.md`
2. Update installation instructions if dependencies changed
3. Refresh feature descriptions and usage examples
4. Resolve any merge conflicts in documentation
5. Ensure all links and references are current
6. Commit documentation changes with descriptive message

```markdown
<!-- Example README structure -->
# PropertyFinder

## Installation
npm install

## Usage
npm start

## Features
- Property search
- Filter options
- User profiles
```

## Testing Patterns

### Test File Structure
- Use `*.test.*` pattern for test files
- Example: `propertyCard.test.js`, `searchFilters.test.jsx`
- Testing framework is not explicitly configured, suggest Jest + React Testing Library

```javascript
// Example test structure
import { render, screen } from '@testing-library/react';
import PropertyCard from './propertyCard';

describe('PropertyCard', () => {
  test('renders property information', () => {
    // test implementation
  });
});
```

## Commands

| Command | Purpose |
|---------|---------|
| `/update-deps` | Update project dependencies and lock files |
| `/add-tool` | Integrate external development tools |
| `/update-docs` | Maintain and update project documentation |
| `/create-component` | Generate new React component with proper naming |
| `/fix-imports` | Standardize import statements to relative paths |
| `/setup-tests` | Configure testing framework and create test files |