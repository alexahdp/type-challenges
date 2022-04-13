Implement the generic version of ```Array.push```

For example

```typescript
// Solution
type Push<A extends unknown[], B> = [...A, B];

type Result = Push<[1, 2], '3'> // [1, 2, '3']
```
