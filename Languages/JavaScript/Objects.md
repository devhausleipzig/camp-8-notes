# Objects

Objects are like a dictionary; but instead of words and definitions, they are keys and values. You use a key to look up a value (the same as you use a word to look up a definition). But they can only have unique entries. You cannot have the same entry twice. Writing to the same entry will overwrite the old one.

```js
const anObject = {
	key1: 123,
	key2: "abc"
};

anObject["key1"] = 345;

console.log(anObject["key1"]); // 345
```
