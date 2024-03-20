---
title: HTML5
draft: false
tags:
---
## HTML Tags 
### Basic Tags
- `<h1></h1>` header 1 (goes up to 6) 
- `<p></p>` paragraph  
- `lorem` + tab will automatically create a sample paragraph 
- `<strong></strong>` bold 
- `<em></em>` emphasized (ie. Italic)
- `<ol></ol>` ordered list, `<ul></ul>` unordered list
  - `<li></li>` list items 
### Self Closing Tags 
- `<br>` break 
- `<hr>` horizontal line
- `<img src="" width="40" height="40">` image 
### Anchor Tag
- `<a href="newpage.html">New Page</a>`  
  - You can wrap other basic tags with the anchor tag to link to other pages
## Student Q&A
### Why index.html? 
- By default, most servers return the `index.html` first so it’s good practice 
### Relative vs Absolute Path 
- Relative path: relative to where the current file is 
- Absolute path: no matter where you reference it, it will take you there
### HTML vs HTML5 
- Semantic elements are added in HTML5  
- For more info check out [w3schools](https://www.w3schools.com/html/)
## HTML Forms 
- `<form></form>` 
  - `<input type=“text” required>`
  - `<input type=“email” required>`
  - `<input type=“password” min=“5”>`
  - `<input type=“submit” value=“Register”>`
  - `<input type=“reset”>`
  - `<input type=“date”>`
  - `<input type=“radio” name=“gender”>`
  - `<input type=“checkbox”>`
  - `<select multiple>`
    - `<option value="">`
- `<!-- Comment -->` 
## Tags that’ll be relevant with CSS
- `<div>` block element 
- `<span>` inline element