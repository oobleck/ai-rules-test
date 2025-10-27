---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Use Property-Based or Fuzz Testing
summary: Employ property-based or fuzz testing for critical components to uncover edge cases and potential vulnerabilities.
scope:
  - critical-components
importance: medium
category: testing
status: draft
---

## Details

Property-based testing and fuzzing are powerful techniques for finding unexpected edge cases and vulnerabilities in critical components. These methods involve generating a wide range of inputs to test the system's behavior against predefined properties or constraints.

## Best Practices

*   Identify critical components for property-based or fuzz testing.
*   Define properties or constraints that should always hold.
*   Use appropriate tools and libraries for test generation.
*   Analyze and address any violations of the defined properties.

## Examples

### TypeScript (using jsverify)

```typescript
import jsc from 'jsverify';

describe('Critical Component', () => {
  it('should satisfy property: result is always positive', jsc.property('nat', (num) => {
    const result = criticalComponent(num);
    return result > 0;
  }));
});
```
