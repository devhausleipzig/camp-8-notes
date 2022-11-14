We use loops to encapsulate a sequence of command, that we want to repeat.

## while

A while loop runs as long as its condition evaluates to true

```js
while(condition) {
	// do something
}
```

```js
let input = "";
while (input.length < 3) {
  input = prompt(
	"Give me your name (should be at least 3 characters long))"
  );
}
document.write(input);
```

### break

The break keyword stops the execution of the loop all together.

```js
let input = "";
while (input.length < 3) {
  input = prompt(
	"Give me your name (should be at least 3 characters long))"
  );
  if (input == "te") {
	break;
  }
}
document.write(input);
```

### continue

Skip the instructions, that come after the keyword, and jumps to the next iteration of the loop

```js
let count = 0

while(count <= 10) {
  count++
  if(count === 5) {
    continue
  }
  console.log(count) // => 1,2,3,4,6,7,8,9,10,11
}
```

## for

```js
for(initialization; end-condition; index-change) {
	// do stuff...
}
```

```js
const fruits = ['banana', 'apple', 'pear']

for(let idx = 0; idx < fruits.length; idx++) {
	console.log(fruits[idx])
}
```

## for...of

If we just want to get access to every element in an array, one at a time, we can use a `for...of` loop

```js
const fruits = ['banana', 'apple', 'pear', 'pineapple']

for(fruit of fruits) {
  console.log(fruit)
}
```

## for...in

If we want to iterate over an object, we use the `for...in` loop. It will create a binding for the key in each iteration. You can use that key binding to access the value.

```js
const person = {
  name: 'Dan',
  age: 33
}

for(key in person) {
  console.log(person[key])
}
```