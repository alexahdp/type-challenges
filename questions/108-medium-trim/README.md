
Implement `Trim<T>` which takes an exact string type and returns a new string with the whitespace from both ends removed.

For example

```ts
type Trim<S extends string> = S extends ` ${infer S}` ? Trim<S> : S extends `${infer S} ` ? Trim<S> : S;

type trimed = Trim<'  Hello World  '> // expected to be 'Hello World'
```
