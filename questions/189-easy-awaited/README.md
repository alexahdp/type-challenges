If we have a type which is wrapped type like Promise. How we can get a type which is inside the wrapped type? For example if we have `Promise<ExampleType>` how to get ExampleType?

> This question is ported from the [original article](https://dev.to/macsikora/advanced-typescript-exercises-question-1-45k4) by [@maciejsikora](https://github.com/maciejsikora)

```typescript
type X = Promise<string>
type Y = Promise<{ field: number }>

type Transform<A> = A extends Promise<infer B> ? B : never;

type ResultX = Transform<X>; // ResultX type equals string
type ResultY = Transform<Y>; // ResultY type equals { field: number }

```