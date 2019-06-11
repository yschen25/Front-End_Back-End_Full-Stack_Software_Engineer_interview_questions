## CSS Interview Questions


1. Please Explain The Difference Between Visibility : Hidden And Display : None?

> - Visibility : hidden;<br/>
> –> It doesn't show up but takes space in the layout flow. (It **DOESN'T** cause DOM reflow)
<br/>

> - Display : none;<br/>
> –> It doesn't show up and removes the element from the layout flow, it allows other elements to fill in. (It **CAUSES** DOM reflow)
<br/>  

1.1 Aditional : Please Explain The Difference Between Visibility : Hidden And Opacity : 0?

> - Opacity : 0;<br/>
> -> It doesn't show up but also takes space in the layout flow.<br/>
> -> The difference is you can click on the elements behind it but you **CAN'T** click on the elements which style is visibility : hidden.

Example : https://jsfiddle.net/yschen25/289xv1ba/1/
<br/>
<br/>

2. When Should You Use Visibility and When Should You Use Display?

> - When you want the element to hold its space even when it’s not seen. => Visibility : hidden;<br/>
> - When you don't want the element to take space in the layout or You want to allowe the other elements on your page to collapse around it. => Display : none;
      
Related Reference : [Visibility vs Display in CSS](http://vanseodesign.com/css/visibility-vs-display/)
<br/>
<br/>

3. Please Explain The Difference Between Inline, Block, Inline-Block?

> - Inline<br/>
> -> It has no line break before or after it, allow other elements to sit to their left and right.<br/>
> -> Height and width properties have no effect.<br/>
> -> It can have left & right margin and padding, but not top and bottom.<br/>
> -> To make the element horizontally center is add text-align : center on it's parent element.<br/>
> -> I.g., \<a>, \<span>, \<img>  
<br/>

> - Block<br/>
> -> It starts on a new line.<br/>
> -> Height, width, margin, padding properties have effect.<br/>
> -> To make this element horizongally center is add margin : auto<br/>
> -> I.g., \<div/>, \<p>, \<h1>, \<ol>, \<ul>, \<li>
<br/>

> - Inline-Block<br/>
> -> It has no line break before or after it, allow other elements to sit to their left and right.<br/>
> -> Height, width, margin, padding properties have effect.
> -> To make this element horizongally center is add margin : auto<br/>
<br/>

4. Please Explain What Is Sprite? When Would You Use It?

> (1) sprite is a collection of images put into a single image. To display the image you can set height, width and background position.<br/>

> (2) Using image sprites will reduce the number of server requests when you have multiple images/icons.
<p align="center">
<img src="img/google.png" alt="sprite_image" title="sprite_image" width="">
</p>
<br/>

5. What Is CSS Reset? What Is The Difference Between CSS Reset And CSS Normalize?

> (1) Every browser has its own default 'user agent' stylesheet, CSS Reset is use to make it look consistent across browsers.
<br/>

> (2) CSS Reset removes all built-in browser styling, after assigning the values of margin padding and other attributes to 0. CSS Normalize keeps useful defaults rather than unstyling everything and corrects some common bugs that are out of scope for             reset.css.
<br/>

6. What Is Box Model?
<br/>

7. What Is Float?

> Float is a CSS positioning property, an element can be declared to be outside the normal flow of elements.<br/>
> There are float : left, right, none(is default), inherit(ie not suppoerted).<br/>
> I.g., By setting the 'float' property of an image to 'left', the image is moved to the left until the margin, padding or border of another block-level element is reached. The normal flow will wrap around on the right side. 
<br/>

8. How To Clear Float?

> Clear is the properity to clear the float.<br/>
> There are clear : left, right, both.<br/>
> I.g., (1)empty https://jsfiddle.net/yschen25/yc1aqhbw/6/ (2)overflow (3)after https://jsfiddle.net/yschen25/ug9m514r/2/ <br/>
Related Reference : [All About Floats](https://css-tricks.com/all-about-floats/)
