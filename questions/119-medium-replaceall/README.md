
Implement `ReplaceAll<S, From, To>` which replace the all the substring `From` with `To` in the given string `S`

For example

```ts
type ReplaceAll<S extends string, I extends string, R extends string> = S extends `${infer M}${I}${infer D}` ? ReplaceAll<`${M}${R}${D}`, I, R> : S;

type replaced = ReplaceAll<'t y p e s', ' ', ''> // expected to be 'types'
```
