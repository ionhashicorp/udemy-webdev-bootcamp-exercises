# 114

## Add javascript to websites

- inline: add javascript to a website (note the body attribute with onload)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body onload="alert('Hello')">
    <h1>Hello</h1>
  </body>
</html>
```

- internal via script tag: add javascript in between the script tag

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1>Hello</h1>
    <script>
      alert('Hello');
    </script>
  </body>
</html>
```

- external via script tag

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1>Hello</h1>
    <script src="app.js"></script>
  </body>
</html>
```

```javascript
// app.js
alert('Hello');
```
