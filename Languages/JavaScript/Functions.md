-   function
    Function is a block of statements. The 'return' statement is how we return a value out of the function.

```js
function increment(number) {
	// parameters are placeholders for args when func is called

	return number + 1; // value that is returned out of the func
}

increment(10); // 10 is the actual value given to the function (the argument) when we call it (ask it to be executed)
```

-   statement vs expressions

Statement is supposed to be "a single action". The sequence of statements that the interpreter goes through one by one is the "thread of execution". These actions (statements) have "side-effects", e.g. writing to hard disk, sending a network message, moving something in memory, changing a data structure, etc... That is, they change something about the world.

Expressions are supposed to be some single "complex value" that the interpreter can reduce down to another single but simpler value/output. They are purely computation and shouldn't change anything about the world.

```js
10 + 89634 - ((34 / 434 / 2) % 21); // is an expression

someFunc(anotherFunc(yetAnotherFunc(124))); // could be an expression

const someBinding = 10; // statement
let myVar; // statement
function myFunc() {} // statement/not statement?
```