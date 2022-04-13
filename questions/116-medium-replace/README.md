Implement `Replace<S, From, To>` which replace the string `From` with `To` once in the given string `S`

For example

```ts
type Replace<S extends string, I extends string, R extends string> = S extends `${infer M}${I}${infer D}` ? `${M}${R}${D}` : S;

type replaced = Replace<'types are fun!', 'fun', 'awesome'> // expected to be 'types are awesome!'
```
