---
layout: doc
title: Static Files
---

Add your files to `public` directory and Kemal will serve these files immediately.

```
app/
  src/
    your_app.cr
  public/
    js/
      jquery.js
      your_app.js
    css/
      your_app.css
    index.html
```

Open index.html and add

```html
<html>
 <head>
   <script src="/js/jquery.js"></script>
   <script src="/js/your_app.js"></script>
   <link rel="stylesheet" href="/css/your_app.css"/>
 </head>
 <body>
   ...
 </body>
</html>
```

## Disabling Static File Serving

By default `Kemal` serves static files from `public` folder. If you don't need static file serving at all(for example an API won't gonna need it) you can disable it like

```crystal
serve_static false
```
