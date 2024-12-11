
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




