---
Type: Learning
Course: ZTM
---
## Scope 
- **Root scope**: window object, the default scope
- Functions have their own scope so even though it can access the root scope, the root scope cannot access what’s inside a function unless specifically specified
- If a function has a variable that’s defined within it that has the same name as a variable in the root scope, the local variable is prioritized within the function
- If a function calls on the variable within the root scope, it modifies the root scope variable
## Advanced control flow 
### Ternary Operator 
Allows you to shorten the if else control flow into one line! 
`condition ? expression1 : expression2;`
If condition is true, then expression1, else expression2 
### Switch 
```js
switch (variable){
	case "case1": 
		expression;
	case "case2": 
		expression;
	default: 
		expression;
}
```
## ES5 & ES6 
- ES - ECMAScript: the standard way of writing javascript
- ES5 means ECMAScript version 5 
- BABEL - translates ES into JavaScript that all browsers can understand 
### Let + Const 
Don’t use `var` anymore and use `let` which creates a new scope 
Use `const` for variables that don’t change (eg. functions) 
- Note that you can change the properties of a constant object but you can’t change the object itself
```js 
const player = 'bobby';
let experience = 100;
let wizardLevel = false;

if (experience > 90) {
	wizardLevel = true; 
	console.log('inside', wizardLevel);
}
console.log('outside', wizardLevel);
```
### Destructuring
```js 
const obj = {
	player = 'bobby';
	experience = 100;
	wizardLevel = false; 
}
// The old way - lots of typing
const player = obj.player;
const experience = obj.experience; 
// Destructuring - does the same thing as above
const { player, experience } = obj;
```
### Object properties
#### Dynamic 
Below is a dynamic way of creating object properties 
```js 
const a = 'john snow';

const obj = {
	[name]: 'hello',
	[1+2]: 'hihi',
}
```
Accessing `obj` will give us: `{3: "hihi", john snow: "hello"}`
#### Short hand for declaring properties 
Below is a shorter way of declaring properties if the value and property name are the same
```js 
const a = "Simon";
const b = true;
const c = {};

// OLD WAY 
const obj = {
	a: a, 
	b: b,
	c: c
}

// NEW WAY
const obj = {
a, b, c
}
```
### Template strings 
```js 
const greetingOld = "Hello" + name + " you seem to be doing " + greeting + "!";
const greetingNew = `Hello ${name} you seem to be doing ${greeting}!`
```
### Default arguments 
```js
function greet(name='', greeting='great') {
	return `Hello ${name} you seem to be doing ${greeting}!`
}
```
### Symbol 
```js 
let sym1 = Symbol();
let sym2 = Symbol('foo');
let sym3 = Symbol(foo);
```
### Arrow functions 
Useful for when you’re only returning one thing
```js 
functon add(a, b) {
	return a + b;
}

const add = (a,b) => a + b;
```
## Advanced Functions 
### Closure
```js 
const first = () => {
	const greet = 'Hi';
	const second = () => {
		alert(greet); 
	}
	return second;
}

const newFunc = first();
newFunc();
```
### Currying 
```js
const multiply = (a, b) => a * b;
const curriedMultiply = (a) => (b) => a * b; 
```
### Compose
- Like the mathematical composition function
```js
const compose 
```
## Important Note 
- Avoid side effects and always return to create a deterministic system
## Advanced Arrays 
### Map 
- Expects the function to return something and it creates a new array 
```js
const array = [1, 2, 10, 16]

const mapArray = array.map((num) => {
	return num * 2;
});
```
### Filter 
- Only adds to the array if it meets the condition
```js
const filterArray = array.filter(num => {
	return num > 5;
});
```
### Reduce 
```js
const reduceArray = array.reduce((accumulator, num) => {
	return accumulator + num;
}, 0); 
```
## Advanced Objects 
### Reference Type 
- Non-primitive type of object that’s created by the programmer 
- Idea of pointers 
### Context vs Scope 
- Context: Where are we in the object? 
- Example: `this.alert()`
### Instantiation 
```js
class Player {
	constructor(name, type) {
		this.name = name;
		this.type = type;
	}
} 

class Wizard extends Player {
	constructor(name, type) {
		super(name, type)
	}
	play() {
		console.log(`WEEEEEEE I'm a ${this.type}`);
	}
}
```
