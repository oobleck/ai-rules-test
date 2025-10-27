---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Include Regression Tests for Known Past Issues
summary: Regression tests must be included for all known past issues to prevent their recurrence.
scope:
  - codebase
importance: high
category: testing
status: draft
---

## Details

Regression tests are essential for ensuring that past issues do not reappear in the codebase. These tests should specifically target the scenarios that caused the original issues and verify that they have been resolved.

## Best Practices

*   Create regression tests whenever a bug is fixed.
*   Ensure that regression tests accurately reproduce the original issue.
*   Run regression tests as part of the standard test suite.
*   Update regression tests if the underlying code changes.

## Examples

### TypeScript

```typescript
describe('Regression Tests', () => {
  it('should prevent recurrence of issue #123', () => {
    // ... test code that reproduces the original issue
    expect(result).toBe(expectedValue);
  });
});
```
