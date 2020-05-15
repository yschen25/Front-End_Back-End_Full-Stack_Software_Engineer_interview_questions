## CSS Questions
<br/>

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

Example : https://jsfiddle.net/yschen25/289xv1ba/
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
> -> To make this element horizongally center is add margin : auto.<br/>
> -> I.g., \<div/>, \<p>, \<h1>, \<ol>, \<ul>, \<li>.
<br/>

> - Inline-Block<br/>
> -> It has no line break before or after it, allow other elements to sit to their left and right.<br/>
> -> Height, width, margin, padding properties have effect.
> -> To make this element horizongally center is add margin : auto.<br/>
<br/>

4. Please Explain What Is Sprite? When Would You Use It?

> (1) sprite is a collection of images put into a single image. To display the image you can set height, width and background position.<br/>

> (2) Using image sprites will reduce the number of server requests when you have multiple images/icons.
<p align="center">
<img src="img/google.png" alt="sprite_image" title="sprite_image">
</p>
<br/>

5. What Is CSS Reset? What Is The Difference Between CSS Reset And CSS Normalize?

> (1) Every browser has its own default 'user agent' stylesheet, CSS Reset is use to make it look consistent across browsers.
<br/>

> (2) CSS Reset removes all built-in browser styling, after assigning the values of margin padding and other attributes to 0. CSS Normalize keeps useful defaults rather than unstyling everything and corrects some common bugs that are out of scope for             reset.css.
<br/>

6. What Is Float?

> - Float is a CSS positioning property, an element can be declared to be outside the normal flow of elements.<br/>
> - There are float : left, right, none(is default), inherit(ie not suppoerted).<br/>
> - I.g., By setting the 'float' property of an image to 'left', the image is moved to the left until the margin, padding or border of another block-level element is reached. The normal flow will wrap around on the right side. 
<br/>

7. How To Clear Float?

> - Clear is the properity to clear the float.<br/>
> - There are clear : left, right, both.<br/>
> - I.g., If there are one large box contain two small float boxes, it will cause the big one can't extend the height, there are many ways to solve the problems.<br/> 
① Empty tag https://jsfiddle.net/yschen25/sandgpLx/ <br/>
② Overflow https://jsfiddle.net/yschen25/sLj6romh/ <br/>
③ CSS pseudo selector : after https://jsfiddle.net/yschen25/8mvqwgoy/ <br/>

Related Reference : [All About Floats](https://css-tricks.com/all-about-floats/)
<br/><br/>

8. What Is The Difference Between Em and Rem?

> - Em is relative to its parent's font size, rem is relative to root font size. If change the container's font size, the children with em **WILL BE AFFECTED**, but the using rem **WILL NOT**.
<br/>

9. What Is The Position : Relative, Absolute, Fixed? <br/>

> ① Position : relative is positioned relative to its normal position. <br/>
> ② Position : absolute is positioned relative to its first positioned (not static) ancestor element. <br/>
> ③ Position : fixed is positioned relative to the browser window.

Example : https://jsfiddle.net/yschen25/gczL8p7k/13/
<br/>

10. What Is Box Model?

<p align="center">
<img src="img/boxModel.png" alt="box_model" title="box_model">
</p>

> - Box model consists of : margins, borders, padding, and the actual content.<br/>
① Content : The content of the box, where text and images appear.<br/>
② Padding : Clears an area around the content, The padding is transparent.<br/>
③ Border : A border that goes around the padding and content.<br/>
④ Margin - Clears an area outside the border, The margin is transparent.
<br/><br/>

11. What Is Box-Sizing : Content-Box And Box-Sizing : Border-Box?

<p align="center">
<img src="img/compareModels.png" alt="compare_models" title="compare_models">
</p>

> - The width of box-sizing : border-box including content, padding, border, but the width of box-sizing : content-box just including content, you just set the width and height of the content area.<br/>

Example : https://jsfiddle.net/yschen25/sk7xqa89/ <br/><br/>

11.1 Aditional : How To Revise The Example To Make The Apperence Of Box-Sizing : Content-Box Same As Box-Sizing : Border-Box?<br/>

> - You can't just set the width, you need to caculate the padding, border.<br/>

Example : https://jsfiddle.net/yschen25/4pns9ah5/ <br/>

Images Source : [CSS3 Box Model Behaviour](https://crypt.codemancers.com/posts/2013-11-17-box-model-behaviour/)
<br/><br/>

12. How To Center An Element Horizontally And Vertically? <br/>

> - See the disscussion here [How To Center An Element Horizontally And Vertically](https://stackoverflow.com/questions/19461521/how-to-center-an-element-horizontally-and-vertically).
</br>

13. What is New Features In CSS3?

> - Please see [HTML5和CSS3特性一覽](https://blog.csdn.net/chandoudeyuyi/article/details/69206236).
</br>

14. Introduction The CSS Selectors

!important > Inline styles > ID Selectors > Class selectors > Element

> - Please see [Introduction to CSS selectors](https://www.creativebloq.com/css3/introduction-css-selectors-61515320)