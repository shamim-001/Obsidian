#doc #react 
## Component

- React components are regular JavaScript functions except:
    1. Their names always begin with a capital letter.
    2. They return JSX markup.


## Exporting and Importing components

**A file can have no more than one _default_ export, but it can have as many _named_ exports as you like.**

|Syntax|Export statement|Import statement|
|---|---|---|
|Default|`export default function Button() {}`|`import Button from './Button.js';`|
|Named|`export function Button() {}`|`import { Button } from './Button.js';`|

## Writing Markup with JSX

JSX looks like HTML, but under the hood it is transformed into plain JavaScript objects. You can’t return two objects from a function without wrapping them into an array. This explains why you also can’t return two JSX tags without wrapping them into another tag or a Fragment.

## JavaScript in JSX with Curly Braces
