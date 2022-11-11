-   var
-   const
-   let

Binding is a pointer. A binding declared with 'const' cannot be re-assigned (you can't point it at a different anymore). A binding declared with 'let' can be re-assigned (you can point it at different stuff as much as you want).

Pretend 'var' is the same as 'let' for now.

```js
let a = 5;
a = 12; // allowed
a = "three"; // allowed

const b = "hello";
b = "bye"; // not allowed
```