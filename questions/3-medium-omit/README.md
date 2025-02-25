Implement the built-in `Omit<T, K>` generic without using it.

Constructs a type by picking all properties from `T` and then removing `K`

For example

```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

// Solution
type MyOmit<T extends Record<string, unknown>, V extends keyof T> = {
  [k in Exclude<keyof T, V>]: T[k];
}

type TodoPreview = MyOmit<Todo, 'description' | 'title'>

const todo: TodoPreview = {
  completed: false,
}
```
