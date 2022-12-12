# Classes

JavaScript _technically_ doesn't support this feature. The way JS is built, it's not possible to directly support a class system. So JavaScript has had some syntactic sugar added to the language to make it look like a class system.

A template for objects. The main benefits over just writing a function that returns new objects:

-   With classes, you can better combine your different templates.
-   You can add "methods" to your class instances, which is just a function that has access to the other attributes of the instance without you having explicity pass a reference to the instance. You automatically know what functions (operations) to can perform on specific data.

Some related terms: - An `abstract` class is one which you never intend to create an instance of. It's only for using as starting point for other classes to extend from.

Keywords:

-   class
-   constructor
-   new
-   this
-   extends
-   super

Things to remember:

-   A class must always have a constructor
-   If a class extends from another class, you must make call to super `super()` inside the constructor before you assign any values to `this`.
-   If you declare an attribute (property) for a class, you must give it a value (either directly or in the constructor). If you don't know or aren't sure, the rule thumb should be to always give a value to a property in the constructor (rather than directly).
-   When you use the `this` keyword inside the constructor or a method, it always refers to one specific instance of the class (whichever one you're calling the method on). It's a placeholder.
-   When you create an instance of a class, you must always use the `new` keyword. Otherwise you're gonna break stuff (all the times you used `this` in your definitions don't get replaced properly with the instance).

## Why we want to use classes (example of problems)

```ts

type Dog = {
	vocalization: string;,
	vocalize: Function,
	eat: Function
}

const someDog: Dog = {
	vocalization: "Woof",
	vocalize: function(object: Dog){
		console.log(object.vocalization);
	}
	eat: function(object: Dog, food){
		// do something with food
	}
}

const differentDog = {}

someDog.vocalize(this);

someDog.eat(differentDog, "meat") // doesn't make any sense


type Cat = {
	vocalization: string;,
	vocalize: Function,
	eat: Function
}

const someCat: Cat = {
	vocalization: "Meow",
	vocalize: function(object: Cat){
		console.log(object.vocalization);
	eat: function(object: Cat, food){
		// do something with food
	}
}

someCat.vocalize(someCat);
```

## Example of using classes

### Ex. 1

```ts
class ShoppingCart {
	items: Array<Product>;

	constructor() {
		this.items = [];
	}

	add(product: Product) {
		this.items.push(product);
	}

	remove(productId: string) {
		// remove product from items using the productId
	}

	calculateTotalCost() {
		let total = 0;

		for (const product of this.items) {
			total += product.price;
		}

		return total;
	}

	initiateBuy() {
		// start the buying process
	}
}

class User {
	id: string;
	email: string;
	cart: ShoppingCart;

	constructor(id: string, email: string) {
		this.id = id;
		this.email = email;
		this.cart = new ShoppingCart();
	}
}

class Product {
	id: string;
	name: string;
	price: number;

	constructor(name: string, price: number) {
		this.id = generateId();
		this.name = name;
		this.price = price;
	}

	checkInventory() {
		// check how many of this product are in the database
	}
}

const exampleShoe = new Product("Tennis Shoes", 19.5);
const exampleShampoo = new Product("Fruity Shampoo+", 3.2);

const Franz = new User("A7fbHdlkfh4387KGdktbrlastd", "franz@example.com");

Franz.cart.add(exampleShoe); // undefined
Franz.cart.add(exampleShampoo); // undefined

Franz.cart.calculateTotalCost(); // 22.70
```

### Ex. 2

