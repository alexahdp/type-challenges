Implement the built-in Parameters<T> generic without using it.

```typescript

type Parameters<F extends (...args: any[]) => any> = F extends (...args: infer U) => any ? U : never;

```