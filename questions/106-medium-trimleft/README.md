
Implement `TrimLeft<T>` which takes an exact string type and returns a new string with the whitespace beginning removed.

For example

```ts
type TrimLeft<S extends string> = S extends ` ${infer S}` ? TrimLeft<S> : S;

type trimed = TrimLeft<'  Hello World  '> // expected to be 'Hello World  '
```
