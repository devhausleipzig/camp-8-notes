## Import

We import external fonts at the top of our css file.

```css
@import url("link-to-font")

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
```

We mainly use [Google Fonts](https://fonts.google.com/) as our resource for external fonts. They are all open source and free to use commercially.

## Font familiy

```css
/* Single word font names */
p {
	font-family: Montserrat
}

/* Multi word font names */
p {
	font-family: 'MesloLGM NF'
}

/* Fallback */
p {
	font-family: Montserrat, sans-serif
}
```

> [!info]
>If we use `sans-serif` or `serif` as a fallback, the users system picks the its default for that familiy.

## Font size

```css
p {
	font-size: 16px;
}
```

## Font style

```css
p {
	font-style: italic; /* normal | italic */
}
```

## Font weight

```css
p {
	font-weight: ; /* 100 - 900 | normal | bold */
	/* 400 - normal */
	/* 700 - bold */
}
```