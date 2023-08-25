#css #psudo 
1. ==`:hover`:== Selects an element when the mouse pointer is over it.
2. ==`:active`:== Selects an element when it is being clicked or activated.
3. ==`:focus`:== Selects an element when it is currently in focus (such as when an input field is selected).
4. ==`:first-child`:== Selects the first child element of its parent.
5. ==`:last-child`:== Selects the last child element of its parent.
6. ==`:nth-child(n)`:== Selects elements that match a specific position within their parent. You can specify a formula using `n` to target elements at specific positions (e.g., `:nth-child(2n)` selects every even child element).
7. ==`:nth-of-type(n)`:== Selects elements of a specific type that match a specific position within their parent. It works similarly to `:nth-child()`, but it only considers elements of the same type.
8. ==`:not(selector)`:== Selects elements that do not match the specified selector.
9. ==`:before`== and ==`:after`:== Inserts content before or after the selected element, respectively. These pseudo-selectors are often used in combination with the `content` property to add decorative elements or text.
10. ==`:empty`:== Selects elements that have no children or text content.