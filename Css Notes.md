
**HTML**
before learn of css we need to know how html works. html  is a _markup language_ that defines the structure of your content in the website, the structure of html consist in elements that are into a open tags and closing tags "<>, </>"

if we wanna put a simply paragraph we can use  the letter p into the tags like the example: 


```
<p>My cat is very grumpy</p>
```

and the output in the webpage is only "my cat is very grumpy " as a paragraph


the structure of this element is 
opening tag: "<p>"" that has the name of the element 
closing tag: "<  /p>"  that say where the element finish
the content: "cat is very grumpy" is the content of the element
element: is the opening tag , closing tag and element together


and also we can have attributes that are extra properties , are settings which handle how a we watch or how html element act and we put it in the opening tag

```
<p class="editor-note">My cat is very grumpy</p>
```

in that example we can see the attribute is editor-note 


Anatomy of html document

```
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image" />
  </body>
</html>
```

<!doctype html>: in the begginings doctypes work as a link with the rules of html , now only is only for make sure the html behaves correctly
`<html></html>`: is an element that wraps teh entire page of html and content the attr lang that describes the lenguague of the webpage

`<head></head>`: is all the stuff you want in the html page and that doenst shown in to the webpage 

`<meta charset="utf-8">`: put the set of characters in this case it use UTF-8
`<meta name="viewport" content="width=device-width">`: ensures tge page renders at the width of viewport
`<title></title>`: has the the title of the webpage

`<body></body>`: has al the content you want to show to the users, la images, videos etc


Html has different kinds of elements such as:
- Images:
```
<img src="images/firefox-icon.png" alt="My test image" />
```

that we can put the source image in the attr src to show the image 

-headings: 

```
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
```

heading is for put headers the greatest header is 1 then the header 2 , and so on 


-Links:
```
<a href="">Mozilla Manifesto</a>
```

yo can put hypertext whit that element and in the href attr put the link


For more information about html click here: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics




**CSS**



Css (cascading style sheets), is a markup language  and i sthe lenguage which to change the style of html elements.


the form to call the styles of css in the html  in the element <head >

```
<link href="styles/style.css" rel="stylesheet" />
```


**Anatomy of css ruleset**


```
p {
  color: red;
}
```

the selector: p is the html element 

declaration: `color: red;` it specifies which of the elements properties you want to style

properties: is the property you want to change 


property value: "red" is the value to change in the property 



if you want change multiple properties you can use semi colons , remember put semicolons after the selector 


```
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

you can select multiple elements with that form put comma after the element: 

```
p,
li,
h1 {
  color: red;
}
```



different types of selectors


element selector : you put the name of the element directly , 

`p`  
selects `<p>`


id selector: is a specific element of the page but with id 

`#my-id`  
selects `<p id="my-id">` or `<a id="my-id">`


```
#my-id{
  color: red;
}
```

class selector: the elements on the page with the specified class 
`.my-class`  
selects `<p class="my-class">` and `<a class="my-class">`

```
.my-class{
  color: red;
}
```


Attribute selector: the element on the page with specified attribute 

`img[src]`  
selects `<img src="my-image.png">` but not `<img>`

Pseudo-class selector: The specified element(s), but only when in the specified state. (For example, when a cursor hovers over a link.):

`a:hover`  
selects `<a>`, but only when the mouse pointer is hovering over the link.

Desendant combianator: select elements descendents from the another element 

```
body article p {
}
```

article is in body 

but is a direct child we use: 

```
ul > li {
  border-top: 5px solid red;
}
```

li , is the direct child from the ul:
```
<ul>
  <li>Unordered item</li>
  <li>
    Unordered item
    <ol>
      <li>Item 1</li>
      <li>Item 2</li>
    </ol>
  </li>
</ul>
```
we use + when we put styles to element only if it appears after the other element:
p + img { border: 5px solid red; }

**put special fonts on the html**


in the element <head> we put the font from google in the element link ```
<link
  href="https://fonts.googleapis.com/css?family=Open+Sans"
  rel="stylesheet" />
```


then we configure the html elment in the css file with the font we want and the size of the letters

```
html {
  font-size: 10px; /* px means "pixels": the base font size is now 10 pixels high */
  font-family: "Open Sans", sans-serif; /* this should be the rest of the output you got from Google Fonts */
}
```


