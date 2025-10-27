---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Treat Flaky Tests as Blockers
summary: Flaky tests should be treated as blockers and either fixed or quarantined immediately to maintain test suite reliability.
scope:
  - test-suite
importance: high
category: testing
status: draft
---

## Details

Flaky tests, which produce inconsistent results, undermine the reliability of the test suite. They should be treated as blockers and addressed immediately by either fixing the root cause or quarantining the test to prevent it from affecting other tests.

## Best Practices

*   Identify and isolate flaky tests.
*   Investigate the cause of flakiness.
*   Fix or quarantine flaky tests promptly.
*   Monitor quarantined tests for resolution.

## Examples

### TypeScript

```typescript
// Example of quarantining a flaky test in Jest
test.skip('Flaky Test', () => {
  // ... test code
});

// Or using a conditional skip
test('Potentially Flaky Test', () => {
  if (isFlakyCondition()) {
    test.skip('Skipping due to flaky condition');
    return;
  }
  // ... test code
});
```
