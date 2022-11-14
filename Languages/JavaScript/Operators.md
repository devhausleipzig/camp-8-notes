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

#### Remainder (Modulo)

Return the remainder of a division. It is very useful to f.e. determine if a number is even.

```js
3 % 2 // => 1
4 % 2 // => 0

//check even 
function isEven(n) {
	return n % 2 === 0
}

//check odd 
function isOdd(n) {
	return n % 2 !== 0
}
```

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

-                                                         OR ( || )

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