**css layout**
![[box-model.png]]

- `padding`, the space around the content. In the example below, it is the space around the paragraph text.
- `border`, the solid line that is just outside the padding.
- `margin`, the space around the outside of the border.

explain : 
```
body {
  width: 600px;
  margin: 0 auto;
  background-color: #ff9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
}
```

width: defines how width the body is in that case is 600px
margin:0 auto; center the body horizontal, without a margin cause is 0 and calculate the margins left and right to center the body 

background-color: #ff9500;

put the color of the background of the body and the value is the color in rgb (is like an orange the color )

padding: 0 20px 20px 20px;
defines the padding of the body and you can see the numbers like a clock the first 0: without space in the top , then 20px , 20px in the right part, and so on


border: 5px solid black, 

5px is the wide of the border and after we can see the color which is solid black


you can see mor information in: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics


**How css works**


first whats the DOM (document object model): is a standart model that represent the structure of a html document to a tree nodes, in the dom is where the html and css meetup


how css works: 

![Rendering process overview](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works/rendering.svg)


1: html is load
2: html is converting in a DOM
3: the browser add the resources like images, videos and the linked css= <link rel="stylesheet" href="estilos.css">
4: the browser search the different slectors based in the type of selectors it deppends how is apllied in to the DOM
5:the browser render the page after the rules of the selectors
6: the visual display of the display is shown on the screen


to more information visit: https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works




**Cascade in css**

if we put two or more declarations in the same selector wins the last declaration, for example: 

```
h1 {
  color: red;
}
h1 {
  color: blue;
}
```

the second h1 wins and the color will be blue


**specificity**

when we have two selectors of the same element it takes the more specific in that example we have the element selector and the class selector for be more specific it takes class selector 

```
.main-heading {
  color: red;
}

h1 {
  color: blue;
}
```
so instead of take the blue it takes the color red


**inheritance**

when we have a nested element the if the principal element has the a specific property value it shows up in all the element, but if we have a selector of specific element it changes to it value

```
body {
  color: blue;
}

span {
  color: black;
}
```

for example span is in body but it has the black color cause we specify that in the selector

**Cascade layers**
is used to organize  and prioritize the styles rules more clear, it helps in a big projects where we have multiple css fonts


```
/* file: layers1.css */

/* unlayered styles */
body {
  color: #333;
}

/* creates the first layer: `layout` */
@layer layout {
  main {
    display: grid;
  }
}

/* creates the second layer: an unnamed, anonymous layer */
@layer {
  body {
    margin: 0;
  }
}

/* creates the third and fourth layers: `theme` and `utilities` */
@layer theme, layout, utilities;

/* adds styles to the already existing `layout` layer */
@layer layout {
  main {
    color: #000;
  }
}

/* creates the fifth layer: an unnamed, anonymous layer */
@layer {
  body {
    margin: 1vw;
  }
}
```

it takes from the last from the first statement; 


**box model in css**

![[Pasted image 20241212102537.png]]


-content box: the area where your content is displayd size it with, inline-size, cloxk-size, height, width

-padding box: padding sit around the content as white space, we use the padding special name
-border: the border box wraps the content and any padding; we use border
-margin box: wrap all the element we said before, and we use padding 


a example of a box is: 

```
.box {
  width: 350px;
  height: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}
```


**handling different text directions**

writing-mode is used to put the direction on the text for example, 

```
body {
  font-family: sans-serif;
  height: 300px;
}
h1 {
  writing-mode: vertical-rl;
  color: white;
  background-color: black;
  padding: 10px;
}
```



that text is put on vertical-rgiht to the left and we have diferent words like;

horizontal-tb: top-to-bottom block flow direction, sentences run horizontally

vertical-rl: vertical to the left

vertical-lr: vertical to the right 


**overflow content**

is when the content of the element dont fit in the dimensions of the element (width, height)


you can fit it with the property overflow:
```
<div class="box">
  This box has a height and a width. This means that if there is too much
  content to be displayed within the assigned height, there will be an overflow
  situation. If overflow is set to hidden then any overflow will not be visible.
</div>

<p>This content is outside of the box.</p>
```

```
.box {
  border: 1px solid #333333;
  width: 250px;
  height: 100px;
  overflow: hidden;
}
```

