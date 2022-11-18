We can type Arrays in two different ways:

`type[]`

```ts
let myArray: number[] = []

myArray.push(2) // valid

myArray.push('hello') // error
```

`Array<type>`

```ts
let myArray: Array<number> = []

myArray.push(2) // valid

myArray.push('hello') // error
```

If you want to create a Array that can only hold number arrays, you can specify that by using the `Array<>` syntax, for a more readable result

```ts
let myNestedArray: Array<number[]> = []
// eqauls
let myNestedArrayUnreadable = number[][]

myNestedArray = [[2], [2,3]]
```

## Tuple

A tuple is an array of fixed size, each value inside of the tuple needs to be explicitly typed

```ts
const threeDimensioanlCoordinate: [number, number, number] = [24, 46, 67]
```