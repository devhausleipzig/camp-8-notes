## What is TypeScript?

TypeScript is a superset of JavaScript. It i a compiled language, that compiles down to plain JavaScript. TypeScripts purpose is to tame the dynamic type system of JavaScript.

Example:
```js
// Write a function that takes 2 numbers and produces the sum
function add(x,y) {
	if(typeof x !== 'number') {
		throw new Error()
	}
	if(type y !== 'number') {
		throw new Error()
	}
	return x + y 
}

add('hello', 3)
```

```ts
// Write a function that takes 2 numbers and produces the sum
function add(x: number, y: number) {
	return x + y
}

add('hello', 3) // Error before the app runs
```

The big benefit of a compiled language is, that we can catch errors and potential bugs before the app runs.

After TypeScript compiles to JS, all TypeScript specific code gets removed. We only use TypeScript to validate our type while we develop.