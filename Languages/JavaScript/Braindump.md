## Bindings

-   var
-   const
-   let

Binding is a pointer. A binding declared with 'const' cannot be re-assigned (you can't point it at a different anymore). A binding declared with 'let' can be re-assigned (you can point it at different stuff as much as you want).

Pretend 'var' is the same as 'let' for now.

```js
let a = 5;
a = 12; // allowed
a = "three"; // allowed

const b = "hello";
b = "bye"; // not allowed
```

## Types

-   string

Using double quote or single quote is basically equivalent. Using backticks allows you to do something special.

```js
"this is a string";
"this is also a string"`this is a string too`;
```

-   number

```js
0;
30;
99999999;
10.97349823 - 1000;
```

-   NaN
    This is a special value that is returned by math operators/functions when you try to do something invalid (like subtract strings, or divide by zero, etc...)

-   boolean
    Either `true` or `false`

```js
true;
false;
```

-   undefined
    This is an empty value. It means nothing is there. You only get this value when something is "unintentionally" empty.

```js
undefined;
```

-   null
    This is an empty value. It means nothing is there. This is usually a sign that "empty" is intentionally a valid state.

```js
null;
```

-   coercion (typecasting)
    Don't think about too much yet.

## Operators

-   assignment
-   call

### basic mathematical operator

-   addition
    Adds two numbers. Also can append two strings.

An operator/function that has different behavior depending on the types of the arguments given is called a 'overloaded' operator / polymorphic function. Concept is "operator overloading" / "polymorphism".

-   subtraction
    Subtracts two numbers.

-   multiplication
    Multiplies two numbers.

-   division
    Divide two numbers.

### Comparison Operators

-   (Strict) Equality
    Checks if two values are the same.

-   Greater than (or equal to)
    Checks if left value is greater (or equal to) the right value.

-   Less than (or equal to)

-   typeof keyword
    Returns a string that tells you what the type of a value is.

-   negation ( ! )
    Takes a boolean value and flips it.

-   double negation ( !! )

-   AND ( && )

-                                 OR ( || )

-   operator assignment combos (+= / -= / etc..)
-   Increment ++
-   Decrement --

-   Arity of an operator/function
    How many arguments does it take? Are they known or not known ahead of time?

Unary operator/function can only take 1 argument.

```js
!false; // one argument is the boolean 'false'

alert("Hello!"); // one argument is the string "Hello!"
```

Binary operator/function can only take 2 arguments.

```js
10 + 71; // 10 is the first argument, 71 is the second argument

someElement.addEventListener("click", someSortOfFunction);
// first argument is the string "click", the second argument is a function to call when the event happens
```

Trinary, quarternary, quintary, ???

N-ary: can only take some unknown but fixed number 'n' arguments.

Variadic: can take any number of arguments

```js
console.log("sdflkjhsf", "asdjhasf", "asdjh7823");
// here 3 arguments, but could have as many as I want
```

## Functions

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

Expressions are supposed to be some "complex value" that the interpreter can reduce down to a single value. They are purely computation and don't change anything about the world.

```js
10 + 89634 - ((34 / 434 / 2) % 21); // is an expression

someFunc(anotherFunc(yetAnotherFunc(124))); // could be an expression

const someBinding = 10; // statement
let myVar; // statement
function myFunc() {} // statement/not statement?
```

## Arrays

Don't think about it too much.

-   includes
-   index
-   pop
-   push

## Objects

Don't think about it too much.

-   get
-   method

## Misc

-   statement
-   console
-   values
-   alert
-   document.write
-   console.log
-   prompt
-   syntactic sugar
