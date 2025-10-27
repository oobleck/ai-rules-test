---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Test All Edge Cases and Input Boundaries
summary: All edge cases and input boundaries must be thoroughly tested to ensure robustness and prevent unexpected behavior.
scope:
  - codebase
importance: high
category: testing
status: draft
---

## Details

Edge cases and input boundaries are common sources of errors and vulnerabilities. Thoroughly testing these scenarios is crucial for ensuring the robustness and reliability of the codebase.

## Best Practices

*   Identify potential edge cases and input boundaries.
*   Create test cases that specifically target these scenarios.
*   Use a variety of input values, including invalid and unexpected ones.
*   Verify that the system handles edge cases and boundary conditions correctly.

## Examples

### TypeScript

```typescript
describe('Edge Cases', () => {
  it('should handle null input', () => {
    const result = myFunction(null);
    expect(result).toBe(expectedValueForNull);
  });

  it('should handle empty string input', () => {
    const result = myFunction('');
    expect(result).toBe(expectedValueForEmptyString);
  });

  it('should handle maximum value', () => {
    const result = myFunction(Number.MAX_VALUE);
    expect(result).toBe(expectedValueForMaxValue);
  });
});
```
