
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
















