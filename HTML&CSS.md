# One HTML Fundamental

HTML is a Markup language, which is called Hyper Text Markup Language.

## 1.1 HTML  structure

```HTML
<!DOCTYPE html>
<!-- Every HTML document needs to be started with this DOCTYPE -->
<!-- The purpose is to let the browser know that we are actually using HTML in this file and all browsers will then
     know that they should use the HTML5 specifications to render this file 
-->
<html lang="en">
      <!-- The default borwser language is setted to English -->
  <head>
      <!-- The head element is basically for things that are not visible in browser window -->
    <meta charset="UTF-8" />
      <!--Set the browser's character to UTF-8.-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
      <!-- External CSS -->
    <link rel="stylesheet" href="style.css" />
        <!-- Internal CSS -->
    <style>
      /* {} is  the declaration block */
      /* Seperate our HTML and CSS */
      /* h1 {
        color: blue;
      } */
    </style>
  </head>

  <body>
    </body>
</html>

```

## 1.2 Semantic HTML



### 1.2.1 The definition of semantic HTML:

First of all, it is crucial for us to know semantic HTML. What I mean is that any certain element has a meaning or a purpose attached to them, so when we think about a certain HTML element, It’s the meaning of the elements that deserves our attention, instead of what they are rendered on the page. 



### 1.2.2 Why should we use sematic HTML?

1. Search engine optimization which basically means that a search engine such as Google will be able to understand the structure of your content. And therefore they will be better able to analyze what your content and what your web page is all about.

2. Writing semantic HTML is extremely important for accessibility, especially for people who rely on screen readers to surf web pages.

3. I also want to make it very clear from the very beginning that when we think about HTML, we should not only think about how it actually looks like in  the browser, but even more about what these elements actually mean and what they stand for.[problem here]

   

## 1.3 HTML Element



### 1.3.1 Basic element

#### body element

The body element is the parent of all the other elements in HTML document.

```html
<body>
    
</body>
```



#### link element

```html
<link rel="stylesheet" href="style.css">			//Import CSS file
```

Style and link are placed inside head.

#### a element

```html
<a>
     href="https://developer.mozilla.org/zh-CN/"      <-- Inside href is the url of the page ->
     target="_blank"> 						          <--target is a property of how the page was opened ->
     MDN Web Docs.
</a>
```



#### em element

The semantics of it means emphasize  

```html
<em>fundamental</em>
```

![image-20231105145240368](./assets/image-20231105145240368.png)

#### italic element

```html
<i>fundamental</i>
```

![image-20231105145530340](./assets/image-20231105145530340.png)

Tips: In HTML 5, we use em element instead of the i element.



#### strong element

strong element has no semantics.



```html
 <P>
        <!-- strong elements can be displayed in bold but it do not have semantics -->
        Posted by <strong>Laura Jones </strong>on Monday, June 21st 2027
</P>
```



#### ul element



```html
 <!-- undered-list -->
	<ul>
        <!-- sematics:list item -->
        <li>To be able to use the fundamental web dev language</li>
        <li>To hand-craft beautiful websites instead of relying on tools like Worpress or Wix</li>
        <li>To build web applications</li>
        <li>To impress friends</li>
        <li>To have fun 😃</li>
    </ul>
```



#### ol element 

```html
 <!-- ordered-list -->
    <ol>
        <!-- sematics:list item -->
        <li>The opening tag</li>
        <li>The closing tag</li>
        <li>The actual element</li>
    </ol>
```



#### p element

```html
<P>

        In this post, let's focus on HTML.

        We will learn what HTML is all about,

        and why you too should learn it.

</P>
```



#### img element

```html
 <img 
      src="laura-jones.jpg"                          			//resource Address of the photo
      alt="Headshot of laura-jones" 
      //Photo captions, care for the visually impaired, access to browser resources using screen readers
      width="50px" 								//Photo display width
      height="50px"							   //Photo display height
 >
```





#### h1~h6 element

```html
<h1>Level 1 title</h1>
```



### 1.3.2 New elements in HTML5



#### header

```HTML
<header> 
	Writing the header content of a web page
</header>
```


