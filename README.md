# nnhtml-css-course
# TUTORIAL 6 - Semantic Tags:

*used to let the browser of what exactly our code is written for.

eg:

 ```
<div>
<p>armaan</p>
</div>
```

Here the browser doesn't what the lines inside the ```<p>``` tags are meant for.

The types of semantic tags are:

* ```<main>``` tag - It is used to include the main content of the webpage.
* ```<section>``` tag - Used to define a specific section of the webpage.
	eg: contacts , address  etc and other specific sections.
* ```<article>``` tag: Used to define an article like content.
* ```<aside>``` tag : Used to distinguish something inside the article , which is not exactly part of the article.
* ```<header>``` tag: Header of the page .
	eg: title , heading etc.
* ```<footer>``` - Used to have footer type information. 
	eg: contact info , copyright info etc.
* ```<nav>``` tag (07:08) : Used for naviagation purposes inside the page .

imp (10:06) - A list of images can be shown by placing them in an ```<li>``` tag , inside an ```<ul>``` tag. 

imp (12:46) - We dont always need to use the submit button.You just need to click enter after submitting every info.


# TUTORIAL 7 - Chrome Developer Tools:


* The "inspect" option provides an overview of all the code used in the webpage.

Uses:

* Copying codes from the elements window to make adjustments in css
* (01:38) - Using as HTML.This can be done by right clicking the code in the elements window to be edited and click on "Edit as HTML".
* (02:15) - Using "scroll intp view" bu right clicking on the code element. This will take you to the body of the webpage related to the code.
* (2:30) - "Hide" or "delete" elements by right clicking them.
* (2:44) - "Edit" or "add" attribute options .
* (3:55) - CSS styling can also be done. This can be done by either editting the code in the "elements.code" tab
imp (04:23) - When a code/property is overwritten , the property appears striked off.
imp (04:47) - We can uncheck different properties to find out the error/reason for not getting the appropriate result.
* The "sources" tab lets you see the files used in the project. You can also edit your code by double clicking those files.
	eg: the html file , the css file etc
imp (07:30) - After editing the page , do not refresh the page until all your edits have been saved to your code in the editor.
      You can make the saves permanent by going to the files system and adding the folder to the workspace.
* The device preview button can show you how exactly the web page you are working on will be displayed on different devices.


# TUTORIAL 8 - Positioning and Layout:

Types of elements based on position:

* Static - The element is static and no property of positioning applies to it
* Relative - This allows the element to be shifted with respect to the original position of the element.
	eg: 20px right , 20 px left 
```
header {
	position : relative;
	margin - left: 200px;
}
```
imp = Using margins here means that the element is being shifted that many pixels away from wherever mentioned.
	eg: ```margin - left: 100px;``` is such that the element is being shifted 100px away from the top

It can move anything you want relative to the position of the parent element.

* Fixed: Keeps an element as fixed.
	eg: 0 px to the top , 0px to the left makes an element stay fixed even when we scroll the page down and up. It does not move
* Absolute: Lets you position a child elememnt with respect to the position of a parent element which also has been given a property.


*To Adjust the resolution of an image:

eg:

```
.banner img {
	max-width:100%          
}
```
The "img" is used here because the image is inside the class "banner" and inside the ```img``` tag.
The property max-width lets you adjust the resolution.
* When you move an element keeping it position relative , the space it was originally in is retained. But when you use absolute 
positioning with its parent moved relatively , then we see that the element does not retain its originl position.

imp => Using o=positon properties like left , top etc will postion the element that many pixels from the left or top . 
It is not similar to 
as using left or top margin positioning.

Here instead of using pixels , we use % as we do not want the welcome element to actually change its size as we change the siz of 
the banner. 

 
VERY IMPORTANT: 
In orde to reach a tag within a class , just call that tag withhin a the class.
	eg:
	
	```
	.banner h2 span {
	font-size: 100px;
	}
	```
	
Also, you can use the pixellation value "em" instead of pixels. 
This is used when you can inherit a paremt pixel value . Here , 1.3 em = 1.3  * the parent pixel value.



