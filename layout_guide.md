# Layout Guide

* Cells are laid out in left to right, top to bottom order.
* Images do not need to be cropped, they'll adjust to fit the container with no gaps.
* Images should not be larger than 1872px wide - 4K probably unnecessary. Save with jpeg quality 10 in photoshop.
* All images should go in the ```content/grid-images``` folder. This folder can then be uploaded to the same folder on the sever when done. The URLs in your template will not need to be changed on the live server.
* Breakpoints are currently using the browser window size and breaks at 768px. This will likely stay this way until container queries are a proper thing although the breakpoint can be changed.

## Cell

```html
<a class="cell span2-1" href="/products">
	<img src="content/grid-images/bsg-photo.jpg" title="Clearance Products"/>
	<div>
		<h1>Clearance Products</h1>
		<h2>Some text about the products</h2>
	</div>
</a>
```

```css
.span2-1
.span2-2
.span3-1
.span3-2
.span3-3
.span4-1
.span4-2
.span4-3
.span4-4
```

```css
.spanX-Y
```

X is the column span, Y is the row span.

```css
.aspect-wide-short
```

For use with 1 column layouts (```grid-1```) and you want a wide image that's also short in height.

```css
.no-hover
```

Disables the hover animation. Useful for static images with no link that still need to be a cell.

## Grids

```css
/* 1 Column */
.grid-1

/* 2 Column */
.grid-2

/* 3 Column */
.grid-3

/* 4 Column */
.grid-4
```

## Images

```css
.img-100w
```

Will give you an image that fits the container by width. Be careful as this could end up taking up the whole screen when the window is maximized unless the image is particularly short. Might be better to use a grid and then span the image across the whole width.