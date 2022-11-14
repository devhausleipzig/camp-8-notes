-   statement
-   console
-   values
-   alert
-   document.write
-   console.log
-   prompt
-   syntactic sugar

- functions
- Control Flow
	- if/ else
	- switch
	- ternary operator
- loop
	- for
	- while
	- do while
	- for ... in
	- for ... of
- nested for loop
- Object.keys
- export
- import
- return
- Remainder Operator (Modulo)



```js
// if

let isDog = true
let num = 4
console.log(12 % 5)


if(num === 4) {
  // code goes here...
  console.log('first condition met')
} else if(animal === 'cat') {
  console.log('a cat')
} else {
  console.log('another animal')
} 

// switch

const permissions = []
let role = 'MODERATOR'

switch(role) {
  case 'ADMIN': {
    permissions.push('edit_article')
  }
  case 'MODERATOR': {
    permissions.push('create_article')
  }
  case 'USER': {
    permissions.push('view_article')
  }
}

console.log(permissions)
```

```js
let num = 10

  

while(num > 0) {

// body

console.log(num)

num--

}

  

// do {

// // body

// num = num - 1

// console.log(num)

// } while(num > 0)

  

for(let idx = 10; idx > 0; idx--) {

console.log(idx)

}

  

let fruits = ['apple', 'banana', 'pineapple']

  

for(let idx = 0; idx < fruits.length; idx++) {

console.log(fruits[idx])

}
```

```js
function buildArray(start, end) {
  const array = []
  let ourStart = start
  let ourEnd = end

  if(end < start) {
    ourStart = end
    ourEnd = start
  }

  for(let counter = ourStart; counter <= ourEnd; counter++) {
    array.push(counter)
  }
  return array
}

const newArray = buildArray(10,5)
console.log(newArray)
console.log(newArray[5])
```

```js
let fruits = ['apple', 'banana', 'pineapple']

for(let i =  0; i < fruits.length; i++) {
  console.log(fruits[i])
}

// Looping over Arrays
for(fruit of fruits) {
  console.log(fruit)
}

let obj = {
  name: 'Test',
  age: 32
}

// Looping over Objects
for(key in obj) {
  console.log(key)
  console.log(obj[key])
}

const person = {
  name: "Dan",
  age: 33
}

console.log(person.name)
// Same as
const objectKey = 'name'
console.log(person[objectKey])
```