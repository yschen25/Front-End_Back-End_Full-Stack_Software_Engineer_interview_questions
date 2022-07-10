# CSS Questions

### **Please Explain The Difference Between Visibility : Hidden, Display : None And Opacity : 0?**

| | Visibility : hidden | Display : none | Opacity : 0 |
|---|---|---|---|
| | Doesn't show up | Doesn't show up | Doesn't show up |   
| | Takes space | Doesn't take space| Takes space|   
| | Unclickable | Unclickable | Clickable |  
| | Doesn't cause DOM reflow | Causes DOM reflow | Doesn't cause DOM reflow |  

> - Example : https://jsfiddle.net/yschen25/289xv1ba/

<br/>

### **When Should You Use Visibility And When Should You Use Display?**

> - When you want the element to hold its space even when it’s not seen. => Visibility : hidden;<br/>
> - When you don't want the element take space or You want to allow the other elements collapse around it. => Display : none;
> - Related Reference : [Visibility vs Display in CSS](http://vanseodesign.com/css/visibility-vs-display/)

<br/>

### **Please Explain The Difference Between Inline, Block And Inline-Block Elements?**

> - Inline Elements<br/>
> -> It has no line break before or after it, allow other elements to sit to their left and right.<br/>
> -> Height and width properties have no effect.<br/>
> -> It can have left & right margin and padding, but not top and bottom.<br/>
> -> To make the element horizontally center is add text-align : center on it's parent element.<br/>
> -> I.g., \<a>, \<span>, \<img>  

> - Block Elements<br/>
> -> It starts on a new line.<br/>
> -> Height, width, margin, padding properties have effect.<br/>
> -> To make this element horizongally center is add margin : auto.<br/>
> -> I.g., \<div>, \<p>, \<h1>, \<ol>, \<ul>, \<li>.

> - Inline-Block Elements<br/>
> -> It has no line break before or after it, allow other elements to sit to their left and right.<br/>
> -> Height, width, margin, padding properties have effect.<br/>
> -> To make this element horizongally center is add margin : auto.

<br/>

### **Please Explain What Is Sprite Image?**

> - Sprite image is a collection of images put into a single image. To display the image you can set height, width and background position.

<br/>


### **When Can I Use It?**
> - Use sprite image will reduce the number of server requests when you have multiple images/icons.
<p align="center">
<img src="img/google.png" alt="sprite_image" title="sprite_image">
</p>
<br/>

### **What Does CSS Reset And CSS Normalize?**

> - Every browser has its own default 'user agent' stylesheet, CSS reset and CSS normalize is use `to make it look consistent across browsers`.

### **What Is The Difference Between CSS Reset And CSS Normalize?**
> - `CSS reset removes all built-in browser styling`, after assigning the values of margin padding and other attributes to 0. `CSS normalize keeps useful defaults` rather than unstyling everything and corrects some common bugs that are out of scope for             reset.css.
> 
<br/>

### **What Is Float?**

> - Float is a CSS positioning property, an element can be declared to be `outside the normal flow of elements`.<br/>
> - There are float : left, right, none(is default), inherit(ie not suppoerted).<br/>
> - I.g., By setting the 'float' property of an image to 'left', the image is moved to the left until the margin, padding or border of another block-level element is reached. The normal flow will wrap around on the right side. 
> 
<br/>

### **Why Should We Clear Float?**
> - If there are one large box contain two small float boxes, it will cause the big one can't extend the height.<br/> 

<br/>

### **How To Clear Float?**
> - Clear is the properity to clear the float. <br/>
> - There are clear : left, right, both. <br/>
> - Way to clear float : 
① Empty tag https://jsfiddle.net/yschen25/sandgpLx/ <br/>
② Overflow https://jsfiddle.net/yschen25/sLj6romh/ <br/>
③ CSS pseudo selector : after https://jsfiddle.net/yschen25/8mvqwgoy/ <br/>
> - Related Reference : [All About Floats](https://css-tricks.com/all-about-floats/)

<br/>

### **What Is The Difference Between Em and Rem?**

> - Em is relative to its parent's font size, rem is relative to root font size. If change the container's font size, the children with em `will be affected`, but the children with rem `will not be affected`.
<br/>

### **What Is The Position: Relative, Absolute, Fixed?**

> ① Position : relative is positioned relative to its own position. <br/>
> ② Position : absolute is positioned relative to its first positioned (not static) ancestor element. <br/>
> ③ Position : fixed is positioned relative to the browser window.
> - Example : https://jsfiddle.net/yschen25/gczL8p7k/13/

<br/>

### **What Is A Box Model?**

<p align="center">
<img src="img/box_model.png" alt="box_model" title="box_model">
</p>

> - Box model consists of : margins, borders, padding, and the actual content.<br/>
① Content : The content of the box, where text and images appear.<br/>
② Padding : Clears an area around the content, The padding is transparent.<br/>
③ Border : A border that goes around the padding and content.<br/>
④ Margin - Clears an area outside the border, The margin is transparent.

<br/>

### **What Is Box-Sizing: Content-Box And Box-Sizing: Border-Box?**

<p align="center">
<img src="img/compare_models.png" alt="compare_models" title="compare_models">
</p>

> - The actual width of box-sizing : content-box -> width + padding + border.
> - The actual width of box-sizing : border-box -> width.
> - Example : https://jsfiddle.net/yschen25/sk7xqa89/ 

<br/>

### **How To Revise The Example To Make The Appearance Of Box-Sizing : Content-Box Same As Box-Sizing : Border-Box?**
> - You can't just set the width, you need to caculate the padding, border.
> - Example : https://jsfiddle.net/yschen25/4pns9ah5/
> - Images Source : [CSS3 Box Model Behaviour](https://crypt.codemancers.com/posts/2013-11-17-box-model-behaviour/)

<br/>

### **How To Center An Element Horizontally And Vertically?**
> - See the disscussion here [How To Center An Element Horizontally And Vertically](https://stackoverflow.com/questions/19461521/how-to-center-an-element-horizontally-and-vertically).

<br/>

### **What Are New Features In CSS3?**

> - Such as gradients, transform, transition, animation, box-sizing: content-box | border-box, flexbox, etc.
> - Related Reference : [HTML5和CSS3特性一覽](https://blog.csdn.net/chandoudeyuyi/article/details/69206236).
> 
<br/>

### **Introduction The CSS Selectors.**

> - !important > Inline styles > ID Selectors > Class selectors > Element > *
> - Related Reference :  [小事之 CSS 權重](https://ithelp.ithome.com.tw/articles/10196454), [Introduction to CSS selectors](https://www.creativebloq.com/css3/introduction-css-selectors-61515320)

<br/>

### **What Is Flexbox?**

> - Related Reference :  [深入解析 CSS Flexbox](https://www.oxxostudio.tw/articles/201501/css-flexbox.html)

<br/>

### **What Is Media queries?**
- We can set the condition for the @media and write the CSS inside the block, the CSS will take effect when the condition is true, we can use media to set the different layout for different width.

<br/>

### **How would you reload a cached CSS file that has changed since it was cached?**
- Change the file name 
- Using query string

<br/>
