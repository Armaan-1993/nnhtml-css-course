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


TUTORIAL 8 - Positioning and Layout:

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
