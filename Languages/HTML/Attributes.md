Attributes fulfill different purposes, some are used to group elements, some are used to uniquely identify an element and others give additional information.

### Grouping

#### Class

If we want to group a set of elements to e.g. apply a certain type of styling we can use a class:

```html
<style>
	.section-heading {
		font-size: 2rem;
		font-weight: bold
	}
	.section-description {
		font-size: 1rem;
	}
</style>

<h2 class="section-heading">...</h2>
<p class="section-description">...</p>
<h2 class="section-heading">...</h2>
<p class="section-description">...</p>
```

All the h2 and p tags with the same class would get the same styling.
H2s with the class of `section-heading` would be 32px and bold.
Ps with the class of `section-description` would be 16px.


### Identifying

#### ID

If we want to select a unique element on the [[Document]] we can use and ID

```html
<p id="super-special-paragraph">...</p>
```

> [!caution]
>A specific ID can only be used once per document.

### Tag-specific attributes

#### Hyperreference

When we use a [[Anchor]] Tag, we need to specifiy where the browser should take us when we click on it.

```html
<!-- External Link -->
<a href="http://google.com">My Link</a>
<!-- Internal Link -->
<a href="about.html">About me</a>
```

#### Target

If we want to open the link in a new tab, we can specify the `target` attribute with the `_blank` value.

```html
<a href="http://google.com" target="_blank">My Link</a>
```

#### Source

The two main types of media on the web are images and videos. We can represent those with their respective tags `<img />` and `<video />`. We need to point to the actual file they should display by using the `src` attribute.

```html
<img src="http://link-to-my-image.jpg" />
<video src="http://link-to-my-video.mp4" />
```

> [!caution]
> You can not directly put a youtuube video link in the `src` of a video.
> Use the YouTube embed snippet instead

#### Alternative Text

The `alt` attribute has multiple responsibilities:
- Image descriptiion
- SEO
- Screen readers

Also the alt text gets displayed when the image link is broken

```html
<img src="http://link-to-my-img.jpg" alt="My fancy image" />
```