Implement the JavaScript `Array.concat` function in the type system. A type takes the two arguments. The output should be a new array that includes inputs in ltr order

For example

```ts
// Solution
type Concat<A extends unknown[], B extends unknown[]> = [...A, ...B];

type Result = Concat<[1], [2]> // expected to be [1, 2]
```
