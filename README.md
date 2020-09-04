<!-- @format -->

# Social-Mockup
### Please NOTE:

#### Icons from font awesome are imported in the head of html. Because these are imported in the html head they will not be imported into codepen if one were to copy and paste there.
<br>
also

##### There is a .css file and a .scss file. Please use the .css file as the .scss file is used by and for Sass.

## Parent Relative, Children Absolute

From W3.org https://www.w3.org/TR/css-position-3/#abspos-layout :

> Absolute positioning not only takes a box out of flow, but also lays it out in its containing block (after the final size of the containing block has been determined) according to the absolute positioning layout model

<br>

### Summary:

I learned while doing this assessment, that when you absolutely position a box it is absolutley positioned to its containing box. This is normally the body which is why absolutley positioned boxes normally appear stuck to the page.
<br>

### Use Case:

I was having problems with setting everything to relative with `margin:auto` because when I would resize the page not everything would stay in exact relation to each other. Sometimes the bottom section would move further to the left then the top section and things just would not stay lined up.
<br>

### Solution:

I then found out that if I wrapped all my code in a box I'll call "page-wrapper" I could set this "page wrapper" to `position:relative`, then everything inside the "page-wrapper" I could set to `position:absolute`. This allowed me to specify where I wanted everything to stay in relation to the "parent-wrapper".
<br>
Since I was using `margin:auto` to center the "page-wrapper" when the page was resized the "page-wrapper" and everything inside would stay centered on the page.
<br>
The one thing to remember is that the "page-wrapper" must have a set width for this to work as noted from w3.org above.

### Here are a couple sites I found to help me figure out this was possible:

[Absolute Positioning Inside Relative Positioning](https://css-tricks.com/absolute-positioning-inside-relative-positioning/)
<br>

> A page element with relative positioning gives you the control to absolutely position children elements inside of it.
> To some, this is obvious. To others, this may be one of those CSS “Ah-ha!” Moments. I remember it being a big deal for me when I first “got it”.

[CSS Position: Relative vs Position Absolute](https://dzone.com/articles/css-position-relative-vs-position-absolute#:~:text=Relative%20%2D%20the%20element%20is%20positioned,related%20to%20the%20browser%20window)
<br>

> ...the parent element has the position set to relative. Now, when you set the position of the child element to absolute, any additional positioning will be done relative to the parent element.

## Used a variation of BEM for naming classes and used Sassy Sass for first time

I decided to start learning Sassy Sass by utilizing a few variables as well as nesting selectors.
<br>
Towards the end of finishing my assessment I decided to go through and change as many of my divs to use better semantics in my project. While doing so I realized I should also rename my class names to be more organized. This is why I decided to start using some [BEM](http://getbem.com/) naming conventions which allowed me to use the ampersand symbol while nesting selectors.
<br>
<br>
Since I wrote the CSS in the Sass or .scss file most of the comments I made can be found in the .scss file. I mostly made comments to describe different sections of the code and point out the wrappers I used for positioning.

> Comments can be found in the .scss file.

Since I was having problems positioning flexboxes I found if I wrapped them in a div I could then position the "wrapper" and declare `display:inline-flex` for the parent div of the flexbox.
<br>



<br>

#### Also I realize that the pictures not only do not have an alt tag they are also high resolution which has poor performance on slow connections. I used unsplash random photo for the photos.(They do look nice though)

<br>
<br>

# Assignment: Style a Social Network Page

## Create a header using what you have learned about the box model and how to position elements using CSS.

1. Header should be exactly 850 pixels wide (including borders)
2. Header should be centered within the full width of the screen

## Below the header, create a two-column layout.

1. The left column should be 328 pixels wide (including borders)
2. The right column should be 512 pixels wide (including borders)
3. The space between them should be 10 pixels wide.
4. This should match the 850 pixel wide header you previously created.

I used normal positioning with the "page-wrapper" set to relative and each part of the header positioned absolute, as well as the flexboxes and the whole grid were also positioned absolute using a wrapper to position each. For the bottom part all I could see when imagining how to do it was a grid. I actually used 4 grids on this page. I used one grid to position and size the 3 boxes. I used `grid-template-columns: 328px 512px` to make the two columns. I also used the `gap:10px` to create a gap between each box of 10px. I then imagined a grid of pictures inside one box since that was one of the mock-up examples. I successfully created grids inside my main grid to lay out the pictures.

## Mock up Goal to match:

<a href="https://imgur.com/PKAE7L2"><img src="https://i.imgur.com/PKAE7L2.png" title="source: imgur.com" /></a>

## Top Half Finished:

<a href="https://imgur.com/Lh6WAyJ"><img src="https://i.imgur.com/Lh6WAyJ.png" title="source: imgur.com" /></a>