* Using Fixed positioning is such that the elemnt will remain fixed even when the whole page is scrolled up or down.
 Here  , we use the padding ( 6px , 12px) in such a way that the 6px denotes the top and bottom padding while the 12px denotes the
bottom padding. 
After using fixed positioning , we can see that the element is fixed inside the image  "banner.png". So in order to bring it out to visibility, 
we use the property ```z-index```. It is used as ```z-index: 1``` here.
As for the h1 tag element "Mario" , we use different properties to align them property.We also use the inline-block display to make
them be displayed  as a block but inline.
(* Using ```header``` tag will let you use the entire area.)

Here we also use the property ```border-radius``` to make a curved like edge to the border. Increasing the pixels will increase 
the curve.

* ```white-space: nowrap``` is simply a property that means that all the elements of the parent element must come in a straight line .
* ```width: 25%``` means the same as the usual width except it is in % rather than in pixels.
* ```margin: 0 auto``` means that the browser will automatically adjust the margin from the left and right.
* ```max-width: 1200px``` is also same as width.
Hence ```max-width``` , ```margin: 0 auto``` , etc are nice ways to centralise an element.
* ```position: sticky``` is used to make the element fix at after it reaches a particuular distance in pixels from whatever side mentioned.

	eg:
```
	position: sticky;
	top: 100px;
```
Here , the scrolling will stop as the element will reach 100 pixels from the top.
* In order to apply propertiies to the entire body and the tags which are in the body , we can use the tags in a single line likee this.

```
	body,h1,h2,ul,li,a {
    	margin: 0;
    	padding: 0;
    	font-family: Arial;
	}
```
* When we reduce the resolutuion % (to mobile devices) of the entire page , we see that some of the elements change their alignment , width etc. 
This is due to the presence of the padding which adds up to the total width of the element, So in order
to adjust them , we use the use ```box - sizing: border-box``` code. It means it basically it will incorporate the padding along with 
the width so that the alignemnt of the page doesnt change when you change the resolution.

##(32:50) - Aligning and resizing images in ```li``` tags - 
They do not appear as inline block even after appliying the display property of inine-block on them## - Need to clarify


* To provide attributes to elements inside a form tag , you dont exactly need to use a div or a class , you can use the form 
and input like this:
	eg:
	
	
```
		form input {
    margin: 20px , 0;
    padding: 10px , 45px;
    font-size: 23px;
    border-radius: 34px;
    border: 4px rgb(255, 254, 254) solid;
}
```

# TUTORIAL 9 - Pseudo Classes and Elements:


Pseudo classes are attributes that show extra properties to the to the elements. These extra properties can be displayed
by using pseudo classes.
Pseudo classes are denoted by a ":".

The different pseudo classes are:

* Hover:

It is used to display a property when you hover over the element.
It can be used by the following format.
eg:

```
nav li a:hover{
    text-decoration: underline;
    background-color: yellow;
    padding: 5px;
}
```

* Focus:

 It is used to show that an element is currently in focus. eg: When we click on an input tag like email so as enter an id , it 
 is in focus.

eg:

```
form input:focus {
border: 5px grey dotted;
outline:none;
}
```
Here , the outline property is used to remove the outline from the email input tab.

* Valid:

It is used to show if an element (data inputted) is valid or not.
It is mainly used in the case of input tags ie to display something if the entered data is valid.

eg:

```
form input:valid {
    border: 5px solid green;
}
```
* First - Child:

It is used to target the first element on a list.  

eg:

```
nav li:first-child {
    border: 3px solid red; 
} 
```

// check w3 schools for many pseudo classes.

*Pseudo Elements: (check w3 schools for different pseudo elements as well)

Pesudo elements allow us to add a dynamic property to an element. We can also insert a content or target a specific content inside 
a tag.

Pseudo elements are denoted by "::".

Soome of the different pseudo elements are:

* first-line : It targets the first line of an element or paragraph or whatever is in a tag.

eg:

```
article p::first-line {
    font-weight: bold;
    font-size: 1.2em;
}
```

*first-letter : It targets the first letter of an element or a line in a tag.

eg:

```
section p::first-letter {
    font-weight: bold;
}
```

* selection:

It targets the selected portion of an element. This is used to display a propert defined when you select a portion in the page.

