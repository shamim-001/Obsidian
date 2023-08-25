#position 
CSS position property is used to control the positioning of elements on a web page. It specifies how an element is positioned within its parent container. The `position` property can take several values:

1. `static` (default): This is the default positioning value, where the element follows the normal flow of the document. It is not affected by the `top`, `bottom`, `left`, `right`, or `z-index` properties.
    
2. `relative`: The element is positioned relative to its normal position in the document flow. It can be moved using the `top`, `bottom`, `left`, and `right` properties. ==Other elements on the page will not be affected by the relative positioning of this element.==
    
3. `absolute`: The element is positioned relative to its nearest positioned ancestor (an ancestor element with a position value other than `static`), or the initial containing block if there is no positioned ancestor. It is taken out of the normal flow, and other elements will ignore it when calculating their positions.
    
4. `fixed`: The element is positioned relative to the viewport (the browser window), even if the page is scrolled. It is also taken out of the normal flow and does not affect the position of other elements.
    
5. `sticky`: The element is positioned based on the user's scroll position. It is similar to `relative` positioning when the element is inside the viewport, but it becomes `fixed` when the user scrolls beyond a specified threshold.
    

The positioning properties (`top`, `bottom`, `left`, `right`) are used to adjust the position of an element when its `position` property is set to `relative`, `absolute`, or `fixed`.