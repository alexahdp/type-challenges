
Implement `Capitalize<T>` which converts the first letter of a string to uppercase and leave the rest as-is.

For example

```ts
type Capitalize<S extends string> = S extends `${infer U}${infer M}` ? `${Uppercase<U>}${M}` : S;

type capitalized = Capitalize<'hello world'> // expected to be 'Hello world'
```
