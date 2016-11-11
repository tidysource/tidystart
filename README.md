# tidystart

## index.html
An empty HTML5 document.

## reset.css

## grid.css
Grid should solve dimension and positioning.

Columns less than a quarter width of row are rare. If necessary, those should be added as custom project CSS.

Grid gutters (margins) should be dealt with using padding.

### Width
Width is based on most common divisions of content and values of same denominator.
Each width is represented by a class name. The naming convention is simple and follows this pattern `w` + `numerator` + `-` + `denominator` 

See table below for class names.

|	Class	|	Width relative to container	|
|----------:|------------------------------:|
|	w1-2	|				1/2				|
|	w1-3 	|				1/3				|
|	w2-3	|				2/3				|
|	w1-4 	|				1/4				|
|	w2-4 	|				2/4				|
|	w3-4	|				3/4				|

__Notes__ 
adding width also sets element display property to inline block.
Since this grid relies on `display:inline-block;` it is imperative to make sure there is no white space between grid elements on the same line within HTML.
You can do this in two ways:

```html
<div class="w1-2">First half</div><div class="w1-2">Second half</div>
```

or by adding comments when using whitespace in your html

```html
	<div class="w1-2">First half</div><!--
 --><div class="w1-2">Second half</div>
```

This may not be ideal, but (for now) `display:inline-block;` means the least overhead when positioning elements. Once you get used to it, empty comments such as these are hardly annoying.

### Offset
Offsetting elements is possible by same divisions relative to the container.
For example to offset an element from the left side by 25% or 1/4 use a class named "offset1-4".

|	Class		|	Offset relative to container	|
|--------------:|----------------------------------:|
|	offset1-2	|				1/2					|
|	offset1-3 	|				1/3					|
|	offset2-3	|				2/3					|
|	offset1-4 	|				1/4					|
|	offset2-4 	|				2/4					|
|	offset3-4	|				3/4					|

These classes do so by adding the appropriate % left margin.