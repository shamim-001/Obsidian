#animation #css 
# code

```html
<div class="box"></div>
```

```css
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: slide; %%this is keyframe name%%
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
%%To hold use `forwards` and dont use infinite %%
}

@keyframes slide {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(200px);
    background-color: blue;
  }
  100% {
    transform: translateX(0);
  }
}

```