#### nav

```html
<nav>
		Write the contents of the navigation bar
</nav>
```



#### article

```html
<article>
Write the content of the article, here the article refers to the broad scope, not only text, but also can be put into other elements, such as video, images, et cetera.
<article/>
```



#### aside

Secondary information on the page

```html
<aside>
	Posts related to arcticle content  
</aside>
```



#### footer

```html
<footer>
    Copyright &copy;2027 by the Code Magazine             
    <!--The copyright information at the end &copy are html entities, you can check the table to find some useful entities-->
</footer>

```

Here is the link of [HTML entities.](https://css-tricks.com/snippets/html/glyphs/), which is the web page written by my teacher [Jonas Schmedtmann](https://twitter.com/jonasschmedtman)



# Two CSS Fundamental

## Section 1


In this section, we’ll talk about  how to add visual styles and spacing to elements.



### 1.1 Definition of  CSS

CSS means Cascading Style Sheets it is also one of the core technologies of the web



### 1.2 CSS applications


We use CSS to describe the visual style and presentation of the content that we previous wrote using HTML. CSS consists of countless properties that developers use to format the content properties about font , text, general spacing,layout of the page,et cetera. Each properties can take different types of values, such as length or key words. 



### 1.3 Constitute


The image below shows us the constitute of CSS.

<img src="./assets/image-20231105160655254.png" alt="image-20231105160655254" style="zoom:67%;" />



### 1.4 CSS type


There are three types of CSS Inline CSS, Internal CSS and External CSS.

#### 1.4.1 Inline CSS

Inline CSS is not recommended to use. It is written inside of each element.

```HTML
  <h1 style="color:RGB(40,135,245)">📘 The Code Magazine</h1>
```


The result of the code above:

 <h1 style="color:RGB(40,135,245)">📘 The Code Magazine</h1>





#### 1.4.2 Internal CSS



Internal CSS is written inside of the header of the HTML file.

```CSS
 <style>
  h1 {
      color: blue;
    } 
  </style>
```





#### 1.4.3 External CSS



External CSS is a css file which css styles are written in it.

```HTML
<link rel="stylesheet" href="style.css">			//import external CSS file
```



### 1.5 Selector

When we want to set some kind of CSS style for HTML elements, we have to use selector to select some kind or other to set CSS style for them.

#### 1.5.1 Types:



##### 1 Important  Key  Word

Usually, we don't use this selector unless it's absolutely necessary.

```HTML
<footer>
    <p id="Copyright">
      Copyright &copy; 2027 by The Code Magazine.
    </p>
  </footer>
```



```CSS
footer p {
    font-size: 16px;
      /* important selector owns the highest priority  */
    color: green !important;
}

```

#### 2 Universal Selector

The Universal selector is useful if we actually want a certain property applied to all elements but which does not get inherited. So the universal selector simply applies to all the elements, and there is no inheritance involved. And therefore, this is perfect if you want to apply a certain property, that does not automatically get inherited to all the elements. On the other hand, any elements we put into the body gets inherited. And so that's completely different mechanism than using the universal selector.

```CSS
* {
  /* border-top:7px solid green;  */
  /* This kind of global reset is actually extremely common  */
  margin: 0;
  padding: 0;
  /* it actually can be easily overwritten */
}
```



#### 3 Element Selector

```CSS
h1 {
    color: blue;
    font-size: 26px;
    /* Set text to uppercase */
    text-transform: uppercase;
    /* Set the form of the font to italic */
    font-style: italic;
}


```



#### 4 List  Selector

```CSS
h1,
h2,
h3,
h4,
p,
li {
    /* sans-serif(typography) */
    font-family: sans-serif;
}
```



#### 5 Descendant selector

```CSS
footer p {
    font-size: 16px;
}
```



#### 6 Hash Selector(ID Selector)

```CSS
 <p id="Copyright">
      Copyright &copy; 2027 by The Code Magazine.
    </p>
```

ID can not be repeatly used.



#### 7 Class Selector

```CSS
.main-header {
    background-color: #f7f7f7;
}
```



#### 8 Pseudo Selector

 We can actually have CSS automatically figure out which is the first li element inside of a container.

```html
<ul>
          <!-- the li element is the first element of its parent ul element -->
          <!-- so if we use pseudo class to style the fist li elemnt in ul, the li element must be the first 			element of the ul element
        in this case,p element is the first element of the ul,so the pseudo class dosen't work -->
          <!-- let's comment it -->
          <!-- <p>test</p> -->
          <!-- And then the pseudo class will work, and the first li will be styled to bold -->
          <li class="first-li">
            To be able to use the fundamental web dev language
          </li>
          <li>
            To hand-craft beautiful websites instead of relying on tools like
            Worpress or Wix
          </li>
          <li>To build web applications</li>
          <li>To impress friends</li>
          <li>To have fun 😃</li>
        </ul>
```



```CSS
/* use a pseudo class */

/* Style the first child of its parent elements */

li:first-child {
    /* the first li element will be bolded */
    font-weight: bold;
}

li:last-child {
    /* the last li element will be italic */
    font-style: italic;
}

li:nth-child(2) {
   /*the color of the second li element will be red.*/
    color: red;
}

/* set all the odd element to be red */
li:ntn:nth-child(odd)
{
  color:red
}

/* we can also do even */
 li:nth-child(even) {
  color: blue;
}

/* This techneque is quite useful, for example, to style tables, which oftentimes have like alterning background colors */
```

The pseudo-class selector selects the elements in the current list in the order in which they are selected.

#### 9 link Style

Now we will learn how style hyperlinks using pseudo classes

```CSS
/* Styling Links
   We shouldn't simply select the anchor and style it instead we should style a pseudo class of the anchor
   because that will then allow us to target different states */
/* Remenber thar when we set pseudo class for the anchor element, the order is LVHA! */
/* The first one is the link pseudo class */

/* a:link only target at anchor elments that do actually have href(Hypertext Reference) attribute  */
a:link {
  color: #170fff;
  /* get rid of the underline */
  text-decoration: none;
}

/* the visited pseudo class */
a:visited {
  /* set the anchor's color after visiting the anchor */
  color: #170fff;
}

/* the hover pseudo class */
/* In the hover pseudo class we can define any styles that we want to be applied to the anchor
   as soon as the element is hovered by the mouse
*/
a:hover {
  color: orange;
  /* set the decoration of the link while it is horvered by the mouse */
  text-decoration: underline dotted orange;
}

/* active pseudo class */
/* This is the state in which we are actually clicking */
/* So when we do actually click on a link, then the act of pseudo class is edited to the element and we can then select
   that here like this.
*/
a:active {
  background-color: black;
  font-style: italic;
}

/* 
  These four states are always defined in this exact order, always link,visited,hover and active  (LVHA) 
*/

/* A couple of fundamental and really important theoretical concepts that we really need to undstand to master CSS */
```



#### 10 adjacent sibling selector

For example, the adjacent sibling of this h3 is this paragraph here. So basically the adjacent element is the sibling that comes after it.

![image-20231108103809842](./assets/image-20231108103809842.png)

CSS:

```css
/*A sibling element is bascially an element that is part of the same parent.
Now the adjacent sibling is a sabling that is actually the very next element 
*/
h3 + p::first-line {
  color: red;
}
```

Here is the resulta

![image-20231108104223520](./assets/image-20231108104223520.png)

#### 2.5.2  Conflicts between Selectors:



The priority of different selectors

1. The highest priority is the declarations marked with the important keyword.(!)
2. The next is Inline styles
3. The next is the ID selector(#ID-name{}), and if there are multiple ID selectors, then it is the last of those selectors that get apply
4. The next in the priority is the Class selector or a Pseudo class selector. （.class-name{}）And, again, if there are multiple ones of those, then it is the last selector of those in the code that get applied. 
5. Then the next is the Element selector(div p a li...)
6. And then is the Universal Selector（*）which is the one with the lowest priority of all.

To sum it up: Important key word(!) > Inline Style > ID Selector > Class Selector or Pseudo Selector >Element Selector > Universal Selector(*)



When a selector is faced with conflicting attributes, it will decide on the conflicting attribute values based on the selector's priority, and for the rest of the non-conflicting parts, the rules set within the selector will still work.

#### 2.5.3  Resolving style conflicts

What we should probably do is to write simpler selectors. Always write our selectors as simple as possible, and do not add too much

 nesting, or don't add too many IDs, and classes all in the same selector.

####  2.6 Element Display property



### 1.6.1 Block-Level element

Element like body, main, header, footer, section, nav, aside, div, h1-h6, p, ul, ol, li, et cetera.

<img src="./assets/image-20231105172122766.png" alt="image-20231105172122766" style="zoom: 50%;" />

Block element will occupy the entire width of the parent element, each block element will occupy a whole line. 

Here is the example

<img src="./assets/image-20231105160547678.png" alt="image-20231105160547678" style="zoom:50%;" />

with CSS: 

```CSS
selector{
    display:   block;
}
```



#### 1.6.2 Inline element

Like the strong element, em element, a element, img element, button element, et cetera.

<img src="./assets/image-20231105172158408.png" alt="image-20231105172158408" style="zoom:67%;" />



The inline element actually occupy exactly the space that is needed for its contents. They also don't create any line breaks after or before the element. And so therefore they can simply stay inside of their parent elements without creating any additional space. 

For example:  

<img src="./assets/image-20231105160616915.png" alt="image-20231105160616915" style="zoom:50%;" />

Keep in mind, for inline elements, the height and width property do not have any effect. Also paddings and margins are only applied horizontally or in other words, on the left and right sides, but not on the top and bottom.   

with CSS: 

```CSS
selector{
    display:   inline;
}
```



For a deeper understanding of the difference between block element and inline element, let’s go to the google browser to debug it.

The first image is <p> element which is actually a block element. We can see that when the margin attribute is set for this block element, space is created both horizontally and vertically.

<img src="./assets/image-20231105185133653.png" alt="image-20231105185133653" style="zoom:50%;" />



The inline element a with the margin attribute set simply creates space only horizontally, but not vertically.

<img src="./assets/image-20231105185306839.png" alt="image-20231105185306839" style="zoom:50%;" />

#### 1.6.3 Inline-block element



What makes even more sense is to transform a block-level element into something called inline-block element. So basically  

that is a mix of inline and block-level. So let’s quickly check it out what that means.

<img src="./assets/image-20231105172326412.png" alt="image-20231105172326412" style="zoom:67%;" />





We can still set width and heights, margins and paddings on a inline-block element just like on block-level boxes or block-level elements. So essentially, inline-block boxes really combines the best of both advantages of block-level and inline.



For example:

We are able to convert  an a element (inline element) to an inline element, all we need to do is change the display attribute to inline-block and then set margins for it. After that each a element can be separated by a certain distance


<img src="./assets/image-20231105184424844.png" alt="image-20231105184424844" style="zoom:50%;" />





### 1.7 Positioning modes



#### 1.7.1 Normal FLOW


So starting from the normal flow, it is simply the default positioning of elements on our page. We can achieve the normal flow by setting position to the value of relative. So in this case, we say that an element is ‘in flow’, which basically means  that the elements are laid out according to the source code in the HTML.   

<img src="./assets/image-20231106133109803.png" alt="image-20231106133109803" style="zoom: 50%;" />

#### 1.7.2 Absolute positioning



Now on the other hand, we have absolute positioning which basically allows us to absolutely position elements anywhere on the page. Now we are able to achieve this  positioning mode, so we can position an element absolutely by setting its position property to the value of absolute. And so in this case, the element is then removed from the normal flow, and we say it is out of flow. What happened with this element is that it completely loses any impact on surrounding elements. And in fact, it might even overlap them. So that is something quite common that happens with absolutely positioned elements. In order to actually position the element that is absolutely positioned, we can use the top, bottom, left or right properties to achieve the goal. And that positioning is going to happen in relation to a relatively positioned container. 



<img src="./assets/image-20231106172452041.png" alt="image-20231106172452041" style="zoom:67%;" /> 



It is important to know that the button element has been completely taken out of the flow, and it is now even hovering over this content. So it is as if the rest of the content here is not even there. And that is becoming even more apparent  



Now what’s important is not to use. We use absolute positioning for single elements like a button or other small things.





### 1.8 Pseudo element

Tips:

1. Any pseudo element is an inline element. So if we want to give it any padding, we want the box model to apply to it normally, we need to render this element as a inline block box.
2. Pseudo element is actually not a specific element in HTML.

#### 1.8.1 :: first-letter

```css
/* pseudo element use two colons */
/* Style the very first letter. */
h1::first-letter {
  font-style: normal;
  margin-right: 5px;
}

```

Now the first emoji letter becomes to be normal.

![image-20231108111147534](./assets/image-20231108111147534.png)

#### 1.8.2 :: first-line



```css
h1::first-line {
  font-style: normal;
  margin-right: 5px;
}

```



Now the first line of h1 element becomes to be normal and have 5px margin-right.


![image-20231108111323794](./assets/image-20231108111323794.png)





#### 1.8.3 :: after



The after pseudo element create a pseudo element that will automatically be the very first child of the selected element.
This can actually be quite useful for some small cosmetic style for which we don’t want to necessarily add a new element to the HTML. So let me show you what I mean by that.



```css

h2 {
  position: relative;
}

h2::after {
  content: "TOP";
  background-color: #ffe70e;
  font-size: 16px;
  font-weight: bold;
  /*  Any pseudo element is an inline element.
    So if we want to give it any padding, we want the box model to apply to it normally, 
    we need to render this element as a inline block box. */
  display: inline-block;
  padding: 5px 10px;
  position: absolute;
  top: -10px;
  right: -25px;
  color: #444;
}

```



![image-20231108114526581](./assets/image-20231108114526581.png)



## Section 2


One of the main application of CSS is to build layouts. And so that’s what we’re gonna do next. In this section we will

learn how to build layouts by using floats and also using two really modern technologies, which are called flexbox and CSS Grid. 	



### 2.1 Definition of Layouts




1. Layouts is the way text, images and other content is placed and arranged on a webpage
2. Layout gives the page a visual structure, into which we place our content
3. Building a layout: arranging page elements into a visual structure, instead of simply having
   them placed one after another (normal flow)


<img src="./assets/image-20231108174529139.png" alt="image-20231108174529139" style="zoom:67%;" />



### 2.2 Three ways of building layouts



![image-20231108175825472](./assets/image-20231108175825472.png)



#### 2.2.1 Float layouts



Similarities and differences between absolute positioning and floats



![image-20231108183556844](./assets/image-20231108183556844.png)


The original layouts

![image-20231108183926025](./assets/image-20231108183926025.png)




```HTML
          <img
            src="img/laura-jones.jpg"
            alt="Headshot of Laura Jones"
            height="50"
            width="50"
            class="author-img"
          />

          <!-- <Strong></Strong> ||<b></b> will bold the text "Laura Jones"-->
          <!-- However in HTML5 we should use Strong instead of <b> element -->
          <!-- We give the p element an ID, and now this element here in this paragraph is basically called author -->
          <p id="author" class="author">
            Posted by <strong>Laura Jones</strong> on Monday, June 21st 2027
          </p>
```



```css
/* Section2 Floats */
.author-img {
  float: left;
  /* What is going to happen is that this image is basically going to be taken out of the document flow.
  Just like an absolutely positioned element.Now the difference here with floats is that all the other elements
  are basically float around it. */

  /* A float element can still create some margins around them */
  margin-bottom: 20px;
}

.author {
  float: left;
  margin-top: 10px;
  margin-left: 20px;
}

```


The final layouts after using float.

![image-20231108183748651](./assets/image-20231108183748651.png)



Float layouts


<img src="./assets/image-20231108193912591.png" alt="image-20231108193912591" style="zoom: 50%;" />




<img src="./assets/image-20231108193852333.png" alt="image-20231108193852333" style="zoom:50%;" />



![image-20231108193748748](./assets/image-20231108193748748.png)





#### 2.2.2 Flex layouts

Flex items are the child elements of the flex container

By default, the space taken up horizontally by each flex item is exactly the space needed for its content and the space taken up vertically by each flex item is the same as the highest element

Here is the example:

<img src="./assets/image-20231109153431206.png" alt="image-20231109153431206" style="zoom:50%;" />

The width of each flex item is exactly the space needed for its content, and the height of each item is the same as the highest item

##### 2.2.2.1 The application of flex layouts

It helps us to simplify center alignment, top box alignment, bottom alignment et cetera.

center alignment:
	All we need to do is set the parent box’s display property to flex and then set align-items to center and then set  justify-content to center.

<img src="./assets/image-20231109160704398.png" alt="image-20231109160704398" style="zoom:50%;" />



top alignment:

​	All we need to do is set the parent box’s display property to flex and then set align-items to start.
<img src="./assets/image-20231109155429866.png" alt="image-20231109155429866" style="zoom:67%;" />


bottom alignment

​		All we need to do is set the parent box’s display property to flex and then set align-items to end.

![image-20231109155505237](./assets/image-20231109155505237.png)



##### 2.2.2.2 The definition and effects of flexbox



![image-20231109190033303](./assets/image-20231109190033303.png)

How to use flexbox?

The element which we want to use flexbox is called the flex container. And all we have to do in order to create a flex container is to set its display property to flex. And that is how we get started with flexbox. So if we do this, then all the direct children of that flex container will become the so-called flex items.


We can actually change the direction of the main axis, and so therefore also the cross axis. Plus we can align elements along the main axis and along the  cross axis in different ways. And therefore we always need to know which axis we are dealing with. 


![image-20231109192151622](./assets/image-20231109192151622.png)







##### 2.2.2.3 Flexbox properties


![image-20231109192945330](./assets/image-20231109192945330.png)




```css
 /* align-items is to align items along the cross axis, which by default is vertically
align-items will make all flex items have the same alignment
*/
align-items: center;
/* justify-content is basically to align items along the main axis which by default is horizontally*/
justify-content: flex-start;
```

###### align-selef

align-self sets the alignment for a single flex element.
Here is the example

![image-20231111155742115](./assets/image-20231111155742115.png)

###### justify-content

To align items along main axis(horizontally, by default)

justify-content: When we want to set the display of the content in the flexbox, we can use the justify-content attribute, when set to space-between, the elements inside the flexbox will automatically calculate the spacing between the elements, and because the main-header dev container contains only the H1 and the navigation bar these two elements, they will occupy the left and right sides of the box respectively, and leave the middle empty, thus achieving the effect we used float left and right before.

<img src="./assets/image-20231115162236138.png" alt="image-20231115162236138" style="zoom: 200%;" />

###### align-items

To align items along cross axis(vertically, by default)

By using the align-items attribute, it is possible to align elements by automatically calculating the distance, rather than manually adding padding or margins, which will greatly improve coding efficiency and spacing accuracy.

![image-20231115163642323](./assets/image-20231115163642323.png)



###### gap

The gap attribute will set the spacing for the elements inside the flexbox, as shown below.

![image-20231115172715453](./assets/image-20231115172715453.png)



###### order

By default, the value of the order attribute is 0. When we set an element's order attribute to be less than 0, the smaller the order value, the more it will be displayed as the first element, and the larger the number (more than 0 is fine), the more it will be displayed as the next element.

![image-20231116121930150](./assets/image-20231116121930150.png)



###### flex-basis

The flexbox automatically calculates the space size that best fits the element. When we want to manually change the size of an element in the flexbox, we shouldn't use width and height, but rather the flex space flex-basis.**`flex-basis`** Specifies the initial size of the flex element in the major-axis direction. If box-sizing is not used to change the box model, then this attribute determines the size of the flex element's content-box.
In this example, we specify the width of the aside element to be 300px, and since flexboxes often shrink the size of an element, we set the default values of flex-grow and flex-shrink from 0 and 1 to 0 and 0 here. That is because flexbox likes to automatically shrink these elements. 

![image-20231115174450496](./assets/image-20231115174450496.png)



###### flex-shrink

When we use flex-basis to set the width of a flex item inside a box, if the size exceeds that of the flex box, the default flex-shrink:1 attribute of the element in the flex box will automatically calculate the optimal size of the element so that the actual size of the element is smaller than the flex-basis we gave it, and if we really want the element not to be shrunk, then we can set the flex-shrink attribute to 0, but the element will extend beyond the boundaries of the box, which is not desirable in some cases. If we really wanted to keep the element from shrinking, we could set the flex-shrink attribute to 0, but the element would extend beyond the boundaries of the box, which is undesirable in some cases.
In this example the element's flex-basis attribute is set to 200px and the box is only 400px in size, by default the flex item will be shrunk to fit the container size as shown in the following image:

![image-20231116132828892](./assets/image-20231116132828892.png)

And when we set the flex-shrink property to 0, the width of the flex item is really set to 200px wide by us manually, but it turns out that the third flex item is already outside the container at this point.



Tips: Here's a shorthand for flex: 0 0 200px; as well.


![image-20231116132609491](./assets/image-20231116132609491.png)

###### flex-grow

The flex-grow attribute determines which element size grows as much as possible or not, because by default in a flex layout, the size of an element is related to the size of the content it occupies, so if we want to change this we can use flex-grow
The following example shows the size of the element by default:

![image-20231116134756087](./assets/image-20231116134756087.png)

When we set flex-grow to 1, the size of the elements will take up as much space as possible within the container and each element will be the same size.

![image-20231116134836649](./assets/image-20231116134836649.png)


If we only set flex-grow:1 for one element and not the others, then that element will occupy as much of the container as possible, while the others will be sized by their own content, as shown below:

![image-20231116135228180](./assets/image-20231116135228180.png)



If we set the flex-grow of the rest of the elements to 1 and the flex-grow of the first element to 2, then the first element will get twice the size of the others, as shown below:

![image-20231116140114864](./assets/image-20231116140114864.png)



###### flex:

By defaults：
flex-grow:0;

flex-shrink:1;

flex-basis: auto;


When we want the size of the element to fill the box as much as possible, and change away from the default value, we can use shorthand and just set flex:1. As shown in the figure below:



![image-20231116140911080](./assets/image-20231116140911080.png)





#### 2.2.3 Grid Layout



##### Introduction:

Elements in a Grid Layout are arranged in rows and columns, and the height of an element in the same row depends on the tallest element; if the height of an element is not set, then the size of the element will be the size of its content.



![image-20231116151146962](./assets/image-20231116151146962.png)

##### Basic CSS Grid Terminology

The orientation of the row and column axis in the CSS Grid can’t be changed.

![image-20231116153513221](./assets/image-20231116153513221.png)



The number of grid lines ranges from 1 up to the number of rows and columns plus 1. Grid track can be either row or column, and grid cells are created at the beginning when the number of rows and columns is determined, and can be filled with elements or not.

![image-20231116154117797](./assets/image-20231116154117797.png)

##### Summary



Here is the summary of Grid container and grid items attributes.

![image-20231116154652450](./assets/image-20231116154652450.png)




##### Grid Container  properties



######  grid-template-columns

Creates CSS GRID columns, one column will be created for each set column size

Tips:

We can set the auto attribute to a column so that the size of the element will be exactly the size of its content, which is useful in many cases.


######  grid-template-rows

Creates rows of CSS GRID, one row will be created for each setting of the row size

Tips:

We can set the auto attribute to a row so that the size of the element will be exactly the size of its content, which is useful in many cases.

###### column-gap

Setting the gap between each column

###### row-gap

Setting the gap between each row





Here is the example to create a CSS Grid with 4 columns and 2 rows:

![image-20231116150019063](./assets/image-20231116150019063.png)





###### Aligning tracks inside container

grid-content and align-item align the items inside the grid horizontally and vertically, respectively.




First up is grid-content, It aligns all elements horizontally

![image-20231116184128438](./assets/image-20231116184128438.png)





Then there's align-content, which aligns all elements vertically

![image-20231116184342501](./assets/image-20231116184342501.png)



When both attribute values are set to center, then all elements will be in the centre of the container, as shown in the following figure:

![image-20231116184437761](./assets/image-20231116184437761.png)







###### Aligning items inside cells



justify-items and align-items will align the elements inside the grid cells.





The first is justify-items, which will align the elements horizontally in the grid cells.

![image-20231116184856148](./assets/image-20231116184856148.png)



Then there's align-items, which will make the elements vertically aligned in grid cells.


![image-20231116184943292](./assets/image-20231116184943292.png)





If the value of both properties is set to center, then all elements will be centered inside the Grid cells, as shown below:

![](./assets/image-20231116185323651.png)





If we set all the above four properties to centre at the same time, then the result will be as shown below, cool right:

![image-20231116185157244](./assets/image-20231116185157244.png)






##### Grid Item  properties



We can find the position of each element in the CSS Grid by using the CSS net in the debugging tool and move the Grid items by using grid-column grid-row.



###### grid-column&grid-row

The meaning of this code block is to move the elements in the CSS Grid of class name el--2 to the position starting from the first column, ending at the last column, and ending at the third row from the beginning of the second row, there are several knowledge points involved here:.

1. The first point of knowledge: is in the CSS network, the row and column number has a positive order and reverse order of the two expressions, when we want to quickly let an element to occupy the entire column or row, we can manually enter the positive order of the expression of the last element under the row and column number, but also directly with -1 to refer to the last element of the row and column number, because the two are essentially the same, just the size of the value and the storage order of the different only.
2. The second point is: if we want to let the element across several CSS Cell, we can either manually specify the position to be spanned to, for example, from the beginning of the 1 to the end of the 4 position, but also we can not calculate their own, but 1 span 4, to express from the beginning of the 1 back to cover 4 (including the position 1 itself)
3. The third point is that if we only want the element to occupy one grid cell, i.e., the end of the span is only the initial position plus 1, e.g., starting at 2 and ending at 3, we can either write 2/3 or there is a shorthand way of doing it, which is to just write 2.

```css
      .el--2 {
        /* grid-column: 1/4; */
        /* grid-column: 1 / span 4; */
        grid-column: 1/-1;
        /* grid-row: 2/3; */
        grid-row: 2;
      }

```


The effect is as follows:



![image-20231116170735368](./assets/image-20231116170735368.png)






##### Unit

Here we will learn a new unit: fr, its semantics is fraction, we set the unit, you can let the size of the grid item element automatically in accordance with the fraction of the proportion of the remaining space occupied by the contents of the following chart shows that there is a two-dimensional CSS Grid column scores were set to 2fr 1fr 1fr 1fr , then it will be the container of the remaining space is divided into five, in accordance with the proportion of the allocation of the grid item element. This is quit similar to flex-grow in flex layout.

![image-20231116161503274](./assets/image-20231116161503274.png)



There is also a quick write-up here for fraction with repeating units and values, as shown below:

grid-template-columns: 2fr repeat(3, 1fr);

![image-20231116162508999](./assets/image-20231116162508999.png)











































# Tips:


Here are some tips that I usually use with HTML&CSS, as well as the parts that are easy to forget.

## 1. HTML usage Tips




## 2. CSS usage Tips



1. Many times is a great idea to have the horizontal padding to be kind of double of vertical. That is a good rule of thumb that many time looks very good.

2. lorem+tab will create a bunch of fake text, which we also call blind text. 

3. Box model

   

   1. The default way of the box model of calculating width and height
      	<img src="./assets/image-20231109085617402.png" alt="image-20231109085617402" style="zoom: 50%;" />
   2. Change the default box model
      <img src="./assets/image-20231109090340554.png" alt="image-20231109090340554" style="zoom:50%;" />



   Here we specify the width of the aside class to be 300px, and set the box-sizing attribute to border-box, so at this point the size of the whole box = content plus padding =  220 + 40 + 40 = 300px

   ​	<img src="./assets/image-20231109091117484.png" alt="image-20231109091117484" style="zoom: 50%;" />

   So when we add some padding to an element, then that will subtract from the content area.

​	

4. Every single CSS developer does and uses:

   ```css
   * {
         margin: 0;
         padding: 0;
         box-sizing: border-box;
   }
   ```

   

   

5.  

   

