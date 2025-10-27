---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Maintain High and Meaningful Coverage Thresholds
summary: Code coverage thresholds must be maintained at a high level to ensure adequate testing of the codebase.
scope:
  - codebase
importance: medium
category: testing
status: draft
---

## Details

High code coverage thresholds should be maintained to ensure that a large portion of the codebase is covered by automated tests. These thresholds should be meaningful and reflect the complexity and criticality of the code.

## Best Practices

*   Set coverage thresholds based on project requirements.
*   Regularly monitor coverage metrics.
*   Investigate and address any coverage gaps.

## Examples

### TypeScript

```typescript
// Example configuration for Jest
coverageThreshold: {
  global: {
    branches: 80,
    functions: 80,
    lines: 80,
    statements: 80,
  },
};
```