eg:

```
p::selection {
    background-color: rgb(235, 57, 57);
    color: white;
}
```
* ::after and ::before elements:

They are used to add anything after or before a specific portion of the page.

eg:
```
p::after {
    content: "Yes!!";
    font-size: 6px;
}
```

Here , the ```content: "..."``` is a property used to add anything , after or before an element or a line.

# TUTORIAL 10: Media Queries:

Media queries are fucntions uses to make the tags and elements responsive.

The syntax of media query used it:

```
@media screen and (min-width:400px) {

    nav ul {
        display: flex;
        justify-content: space-between;
    }
    nav ul li {
        flex:1;  /* flex: grow , shrink , basis*/
    }
} 
```


# CSS FLEXBOX:


# TUTORIAL 1:

* Flexbox are display types used to make css aligning and display properties a lot easier.
Its used to control the size , position , spacing od elememnts etc.

* For applying flex , we need to assign a container (flex container) and a list of divs or other tags inside the parent divs called
children or flex items.

They are very responsive as well.

# TUTORIAL 2 - Flex Containers:

* The flex properties are applied relative to the parent flex container , through which the properties will be applied to the flex items
as well.

* The flex property can be applied to the parent by providing a display tag of flex in this manner:

```
.container{
display : flex;
}

.box {
    height: 100px;
    min-width: 100px;
}
```

Thus all the elements inside the div will have the flex property. It will display the  minimum width of the elements.
(In case of the example we did , the three flex elements will be displayed in a row each with the specified minimum width of 100px)

# TUTORIAL 3 - Flex Grow:

* We can control the flexibility of the flex elements by applying the property ```flex:grow``` to the flex items inside the flex container.

eg:

```
.flex-box {
    display :flex;
}
.box {
    height: 100px;
    min-width: 100px;	
    /*flex-grow: 3;*/	
} 
.one {
    background-color: red;
    flex-grow: 1;
}
.two {
    background-color: #0400ff;
    flex-grow: 2;
}
.three {
    background-color: #3cff00;
    flex-grow: 3;
}
```
Here , the ```flex-grow``` property is applied to each flex element with different values and the flex element is grown by the rates 
specified .
We can either do it this way , or we could use the flex grow commonly for all items to grow the elements with the same rate.

eg:

```
.flex-box {
    display :flex;
}
.box {
    height: 100px;
    min-width: 100px;	
    /*flex-grow: 3;*/	
} 
```

# TUTORIAL 4 -Flex Shrink:

* ```Flex: Shrink``` is used to shrink the flex element which has already been applied the display:flex property.
The elements shrink when the browser display area is reduced and they shrink at a rate specified by the user.

eg:

```
.flex-box {
    display :flex;
}
.box {
    height: 100px;
    width: 320px;
} 
.one {
    background-color: red;
    flex-shrink: 1;
}
.two {
    background-color: #0400ff;
    flex-shrink: 7;
}
.three {
    background-color: #3cff00;
    flex-shrink: 3;
}
```


# TUTORIAL 5 -Flex Wrap:

* When you reduce the size of the page and it reaches a situation such that the flex element has reached the min width specified and cannot 
shrink any further ,and then the scroll bars appear at the bottom of the page so as to see the rest of the element.
Hence we use ```flex-warp: wrap``` or ```flex-wrap: wrap-reverse``` for reverse wrapping.

eg:

```
.flex-box {
    display :flex;
    min-width: 200px;
    flex-grow: 1;
    flex-wrap: wrap-reverse;
}
.box {
    height: 100px; 
    width: 320px;
} 
.one {
    background-color: red;
}
.two {
    background-color: #0400ff;
}
.three {
    background-color: #3cff00;
}
```
Here , all the properties are applied to the parent "flex-box"

# TUTORIAL 6 -Flex Basis:

* ```flex:basis``` is pretty similar to ```min-width``` as it defines the starting width of the flex element.

eg:

```
.flex-box {
    display :flex;
    min-width: 200px;
    flex-grow: 1;
    flex-wrap: wrap;
}
.box {
    height: 100px; 
    width: 320px;
} 
.one {
    background-color: red;
    flex-basis: 100px;	
}
.two {
    background-color: #0400ff;
    flex-basis: 100px;	
}
.three {
    background-color: #3cff00;
    flex-basis: 200px;	
}
```

