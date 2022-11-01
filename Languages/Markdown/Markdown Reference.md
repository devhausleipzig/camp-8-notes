
- [x] Paragraph
- [x] Heading
- [x] Lists
- [x] Emphasis
	- [x] Bold
	- [x] Italic
	- [x] Color
	- [x] Strikethrough
	- [x] Blockquote
- [x] Code Block
- [x] Images
- [x] Links
- [x] Tables
- [x] Caption
- [x] Subscript / Superscript
- [x] Footnotes



## Structure

### Paragraphs

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean commodo, nulla eu viverra porta, nulla magna eleifend neque, et laoreet magna lorem ut mauris. Aenean scelerisque purus sit amet pellentesque mattis. Donec malesuada id lorem eu viverra. Nullam est odio, luctus vel mauris ut, faucibus ornare metus. Fusce auctor nisi nec aliquet commodo. Aenean sed sem eu ligula porttitor semper. Phasellus auctor luctus mi id ullamcorper. Nam pellentesque, diam at laoreet convallis, mauris justo lacinia neque, viverra placerat nisi velit ac neque. Quisque ut mi sagittis, molestie velit nec, dapibus tellus. Phasellus nisi leo, posuere sodales tortor at, tincidunt tincidunt velit. Fusce vulputate rhoncus lacus, vitae ornare purus feugiat ac.

###  Headings

#### Common Syntax

```
# Level 1
## Level 2
### Level 3
#### Level 4
##### Level 5
###### Level 6
```

```js
var x = 2
```

#### Alternative Syntax

```
Header
====
```

### Lists

#### Unordered Lists

```
- List item 1
- List item 2
```

##### Result:
- List item 1
- List item 2

---

```
+ List item 1
+ List item 2
```

##### Result:
+ List item 1
+ List item 2

---

```
* List item 1
* List item 2
```

##### Result:
* List item 1
* List item 2

#### Ordered Lists

```
1. Item 1
2. Item 2
3. Item 3
```

##### Result:
1. Item 1
2. Item 2
3. Item 3

## Emphasis

### Bold

```
This is the __word__ I wanna put emphasis on.
This is the **word** I wanna put emphasis on.
```


#### Result:
This is the __word__ I wanna put emphasis on.
This is the **word** I wanna put emphasis on.


### Italilic

```
Put some _emphasis_ on me.
Put some *emphasis* on me.
```

#### Result:
Put some _emphasis_ on me.
Put some *emphasis* on me.

### Marker

```
Put some ==emphasis on== me.
```

#### Result:
Put some ==emphasis on== me. Continues ==here==

### Strikethrough

```
We use ~~JavaScript~~ TypeScript for writing interactive web applications
```

#### Result:
We use ~~JavaScript~~ TypeScript for writing interactive web applications

### Blockquotes

```
> This is an awesome quote

> This is a 
> multiline quote
```

#### Result:
> This is an awesome quote

> This is a 
> multiline quote

## Code Blocks

### Inline Code

```
To get the application running we need to type `yarn dev` in the terminal
```

#### Result:
To get the application running we need to type `yarn dev` in the terminal

### Fenced Code Block

````
```javascript
function add(x, y) {
	return x + y 
}

console.log(add(1,2))
```
````

#### Result:
```javascript
function add(x, y) {
	return x + y 
}

console.log(add(1,2))
```

```js
var x = 0
```

## External Resources

### Links

```
[Google](http://google.com)
```

#### Result:
[Google](http://google.com)

### Images

```
![Flowers](https://images.unsplash.com/photo-1666110784741-e653219aacf1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1036&q=80)

![](../images/rectangle.png)
```

#### Result:

![Flowers](https://images.unsplash.com/photo-1666110784741-e653219aacf1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1036&q=80)

![](../images/rectangle.png)

## Tables

```md
| ID  | Name    | Quantity | Price |
| --- | ------- | -------- | ----- |
| 1   | MacBook | 24       | 1500  |
| 2   | iPad    | 10       | 950   |
| 3   | iPhone  | 15       | 1400  |

```

Left Align `:--`
Right Align `--:`
Center Align `:-:`

### Result:

| ID  | Name    | Quantity | Price |
| :-: | :------ | :------: | ----: |
| 1   | MacBook | 24       | 1500  |
| 2   | iPad    | 10       | 950   |
| 3   | iPhone  | 15       | 1400  |

## Caption

| ![Recangle](../images/rectangle.png) |
| --: |
| Caption | 

## Sub- / Superscript

```
$v_{min}$
$1^{e-1}$
```

### Result:

$v_{min}$
$1^{e-1}$

## Footnotes

```
Markdown[^1] is pretty cool to quickly write documentation

[^1]: https://daringfireball.net/projects/markdown/syntax

```

### Result:

Markdown[^1] is pretty cool to quickly write documentation


[^1]: https://daringfireball.net/projects/markdown/syntax

## References

```
[Github][github]

[github]: https://github.com/
```

When we use references we need to use square brackets `[]`.
So don't do this `[Github](github)`, do that `[Github][github]`

### Result:

[Github][github]

[github]: https://github.com/

l First Header | Second Header |
| ------------- | ----------------- |
l Content from cell 1 | Content from cell 2 |
| Content in the first column | Content in the second column |







