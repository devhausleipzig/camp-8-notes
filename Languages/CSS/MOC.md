## What is CSS?

CSS - Cascading Style Sheets is Domain specific language (Browser) that provides styling to the structure (markup) we defined in [[Languages/HTML/MOC|HTML]]

## How to use CSS

There are three ways to apply CSS to our markup. They are ordered by specifity (highest at the bottom).

### External Stylesheet

[[Link]]
```html
<head>
	<link rel="stylesheet" href="styles/main.css" />
</head>
```

### Style tag

```html
<head>
	<style>
	/* CSS goes here */
	</style>
</head>
```

### Inline Styles

```html
<p style="color: red;">...</p>
```

[[Selectors]]
[[Properties]]
[[Units]]
[[Variables]]