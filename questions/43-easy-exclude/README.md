Implement the built-in Exclude<T, U>
> Exclude from T those types that are assignable to U

```typescript

type Cars = 'Mersedes' | 'BMW' | 'Opel' | 'Kia';
type KoreanCar = 'Kia';

type Exclude<T, V> = T extends V ? never : T;

type NotKoreanCars = Exclude<Cars, KoreanCar>;

```