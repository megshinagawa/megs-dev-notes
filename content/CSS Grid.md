---
Type: Learning
Course: ZTM
---
CSS Grid vs Flexbox vs Bootstrap 
- CSS grid is great if you're trying to make something in a 2D formation 
- Bootstrap came about before CSS grid came out
- Very important to know CSS grid as opposed to Bootstrap 
## CSS Grid 
```CSS 
.container {
	display: grid;
	gap: 20px;
	grid-template-columns: repeat(3, 1fr);
	grid-template-rows: 1fr;
}
.green {
	grid-column: span 2;
	grid-row: 1/3;
}
```

```CSS
grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
```
## CSS Grid Cheatsheet 
- https://grid.malven.co/