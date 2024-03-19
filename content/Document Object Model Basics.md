---
Type: Learning
Course: ZTM
---
What is the DOM? 
- Document is an object (the page that we see)
- Document's parent is Window 
  - Window is the parent of everything so it's the default if you don't specify 
- JavaScript is able to talk to the DOM in order to make the necessary changes
### Resource
[The HTML DOM](https://www.w3schools.com/js/js_htmldom.asp)
## DOM Selectors 
```js 
document.getElementsByTagName("h1");
document.getElementsByClassName("container");
document.getElementByID("first");

// finds first element it finds 
document.querySelector("h1");
// lists all applicable elements 
document.querySelectorAll("li");

document.querySelector("li").getAttribute("random");
document.querySelector("h1").setAttribute("random", 1000);
```
## Changing Styles 
```js 
// Not good practice but you can change attributes here 
document.querySelector("h1").style.background = "yellow"; 
// Better practice is to add classes 
document.querySelector("h1").className = "className";
// Shows list of classes
document.querySelector("h1").classList; 
	document.querySelector("h1").classList.remove("coolTitle");
	document.querySelector("h1").classList.add("done");
	document.querySelector("h1").classList.toggle("done");
```
## Bonus 
```js 
//DANGEROUS!
document.querySelector("h1").innerHTML = "<strong>!!!!</strong>"; 
// Access parents and children of elements
document.querySelector("li").parentElement;
document.querySelector("li").children;

```

> [!important] It is important to CACHE selectors in variables! 
## DOM Events 
```js 
var button = document.getElementsByTargetName("button")[0];

button.addEventListener("click", function() {
	console.log("CLICK!!");
})
```
### Resources 
- [Event Reference](https://developer.mozilla.org/en-US/docs/Web/Events)
- [JavaScript Char Codes](https://www.cambiaresearch.com/articles/15/javascript-char-codes-key-codes)
- 