The `link` tag is used to import external resources (files) into our document
2 major use cases would be importing [[Languages/CSS/MOC|CSS]] and `fonts`

```html
<!-- Import a css file -->
<link rel="stylesheet" href="styles/main.css" />

<!-- Import an external font -->
<link rel="preconnect" href="https://fonts.googleapis.com">  
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>  
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```