-   statement
-   console
-   values
-   alert
-   document.write
-   console.log
-   prompt
-   syntactic sugar


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