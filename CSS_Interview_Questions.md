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
<br/>     

2. When Should You Use Visibility and When Should You Use Display?

> - When you want the element to hold its space even when it’s not seen. -> Visibility : hidden;<br/>
> - When you want the element to give back its space allowing the other elements on your page to collapse around it. -> Display : none;
      
Related Reference : [Visibility vs Display in CSS](http://vanseodesign.com/css/visibility-vs-display/)
<br/>  

3. Please Explain The Difference Between Inline, Block, Inline-Block?

> - Inline<br/>
> -> It has no line break before or after it.<br/>
> -> Height and width properties have no effect.<br/>
> -> It can have left & right margin and padding, but not top & bottom.
<br/>

> - Block<br/>
> -> It starts on a new line.<br/>
> -> Height, width, margin, padding properties have effect.
<br/>

> - Inline-Block<br/>
> -> It has no line break before or after it.<br/>
> -> Height, width, margin, padding properties have effect.
> - Opacity : 0;<br/>
