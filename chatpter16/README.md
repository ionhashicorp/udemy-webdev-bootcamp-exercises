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

# 115

## Add javascript to websites

- using DOM target this HTML elements

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8" />
    <title>My Website</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1 id="title">Hello</h1>
    <input type="checkbox" />
    <button style=":active color:red;">Click Me</button>
    <ul>
      <li class="list">
        <a href="https://www.google.com">Google</a>
      </li>
      <li class="list">Second</li>
      <li class="list">Third</li>
    </ul>
  </body>
</html>
```

```js
// results in <h1>Hello</h1>
document.firstElementChild.lastElementChild.firstElementChild;

// Change h1 element into Good Bye
document.firstElementChild.lastElementChild.firstElementChild.innerHTML =
  'Good Bye';

// DOM target h1 using querySelector
document.querySelector('h1');

// DOM simulate a mouse click
document.querySelector('input').click();

// Select third element of the list and change its text to iooon
document.querySelectorAll('li')[2].innerText = 'iooon';
```

# 116

```js
// Select elements by TAG getElementsByTagName (plural)
document.getElementsByTagName('li');

// Select third eleemnt of the list and change color to blue
document.getElementsByTagName('li')[2].style.color = 'blue';

// Select an elements by targeting the class name - bellow returns all list items
document.getElementsByClassName('list');

// Target element ID (one only) - returns h1 - and replace it to its text
document.getElementById('title').innerHTML = 'Good Bye';

// Target a class of an element -> returns only one element
document.querySelector('.btn');

// Target an ID only
document.querySelector('#title');

// Combine selectors - return the anchor that has as ancestor the li element
document.querySelector('li a');

// Return the list item that also has as attribute class .item
document.querySelector('li.list');

// Make the anchor tag red
document.querySelector('ul li a').style.color = 'red';
```

# 118

```js
// Make font size 10rem for h1
document.querySelector('h1').style.fontSize = '10rem';

// hide h1 element
document.querySelector('h1').style.visibility = 'hidden';

// set background color of button to yellow
document.querySelector('button').style.backgroundColor = 'yellow';
```

# 119

- styles should be placed in CSS files and HTML in html files (separation is the key)
- Add this to the style.css

```css
.invisible {
  visibility: hidden;
}
.huge {
  font-size: 10rem;
}
```

```js
// Return a class list (all class attributes of an HTML element)
document.querySelector('li').classList;

// add a class value to an HTML attribute (button should dissapear)
document.querySelector('button').classList.add('invisible');
document.querySelector('button').classList;

// add class .huge to h1 element (style.css includes already this class)
document.querySelector('h1').classList.add('huge');
```

# 120

- innerHTML vs textContent

```js
// return inner HTML of the first li
document.querySelector('ul li');

// target h1 and add BYE between em tags
document.querySelector('h1').innerHTML = '<em>BYE</em>';

// return ALL text within the unordered list
document.querySelector('ul').innerText;
```
