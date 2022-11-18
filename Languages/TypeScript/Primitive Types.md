We can declare type on bindings, by adding a *type annotation* to that binding.

```ts
let myBinding: string = 'something'
```

## Inference

If you don't explicitly type a binding, TS will try to infer the type from the initial value given.

```ts
let myBiding = 'hello' // => TS infers that as a string
```

If TS cannot infer the type, it will assume a type of any

```ts
let myBiding // => TS infers that as a any
```

If you don't want to give your binding a value right away, you can still use a type annotation and assign a value later.

```ts
let myBinding: 
```

A better way would be to use neutral values (falsy) on binding initialization. 

```ts
let myString: string = ''
let myNumber: number = 0
let myBoolean: boolean = false
```


## string

```ts
let myString: string = 'hello'
```

## boolean

```ts
let myBoolean: boolean = true
```

## number

```ts
let myNumber: number = 23.56
let myNan: number = NaN
```

## undefined

Typing a binding as undefined is not very useful, it would prevent the binding from taking any value in the future

```ts
let myUndefined: undefined
```

## null

```ts
let myNull: null = null
```

Use null if you want to create a binding that can either hold a value or is empty.

```ts
let option: string | null = null

option = "hello world"

function splitOptionalString(optionalString: string | null): Array<string> {
  if(!optionalString) {
    return []
  } else {
    return optionalString.split(" ")
  }
}

console.log(splitOptionalString(option)) // => ['hello', 'world']
```

## never

The never says that there can never be a value.

```ts
let myArray = [] // infers never[]
```


## any

Any literally means any value is valid

```ts
ley myAny: any

myAny = 'hello'
myAny = 2
myAny = udefined
//...
```

## unknown

The unknown type says, we don't know which type is gonna be passed in. TS forces us to make checks to determine the type.

```ts
function unknownFn(a: unknown) {
  if(typeof a === 'string') {
    return a.split(' ')
  }
  if(typeof a === 'number') {
    return 12 * a
  } else {
    return null
  }
}
```


## literals

Literals are a specific value of a primitive type

```ts
let myLiteral: 'hello' = 'hello'

myLiteral = 'bye' // error
```

In general literals are mostly used in conjuntion with [[Unions|union]] type.

```ts
let myRole: 'admin' | 'user'

myRole = "user" // valid
myRole = "admin" // valid
myRole = "superuser" // error
```