---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Require Automated Unit and Integration Tests
summary: New features must include automated unit and integration tests to ensure functionality and prevent regressions.
scope:
  - new-feature
importance: high
category: testing
status: draft
---

## Details

All new features must be accompanied by automated unit and integration tests. These tests should cover the core functionality of the feature and ensure that it integrates correctly with existing systems.

## Best Practices

*   Write tests before or concurrently with the code.
*   Ensure tests are reliable and repeatable.
*   Use clear and descriptive test names.

## Examples

### TypeScript

```typescript
describe('New Feature', () => {
  it('should perform core functionality', () => {
    // ... test code
    expect(result).toBe(expectedValue);
  });

  it('should integrate with existing system', () => {
    // ... test code
    expect(system.state).toBe(expectedState);
  });
});
```