Hence we can see that the flex-basis with the largest pixels will appear with larger width as a flex element.

Here , we can write all  3 properties , ie ```flex: grow``` , ```flex: shrink``` and ```flex-basis``` as a single flex element.

eg:

```
.box {
    height: 100px; 
    flex-grow: 1;
    flex: 1 1 300px;
} 
```
# TUTORIAL 7 -Flex Menu:


* Here in the files "flexbox7.html" and "flexbox7.css" , we made the ```ul``` tag as the flex container , applied properties 
to its ```li``` elements ie ```a``` elements. 
All these ul and li elements are defined inside a nav

After designing these , we used a media query function to create a responsive menu.

eg:
```
@media screen and (min-width:400px) {

    nav ul {
        display: flex;
        justify-content: space-between;
    }
    nav ul li {
        flex:1;  /* flex: grow , shrink , basis*/
    }
} 
```
Here ,the ```justify-content``` property is used to align the flex elements in different ways based on it different properties.

Some of the properties of ```justify-content``` are:

	```
	justify-content: space-around;
        justify-content: flex-end;
        justify-content: flex-start;
        justify-content: center;
        justify-content: space-between;
	```
# TUTORIAL 10: Media queries:

* Tell the browser how to style an element at particular viewport dimensions.

* viewport meta tag - tells the browser what width the viewport should be
* meta tag - <meta name="viewport" content="width=device-width, initial-scale=1.0">

Syntax:

```
@media screen (max-width:960px) {}

@media screen (min-width:960px) {}
```

# CSS POSITIONING:

# Box Model:

* The box model in CSS is represted as an element , surrounded by padding and then it is surrounded by the margin.
  The margin is further surrrounded by the border of the element.

* This is a box model and only block elements can be represnted in this way and not inline elements.

* The  p tag element is a block element by default and that is why multiple p tags are shown per line and not in a single line.
  a tag ie href is an inline element and the box model cannot be represnted in its case.
  Hence we can apply box model properties to the p tag elements and not the a tag elements.

* Block type elememts take up 100% width of the page by default. Whereas inline elements just take up their surroiunding area.
  In which case if you , use ```width: 50%``` , then 50% of the total 100% width will be displayed.
  If you add a margin property like ```margin: 50px``` , then it will be applied to the block element and not the line type element.
  Hence an ```a```  tag element below a ```p``` tag element will display as if it is oveerlaped to the p type element if you add these 
  properties to it. However , if you change the display of the inline ```a``` tag element to block or inline block , then there proprties
  will be applied to it.

# Normal Documentation Flow: 

*  The block type elements occur on top of one another ie from top to bottom while the inline elements occur in the same line  , ie 
   from left to right.
*  ```line-height: 20px``` means it will modidfy the gap between different lines in a paraghraph element.

# Floating Elements:

* ```margin: 0 auto``` means "margin left and right auto". It is used to position elements to the middle of the screen.
* Using ```width:95%``` is almost equivalent to using ```width: 960px```. This is how you use  % to size elements in case of block elements.

* Image elements can be given width too.
* In normal documentation flow , the element specified below a block element comes below it . However , if we want to align the elements 
  in the same line , then we can use the float property.
  
  eg:
	```img {
    width:300px;
    float: left;
    }	
	```

  Using this propert will align the top element to the left of the element below it.
  The same thing can be done by using ```float: right```.
   
  In case of the exmple done with 4 colors (flotingelements html and css) , we see that if we use float left on a color , it will hide 
  in to the left of the second color. (if you add a margin property to the second color , you can see the first color hiding beside it).
  However , if you provide a ```float: right``` propert , then the color will be in the right. If we provide th same ``float:right``` 
  property to the next color , it will also be aligned to the right of the element , not from top to bottom , but from left to right , 
  ie in the same line.  

# Clear Floats:

* The ```clear:left``` 

  or 

  ```clear: right``` 

  or 

  ```clear: both```

  , are used to clear the elements from the applied float propetiers. However , using this property will not completely let the 
  float propertis be cleared and be converted back to the normal document flow.
  If we use properties on a block element just below the floated element (the new block element is inside the main div as the 
  float elements) , then the properties like margin etc wont work on it , as the floating properties are also applicable to them.
  Hence to solve this , we use an empty div to seperate the floating element with the block element.

  This can be done by using a div to seperate them :

 
 ```
