Implement the built-in `ReturnType<T>` generic without using it.

For example

```ts
const fn = (v: boolean) => {
  if (v)
    return 1
  else
    return 2
}

// Solution:
type MyReturnType<T> = T extends (...args: any[]) => infer U ?  U : never;

type a = MyReturnType<typeof fn> // should be "1 | 2"
```
