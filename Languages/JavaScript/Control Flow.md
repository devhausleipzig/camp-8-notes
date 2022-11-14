In our code we need to make descisions. We might need to validata a user input. E.g. the user is supposed to put in a email address for signup. If the value is not a valid email address, the user need to be notified to re-enter the email address. If it is valid, we can submit the form.

## if / else

```js
if(condition) {
	// execute some code ...
} else {
	// execute some code ...
}
```

```js
if(email_is_valid) {
	// submit the form
} else {
	// send an error
}
```

The condition can be any expression that evaluates to a boolean.

We can also have multiple checks with `else if`

```js
if(condition) {
	// execute some code ...
} else if(another_condition) {
	// execute some code ...
} else {
	// execute some code ...
}
```

### Example

```js
if(typeof input !== 'number') {
	console.log('This is not a number')
} else if(input > 10 || input < 1) {
	console.log('The number is not between 1 and 10')
} else {
	console.log('Thanks')
}
```

## Ternary Operator

If/else is a statement, so you cannot save the result to a binding. If you want to have a simple if/else check that evaluates to a value, you can use the ternary operator.

```js
condition ? 'true' : 'false'
```

if the condition evaluates to true, the ternary itself evaluates to the value after the question mark. If the condition evaluates to false, the ternary iteself evaluates to the value after the colon `:`.

```js
let input = 5

const result = input <= 5 ? 'low' : 'high'
```

## Switch

The switch statement can match on any value. It will execute the command on the matching case. If you dont brek inside of your case if will keep executing every command that comes after that point, until it hits a break or the end of the switch statement.

```js
switch(value) {
	case 'case1':
		// do something...
		break;
	case 'case2':
		// do something...
		break;
	case 'case3':
		// do something...
		break;
	default: 
		// do something...
}
```

```js
let animal = 'dog'

switch(animal) {
	case 'cat':
		alert('You have a cat!')
		break;
	case 'dog':
		alert('You have a dog!')
		break;
	default: 
		alert('You have something else')
}
```

We can take advantage of that waterfall behavior, by checking the highest role first and on the first match we assign every remaining permission.

```js
const role = 'ADMIN'

const permissions = []

switch(role) {
  case 'ADMIN':
    permissions.push('create')
  case 'MODERATOR':
    permissions.push('edit')
  case 'USER':
    permissions.push('read')
}
```