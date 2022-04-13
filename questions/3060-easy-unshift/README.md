Implement the type version of ```Array.unshift```

For example

```typescript
// Solution
type Push<A extends unknown[], B> = [B, ...A];

type Result = Unshift<[1, 2], 0> // [0, 1, 2,]
```