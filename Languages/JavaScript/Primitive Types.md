-   string

Using double quote or single quote is basically equivalent. Using backticks allows you to do something special.

```js
"this is a string";
"this is also a string"`this is a string too`;
```

-   number

```js
0;
30;
99999999;
10.97349823 - 1000;
```

-   NaN
    This is a special value that is returned by math operators/functions when you try to do something invalid (like subtract strings, or divide by zero, etc...)
    > [!info]
    > NaN is also of type number

-   boolean
    Either `true` or `false`

```js
true;
false;
```

-   undefined
    This is an empty value. It means nothing is there. You only get this value when something is "unintentionally" empty.

```js
undefined;
```

-   null
    This is an empty value. It means nothing is there. This is usually a sign that "empty" is intentionally a valid state.

```js
null;
```

-   coercion (typecasting)
    Don't think about too much yet.