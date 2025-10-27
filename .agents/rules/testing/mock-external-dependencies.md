---
$schema: '/Users/oobleck/workspace/Sandbox/ai-rules-test/.agents/schemas/rules.yml'
title: Mock External Dependencies and APIs Reliably
summary: External dependencies and APIs must be mocked reliably to ensure test isolation and prevent external factors from affecting test results.
scope:
  - test-suite
importance: high
category: testing
status: draft
---

## Details

Mocking external dependencies and APIs is crucial for isolating tests and ensuring that they are not affected by external factors, such as network connectivity or API changes. Reliable mocking ensures that tests are repeatable and provide accurate results.

## Best Practices

*   Use mocking libraries to create reliable mocks.
*   Mock all external dependencies and APIs.
*   Verify that mocks are configured correctly.
*   Avoid using real external dependencies in tests.

## Examples

### TypeScript (using Jest)

```typescript
jest.mock('./external-api');

describe('Component with External API', () => {
  it('should call the external API with correct parameters', () => {
    const externalApi = require('./external-api');
    externalApi.getData.mockReturnValue(Promise.resolve({ data: 'mocked data' }));

    // ... test code

    expect(externalApi.getData).toHaveBeenCalledWith(expectedParameters);
  });
});
```
