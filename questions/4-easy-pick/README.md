Implement the built-in `Pick<T, K>` generic without using it.

Constructs a type by picking the set of properties `K` from `T`

For example

```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

// Solution
type MyPick<T extends Record<string, unknown>, V extends keyof T> = {
  [k in V]: T[k]
}

type TodoPreview = MyPick<Todo, 'title' | 'completed'>

const todo: TodoPreview = {
    title: 'Clean room',
    completed: false,
}
```