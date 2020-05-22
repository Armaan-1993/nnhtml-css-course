# nnhtml-css-course
#TUTORIAL 6 - Semantic Tags:

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


#TUTORIAL 7 - Chrome Developer Tools:


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


#TUTORIAL 8 - Positioning and Layout:

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
