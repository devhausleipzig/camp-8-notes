
Unions create a either-or type.
In the example below the binding can hold an array that can have nested arrays, that can hold exclusively strings or numbers.

```ts
let myNestedArray: Array<number[] | string[]> = []
myNestedArray = [['hello'], [12]]
```

In this example the nested arrays can hold mixed values of either numbers or strings.

```ts
let myNestedMixedArray: Array<(number | string)[]> = []
myNestedMixedArray = [['hello', 2], ['bye', 1]]
```

## Discriminated Union

This is similiar to extends on an interface, but it only works on a [[Type]]

```ts
interface User {
  username: string
  password: string
}

type Admin = {
  permissions: string[]
} & User

const admin: Admin = {
  permissions: [],
  username: "",
  password: "",
}
```