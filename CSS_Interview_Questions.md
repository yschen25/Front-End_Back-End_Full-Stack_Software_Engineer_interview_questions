## CSS Interview Questions


1. Please Explain The Difference Between Visibility : Hidden And Display : None?

> - Visibility : hidden;<br/>
> –> It doesn't show up but takes space in the layout flow. (It **DOESN'T** cause DOM reflow)
<br/>

> - Display : none;<br/>
> –> It doesn't show up but removes the element from the layout flow and allow other elements to fill in. (It **CAUSE** DOM reflow)
<br/>  

1.1 Aditional : Please Explain The Difference Between Visibility : Hidden And Opacity : 0?

> - Opacity : 0;<br/>
> -> It doesn't show up but also takes space in the layout flow.<br/>
> -> The difference is you can click on the elements behind it but you **CAN'T** click on the elements which style is visibility : hidden.

Example : https://jsfiddle.net/yschen25/289xv1ba/1/
<br/>
<br/>

2. When Should You Use Visibility and When Should You Use Display?

> - When you want the element to hold its space even when it’s not seen. -> Visibility : hidden;<br/>
> - When you want the element to give back its space allowing the other elements on your page to collapse around it. -> Display : none;
      
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
<br/>
<br/>

4. Please Explain What Is Sprite? When Would You Use It?

> (1) sprite is a technique to combine all/ some of them in one image. To display the img you set height, width and background position.<br/>
> (2)When you have multiple images/ icons, browser makes separate call to the server for each one of them. sprite is a technique.