![[Pasted image 20241212105125.png]]


we can surf in to teh text with a scroll if we put 

overflow: scroll;

and we can put the scroll in diferents axes (x,y) y for vertical and x for horizontal

```
.word {
  border: 5px solid #333333;
  width: 100px;
  font-size: 250%;
  overflow-x: scroll;
}
```

**css values and units**

![[Pasted image 20241212105530.png]]

![[Pasted image 20241212105554.png]]

![[Pasted image 20241212105630.png]]



**example of sizing elements**

```
<div class="box">I have margin and padding set to 10% on all sides.</div>
```

```
body {
  font: 1.2em sans-serif;
}
.box {
  border: 5px solid darkblue;
  width: 200px;
  margin: 10%;
  padding: 10%;
}
```
![[Pasted image 20241212110259.png]]



**sizing images**


if the image is greater tahn the container sizes we use object-fit to fit that elemnt in the container correctly:

```
<div class="wrapper">
  <div class="box">
    <img
      alt="balloons"
      class="cover"
      src="https://mdn.github.io/shared-assets/images/examples/balloons.jpg" />
  </div>
  <div class="box">
    <img
      alt="balloons"
      class="contain"
      src="https://mdn.github.io/shared-assets/images/examples/balloons.jpg" />
  </div>
</div>
```

```
.wrapper {
  display: flex;
  align-items: flex-start;
}

.wrapper > * {
  margin: 20px;
}

.box {
  border: 5px solid darkblue;
  width: 200px;
  height: 200px;
}

img {
  height: 100%;
  width: 100%;
}

.cover {
  object-fit: cover;
}

.contain {
  object-fit: contain;
}
```



when we use contain the object change the scale to fit correctly into the conteiner.

**styling form**

```
<form>
  <div><label for="name">Name</label> <input id="name" type="text" /></div>
  <div><label for="email">Email</label> <input id="email" type="email" /></div>

  <div class="buttons"><input type="submit" value="Submit" /></div>
</form>
```
```
input[type="text"],
input[type="email"] {
  border: 2px solid #000;
  margin: 0 0 1em 0;
  padding: 10px;
  width: 80%;
}

input[type="submit"] {
  border: 3px solid #333;
  background-color: #999;
  border-radius: 5px;
  padding: 10px 2em;
  font-weight: bold;
  color: #fff;
}

input[type="submit"]:hover,
input[type="submit"]:focus {
  background-color: #333;
}
```

and if we wanna use inheritance we can put like that: 
```
button,
input,
select,
textarea {
  font-family: inherit;
  font-size: 100%;
}
```


**styling tables**
```
<table>
  <caption>
    A summary of the UK's most famous punk bands
  </caption>
  <thead>
    <tr>
      <th scope="col">Band</th>
      <th scope="col">Year formed</th>
      <th scope="col">No. of Albums</th>
      <th scope="col">Most famous song</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Buzzcocks</th>
      <td>1976</td>
      <td>9</td>
      <td>Ever fallen in love (with someone you shouldn't've)</td>
    </tr>
    <tr>
      <th scope="row">The Clash</th>
      <td>1976</td>
      <td>6</td>
      <td>London Calling</td>
    </tr>

    <!-- several other great bands -->

    <tr>
      <th scope="row">The Stranglers</th>
      <td>1974</td>
      <td>17</td>
      <td>No More Heroes</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row" colspan="2">Total albums</th>
      <td colspan="2">77</td>
    </tr>
  </tfoot>
</table>
```
```
/* spacing */

table {
  table-layout: fixed;
  width: 100%;
  border-collapse: collapse;
  border: 3px solid purple;
}

thead th:nth-child(1) {
  width: 30%;
}

thead th:nth-child(2) {
  width: 20%;
}

thead th:nth-child(3) {
  width: 15%;
}

thead th:nth-child(4) {
  width: 35%;
}

th,
td {
  padding: 20px;
}
```


the table-layout: fixed;: saids the width of the columns will be calculate wuth the total width and the width of the columns



width: 100% the table use the 100% of the container

thead th:nth-child(n): selects the header th in teb position n in to the row <thead>

for example thead th:nth-child(1): aplies to the first header


and width: x%, is to describe the width of the header



