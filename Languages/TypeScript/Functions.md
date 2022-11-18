## Arguements and Return 

When we write a function slkeleton we should alsways think about the *contact* of that function. Contract means -> What are my inputs and what should be the output of my function.

```ts
// Function Skeleton with contract
function add(x: number, y: number): number {}

function add(x: number, y: number): number {
	// Implementation
	return x + y
}

add('hello', 1) // invalid
```

## Function Type

```ts
type Bird = {
  name: string
  fly: () => void
}

const bird: Bird = {
  name: "Birdie",
  fly: function (): void {
    console.log('Im flying')
  }
}

bird.fly()
```

```ts
// You can put the function type into an type alias
type AddFunction = (a: number, b: number) => number

// Arrow function
const add: AddFunction = (a, b) =>  a + b
// equal
const addWithBody: AddFunction = (a, b) => {
  return a + b
}

console.log(add(1,2))

// You can inline the function type
const getTheBiggerNumber: (x: number,y: number) => number = (x, y) => {
  if(x >= y) {
    return x
  } else {
    return y
  }
}

console.log(getTheBiggerNumber(3,2))
```

## void

The return type of `void` means that our function doesn't return anything. The function only performs one or more side effects (function is impure).

```ts
function logger(...args) {
  console.log(...args)
}

logger('hello', 'word')
```