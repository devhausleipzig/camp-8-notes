Is a list of values. Arrays can hold any type of value, they can even be mixed. Elements in an array are origanized by index. The first element has the index *0*

```js
const fruits = ['apple', 'banana', 'pineapple']

const mixed = ['Dan', 33, true]
```

## Element Access

We can access elements in an array with the *lookup operator* `[]`. It takes an index and returns the element at given index.

```js
const fruits = ['apple', 'banana', 'pineapple']

fruits[0] // => 'apple'
fruits[1] // => 'banana'

// Access the last element
fruits[fruits.length - 1] // => 'pineapple'
```

## Getters

Getters just return a value and can't take arguments.

## Length

We can use `.length` on any array to get the number of items in that array. The length of an array is alway *one more* than the *last index* . Length is not an array methods, although it's called with the dot. Length is actually a *getter*.

## Methods

We can call methods an arrays by appending the method name with a dot to the array. `array.method()`. 

### push

Appends a value to give array. Push mutates the array (You don't have a reference to what the array looked like before you used push). Push returns the new length of the array after appending the value.

```js
const fruits = ['apple', 'banana', 'pineapple']

fruits.push('dragonfruit') // => 4

fruits // => ['apple', 'banana', 'pineapple', 'dragonfruit']
```

### pop

Remove the last element of an array. It also mutates the array. Returns the element is removed.

### unshift

Adds a new element to the beginning of an array. Return the new length of that array

```js
const fruits = ['apple', 'banana', 'pineapple']

fruits.unshift('dragonfruit') // => 4

fruits // => ['dragonfruit', 'apple', 'banana', 'pineapple']
```

### shift

Remove the first element of an array. It also mutates the array. Returns the element is removed.

```js
const fruits = ['apple', 'banana', 'pineapple']

fruits.shift() // => 'apple'

fruits // => ['banana', 'pineapple']
```

### includes

Checks if give value exists in the array. Returns a boolean.

```js
const fruits = ['apple', 'banana', 'pineapple']

fruits.includes('apple') // => true
fruits.includes('dragonfruit') // => false
```

### slice

Takes 2 optional arguments (startIndex and endIndex) and creates a copy of the original array, starting at *startIndex* and ending right before *endIndex*. Returns a copy of the specified section. If we dont pass any arguments, we create a copy of given array.

```js
const fruits = ['apple', 'banana', 'pineapple']

const arraySlice = fruits.slice(1) // => ['banana', 'pineapple']

fruits // => ['apple', 'banana', 'pineapple']
```


### splice

#### splice/2

Removes a section from an array. It can take 2 arguments (startIndex and deleteCount). *deleteCount* is optional. If we dont specifiy *deleteCount*, it removes every element till the end.

```js
const fruits = ['apple', 'banana', 'pineapple']

const removedElements = fruits.splice(1) // => ['banana', 'pineapple']

fruits // => ['apple']
```

```js
const fruits = ['apple', 'banana', 'pineapple']

const removedElements = fruits.splice(1, 1) // => ['banana']

fruits // => ['apple', 'pineapple']
```

#### splice/3

Works like `splice/2`, but also can take any number of replacement arguments.

```js
const fruits = ['apple', 'banana', 'pineapple']

const removedElements = fruits.splice(1, 1, 'dragonfruit') // => ['banana']

fruits // => ['apple', 'dragonfruit', 'pineapple']
```

```js
const fruits = ['apple', 'banana', 'pineapple']

const removedElements = fruits.splice(1, 1, 'orange', 'peach') // => ['banana']

fruits // => ['apple', 'orange', 'peach', 'pineapple']
```

If you want to use `splice`, you should create a copy of your original array first. One way to do that is calling `slice()` with no arguments.

```js
const originalFruits = ['apple', 'banana', 'pineapple']

const newFruits = originalFruits.slice()

newFruits.splice(1, 1, 'peaches')

newFruits // => ['apple', 'peaches', 'pineapple']
originalFruits // => ['apple', 'banana', 'pineapple']
```

### indexOf

Takes a value as an arguement and checks if that value is in the array. If it is, indexOf return the first index it found. Otherwise it return -1

```js
const fruits = ['apple', 'banana', 'apple', 'pineapple']

fruits.indexOf('apple') // => 0
fruits.indexOf('peach') // => -1
```

### Reference

if we want to create a copy of an array, it is not enough to create a new binding and assign the value of a previous binding

```js
const fruits = ['apple', 'banana']

const newFruits = fruits
```

This would point to the exact place in memory.
If you want to create a copy use methods like `slice`

![[reference.png]]