```ts
type Leg = {
	length: "small" | "medium" | "long";
};

type Tail = {
	length: number;
};

class Mammals {
	legs: Array<Leg>;
	tail: Tail;
	vocalization: string;
	canClimb: boolean;
	activityPeriod: "diurnal" | "nocturnal";
	producesMilk: boolean;

	constructor(
		legs: Array<Leg>,
		tail: Tail,
		vocalization: string,
		canClimb: boolean,
		activityPeriod: "diurnal" | "nocturnal"
	) {
		this.producesMilk = true;
		this.legs = legs;
		this.tail = tail;
		this.vocalization = vocalization;
		this.canClimb = canClimb;
		this.activityPeriod = activityPeriod;
	}

	breathe() {
		console.log("all mammals breath");
	}

	move() {
		throw new Error("WTF are you doing?");
	}
}

class Dog extends Mammals {
	canHerd: boolean;

	constructor(breed: string) {
		let legs, tail;

		if (breed == "Chihuahua") {
			legs = [
				{ length: "small" },
				{ length: "small" },
				{ length: "small" },
				{ length: "small" }
			];

			tail = { length: 10 };
		}

		const vocalization = "Woof!";

		const canClimb = false;

		const activityPeriod = "diurnal";

		super(legs, tail, vocalization, canClimb, activityPeriod);

		this.canHerd = true;
	}

	move(): void {
		console.log("gallop");
	}
}

class Cat extends Mammals {
	extraLives: number;

	constructor(breed: string) {
		let legs, tail;

		if (breed == "Tabby") {
			legs = [
				{ length: "large" },

				{ length: "large" },

				{ length: "large" },

				{ length: "large" }
			];

			tail = { length: 10 };
		}
		const vocalization = "Meow!";
		const canClimb = true;
		const activityPeriod = "nocturnal";

		super(legs, tail, vocalization, canClimb, activityPeriod);

		this.extraLives = 8;
	}

	move(): void {
		console.log("saunter");
	}
}

const aDog = new Dog("Chihuahua");
const aCat = new Cat("Tabby");

aCat.breathe(); // "all mammals breath"

aDog.breathe(); // "all mammals breath"

aCat.move(); // "saunter"

aDog.move(); // "gallop"
```

## Example -- Calculator Class

```ts
class Calculator {
	display: string = "0";
	prevValue: string = "";
	currentValue: string = "";
	operator: string | null = null;
	moveValue: boolean = false;

	constructor() {}

	updateDisplay() {
		this.display = this.currentValue;
	}

	clear() {
		this.display = "0";
		this.currentValue = "";
	}

	// checks if value given is exactly one character; that character can only be 0-9
	isDigit(value: string) {
		const pattern = /[0-9]/;
		return pattern.test(value);
	}

	pressButton(value: string) {
		const operatorIsSet = this.operator != null;
		const isDigit = this.isDigit(value);

		if (operatorIsSet) {
			if (this.moveValue) {
				this.prevValue = this.currentValue;
				this.currentValue = "";
				this.moveValue = false;
			}

			if (isDigit) {
				this.currentValue += value;
				this.updateDisplay();
			} else {
				this.calculate();
				this.updateDisplay();

				if (value != "=") {
					this.operator = value;
					this.moveValue = true;
				} else {
					this.operator = null;
				}
			}
		}

		if (!operatorIsSet) {
			if (isDigit) {
				this.currentValue += value;
				this.updateDisplay();
			} else {
				if (value != "=") {
					this.operator = value;
					this.moveValue = true;
				}
			}
		}
	}

	calculate() {
		if (this.operator == "+") {
			this.currentValue = String(
				Number(this.prevValue) + Number(this.currentValue)
			);
		} else if (this.operator == "-") {
			this.currentValue = String(
				Number(this.prevValue) - Number(this.currentValue)
			);
		} else if (this.operator == "*") {
			this.currentValue = String(
				Number(this.prevValue) * Number(this.currentValue)
			);
		} else if (this.operator == "/") {
			this.currentValue = String(
				Number(this.prevValue) / Number(this.currentValue)
			);
		} else {
			console.log("don't know how to calculate");
		}
	}
}

const myCalc = new Calculator();

/// press 1, shows 1
/// press 1, show 11
/// press +, show 11
/// press 1, shows 1
/// press 1, show 11
/// press = , shows 22

myCalc.pressButton("1");
console.log(myCalc.display);
myCalc.pressButton("1");
console.log(myCalc.display);
myCalc.pressButton("+");
console.log(myCalc.display);
myCalc.pressButton("1");
console.log(myCalc.display);
myCalc.pressButton("1");
console.log(myCalc.display);
myCalc.pressButton("=");
console.log(myCalc.display);
```