**advanced styling effects**

we have for example a shadow 

```
<article class="simple">
  <p>
    <strong>Warning</strong>: The thermostat on the cosmic transcender has
    reached a critical level.
  </p>
</article>
```

```
p {
  margin: 0;
}

article {
  max-width: 500px;
  padding: 10px;
  background-color: red;
  background-image: linear-gradient(
    to bottom,
    rgb(0 0 0 / 0%),
    rgb(0 0 0 / 25%)
  );
}

.simple {
  box-shadow: 5px 5px 5px rgb(0 0 0 / 70%);
}
```

![[Pasted image 20241212114021.png]]
![[Pasted image 20241212114433.png]]




And also we can put filters, like gray of blurry, with the property filter: 

```
<div class="wrapper">
  <div class="box">
    <img
      alt="balloons"
      class="blur"
      src="https://mdn.github.io/shared-assets/images/examples/balloons.jpg" />
  </div>
  <div class="box">
    <img
      alt="balloons"
      class="grayscale"
      src="https://mdn.github.io/shared-assets/images/examples/balloons.jpg" />
  </div>
</div>
```
```
img {
  height: 100%;
  width: 100%;
  display: block;
  object-fit: cover;
}

.blur {
  filter: blur(10px);
}

.grayscale {
  filter: grayscale(60%);
}
```

![[Pasted image 20241212114614.png]]



if you want more information visit: https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks



**flexbox**

examples of use from froggy game: 
Flexbox Froggy

Use justify-content again to help these frogs get to their lilypads. Remember that this CSS property aligns items horizontally and accepts the following values:

    flex-start: Items align to the left side of the container.
    flex-end: Items align to the right side of the container.
    center: Items align at the center of the container.
    space-between: Items display with equal spacing between them.
    space-around: Items display with equal spacing around them.
    
    
 Now use align-items to help the frogs get to the bottom of the pond. This CSS property aligns items vertically and accepts the following values, we can use align-self for only one item:

    flex-start: Items align to the top of the container.
    flex-end: Items align to the bottom of the container.
    center: Items align at the vertical center of the container.
    baseline: Items display at the baseline of the container.
    stretch: Items are stretched to fit the container.
    
    
 The frogs need to get in the same order as their lilypads using flex-direction. This CSS property defines the direction items are placed in the container, and accepts the following values:

    row: Items are placed the same as the text direction.
    row-reverse: Items are placed opposite to the text direction.
    column: Items are placed top to bottom.
    column-reverse: Items are placed bottom to top.
    
Oh no! The frogs are all squeezed onto a single row of lilypads. Spread them out using the flex-wrap property, which accepts the following values:

    nowrap: Every item is fit to a single line.
    wrap: Items wrap around to additional lines.
    wrap-reverse: Items wrap around to additional lines in reverse.
    
    
The two properties flex-direction and flex-wrap are used so often together that the shorthand property flex-flow was created to combine them. This shorthand property accepts the value of the two properties separated by a space.

For example, you can use flex-flow: row wrap to set rows and wrap them.

Try using flex-flow to repeat the previous level.

The frogs are spread all over the pond, but the lilypads are bunched at the top. You can use align-content to set how multiple lines are spaced apart from each other. This property takes the following values:

    flex-start: Lines are packed at the top of the container.
    flex-end: Lines are packed at the bottom of the container.
    center: Lines are packed at the vertical center of the container.
    space-between: Lines display with equal spacing between them.
    space-around: Lines display with equal spacing around them.
    stretch: Lines are stretched to fit the container.

This can be confusing, but align-content determines the spacing between lines, while align-items determines how the items as a whole are aligned within the container. When there is only one line, align-content has no effect.


**css grid **

we put the container in mode grid putting in display grid instead of flex
```
.container {
  display: grid;
}
```


we can create columns with grid-template-columns:
```
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px;
}
```

![[Pasted image 20241212145931.png]]


we can use the unit fr , how it works?

for example if i create 1fr 1fr 1fr, im creating 3 columns of 1/3 each one couse are 3 columns

```
.container {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
}
```

![[Pasted image 20241212150508.png]]


in that example we have 2/4 1/4 /14



and we can put a gap between the columns:

![[Pasted image 20241212150633.png]]

