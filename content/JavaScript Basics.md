---
Type: Learning
Course: ZTM
---
What is JavaScript 
- The "verb" of websites 
- Allows actions on websites 
## JavaScript Types 
- Number - math equation calculations
  - `NaN` - means not a number
- String - characters that are surrounded by `""` 
  - Note: you can use `''` but then it can misread apostrophes so be careful 
- Boolean - true or false
  - When comparing things, use ===
- Undefined - variable has not been assigned
- Null - empty object
- Symbol - 
- Object - 
## Comparisons 
`!==`
`>=`
`<=`
`>`
`<`
## Variables 
- `var` used for variables 
  - Example: `var sentence = "hello world";`
- `Number(variable-name)` to change string into number 
## Control Flow  (Conditionals)
- `if` 
- `else`
- `else if`
- `ternary operator `
- `switch`
## Connecting HTML to JavaScript 
- Note: Place `<script>` under the body because it won't load the rest of the website until the script runs
- `<script type="text/javascript" src="script.js"></script>`
## Console 
`console.log("")` to log your actions on the console
## Functions 
- `prompt("What is your user name?");` asks for input from user 
- `alert();` alerts user with content
- The parenthesis means call the function in JavaScript
- ==Arguments== (aka parameters): the information given to the function inside the parenthesis 
- ==Functions==: bundles up actions and makes it easier to call
### Function Declaration 
```javascript 
function sayHello() {
	console.log("Hello");
}
```
### Function Expression 
```javascript
// Anonymous function
var sayBye = function() {
	console.log("Bye");
};
// NOTE: Function Expression ends in a ;  
```
- ==Anonymous function==: Doesn't have a name so we can't call on it later 

> [!important] DRY: Don't Repeat Yourself 

### Functions with Arguments 
```js
function multiply(a, b) {
	return a * b;
}
```
- Note that for functions to return something you need to specify (duh)

## Terminology 
- Expression: Something that produces an output 
- Function vs Method 
  - Method: Something inside an object
## Loops 
`for` 
`while`
`do, while`
`forEach`: Shorter version and new to the language
## Javascript Keywords 
- These words can't use as variable names
- Examples: `for`, `break`, etc. 
## Data Structures - Arrays
```js 
var list = ["tiger", "cat", "bear", "bird"];
// Removes first argument and shifts the list over to the left
list.shift(); 
// Pops last argument
list.pop();
// Adds argument to the end 
list.push("elephant");
// Adds lists together BUT does not do it in place 
list.concat(["bee", "deer"]);
// Sorts list 
list.sort()
```
## Data Structures - Objects
```js 
var user = {
	name: "John";
	age: 34;
	hobby: "Soccer";
	isMarried: false;
};
```
### Methods 
```js
user.favoriteFood = "spinach";
user.isMarried = true;
```
