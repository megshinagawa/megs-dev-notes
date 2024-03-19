---
Type: Learning
Course: ZTM
---

Basics 
- CSS is cascading, meaning that whatever comes last is what’s true; ie: order matters 
### Basic format of CSS
```css
Selector {
	Property: Value;
}
```
### Adding style sheet to HTML 
`<link rel="stylesheet" type="text/css" href="style.css">`
Alternatively, you can create a style tag in the HTML: `<style></style>`
### Cheat Sheet
- `.class` can be applied to more than one thing
- `#id` specific to one thing
- `element` applied to the specific element 
- `element, element` applied to all the listed elements 
- `element1 element2`  applied to all element2 that’s inside element1 
- `element1 > element2`  applied to all element2 that have parent element1
- `element1 + element2` applied to element2 that comes directly after element1
- `:hover` apply when hovering over with cursor
- `:last-child` applied to last child 
- `:first-child` applied to first child
- `!important` overrides the cascading nature of CSS (Don’t use, but be aware of it) 
### What selectors win out in the cascade depends on: 
- Specificity ([Specificity calculator](https://specificity.keegan.st/)) 
- Importance 
- Source order
## Box Model 
- Margin - outside of the box 
- Border - lines the box
- Padding - inside the box 
## px vs em vs rem
- px: pixel size 
- em: size in relation to the parent element
- rem: size in relation to the root element (HTML tag) 
Resource: [What's The Difference Between PX, EM, REM, %, VW, And VH?](https://elementor.com/help/whats-the-difference-between-px-em-rem-vw-and-vh/)
## Critical Render Path 
- You won’t be able to render the page until your CSS file loads up 
- If you have a font file, it might take even longer 
- Good practice: keep your CSS file short
  - [CSS Minify](https://www.cleancss.com/css-minify/) - program that compresses your CSS file
## Flexbox 
Resource: [CSS Tricks Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Froggy game](http://flexboxfroggy.com/)
## CSS Browser Support 
- Reference: [CSS Reference Browser Support](https://www.w3schools.com/cssref/css3_browsersupport.asp)
## Responsive UI 
- Does it open well in all screen sizes? 
## Resources 
[CSS Quiz](https://www.w3schools.com/css/css_quiz.asp)
[CSS-Tricks](https://css-tricks.com/)
[Paletton](https://paletton.com/)
[CSS Selectors Reference](https://www.w3schools.com/cssref/css_selectors.php)
[CSS Diner - CSS selector game](https://css-diner.netlify.app/)
