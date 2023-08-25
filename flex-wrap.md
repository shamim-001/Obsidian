#flex-wrap
1. `nowrap` (default): This value prevents the flex items from wrapping onto multiple lines. The items will all be forced to fit within a single line, even if it causes overflow or resizing of the flex container.
2. `wrap`: This value allows flex items to wrap onto multiple lines if needed. If the items exceed the available width of the flex container, they will wrap onto a new line.
3. `wrap-reverse`: This value behaves similarly to `wrap`, but the wrapping starts from the opposite direction. The wrapping occurs from the bottom to the top or from the right to the left, depending on the flex container's flex direction.
```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```