.service {
    float: left;
    background-color: cornflowerblue;
    margin: 2%;
    width: 25;
    padding: 5px;
    height: 140px;
    clear: both;
}
```
```
.services:after {
    content: "yoyoyo";
    display: block;
    clear:both;
}
```

 * The after pseudo class is used to enter an element after a certain tag.

# Column Floats:

It can be used to align the div elements as columns . 

In case of of divs consisting of p types or other types of tags and we want to alignt them as columns , we can use the ```float```
property to align them as floast and break the normal documentation flow.

However , if we are defining block elements , we need to provide them seperate widths for the flaot properties to kick in coz 
otherwise the block elements have default width of 100% and applying float property won't make any difference.
Hence , to display the elements as columns in the same screen , we need to provide seperate widths for them elements.

After aligning them as float elements , we need to clear the floats so that the elements that way be defined below the columns will
not inherit the float properties. This can be done by defining these elements inside a single parent div and adding any element after
the div so as to seperte it from new elements to be added.

```
.columns {
content : "";
display: block;
clear: both;
}
```

# Text Columns without using float:

This can be done using a the following properties.

*
```
content {
-webkit-column-count: 4;
	column-count: 4;
}
```
This property is used to input the number of columns you want toi divide the texts into.

*
```
content {
 -webkit-column-gap: 20px;
    column-gap: 20px;
}
```

It can be used to specify the gap between the columns

*
```content {
   -webkit-column-rule: 2px solid black;
    column-rule: 2px solid #8d8dd6;
}
```

It is used to add a line between the columns and to give it a size , type and color.

# Position Relative:

Position relative is used to visually move the element and not in reality. In reality the element is still in the normal document flow as 
seen by the browser. Hence we should use this property only if we need to like really bad.

# Position Absolute:

```max-height```
```overflow:hidden``` 

The overflow property is used to make the overflow of the elements hidden.

* The relative absolute property is used to move an element absooutely relative to the postion of its parent element.
ie , we need to applty a relative property to the parent element first and then the element to be moved is applied an absolute 
property.

```
.wrapper {
    position: relative;
}
.service {
    position: absolute;
    left: 350px;
}
```
# Position fixed: 


It is used to fix an element and never move it. It is in such a way that the element is fixed relative to the browser window.
Remember that while we use fixed positioning , the element is taken out of the normal document flow and hence the initial space occupied
by the element will be gone , unlike relative.

eg:

```
ul {
float: left;
position: fixed;
top:50px;
background-color: blue;
align-content: center;
width: 100%;
margin: auto 0;
}
```
# z-index:

* Thew further down you are , then higher the stacking order and vice versa.

* By default , the z-index of the elements is zero. So in order to increase the stacking order , we need to increase their z-index
  to 1. 
* In order for the z-index property to work , we need to provide a relative positioning property to the element. 
  Suppose , we give the first element z-index 1 for a fixed element , it has more stacking order than all the other elements and 
  none of them will overlap this element when we scroll down.
  Suppose , we give z-index - 2 for another element , then when we scroll down , the element with z-index=2 will overlap the first
  element with z-index:1 and the rest of the elements will not. This is the use of z-index.\
  eg:

  ```
  section , aside {
    position: relative;
    float: left;
    width: 40%;
    padding: 2%;
    margin:2%;
    background-color: greenyellow;
    z-index:1;
}
	```

# Clipping Content:

* Using max-height to a div or a tag in which an element placed in another div is placed  will provide a value to it will fix the maximum 
  height an element can have. If the element is overlapping the parent div , then we can use the ```overflow``` property to it and the 
  element will be completely inside the parent div.

  If we use ```overflow: auto``` , then the area the element was overflowing with will be placed inside the the parent container with a
  scroll bar.
  Or use the ```overflow: hidden``` to completely the hide the overflowing area from the parent div.












