<h2>Document Object Model (DOM)</h2>
<p align='right'><a href="https://github.com/nrjp/javascript">Index</a></p>

The `Document Object Model (DOM)` is the data representation of the objects that comprise the structure and content of a document on the web

The Document Object Model (DOM) is an API for manipulating DOM trees of HTML and XML documents (among other tree-like documents). This API is at the root of the description of a page and serves as a base for scripting on the web.

```
<html lang="en">
  <head>
    <title>My Document</title>
  </head>
  <body>
    <h1>Header</h1>
    <p>Paragraph</p>
  </body>
</html>
```
![Screenshot](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Using_the_Document_Object_Model/using_the_w3c_dom_level_1_core-doctree.jpg)

<h3>DOM Method</h3>
<br />

| Method | Description |
|--------|-------------|
| `document.getElementById(id)` | Returns the element with the specified ID. |
| `document.getElementsByClassName(className)` | Returns a collection of elements with the specified class name. |
| `document.getElementsByTagName(tagName)` | Returns a collection of elements with the specified tag name. |
| `document.querySelector(selector)` | Returns the first element that matches the specified CSS selector. |
| `document.querySelectorAll(selector)` | Returns a static NodeList of all elements that match the specified CSS selector. |
| `document.createElement(tagName)` | Creates a new element with the specified tag name. |
| `parent.appendChild(node)` | Adds a node as the last child of a parent node. |
| `element.innerHTML` | Gets or sets the HTML content of an element. |
| `element.style.property` | Gets or sets the value of a specified style property for an element. |
| `element.setAttribute(name, value)` | Sets the value of an attribute on an element. |
| `element.getAttribute(name)` | Gets the value of an attribute on an element. |
| `element.addEventListener(event, function)` | Attaches an event listener to an element. |
| `window.content` | Returns a reference to the window object's document. |
| `window.onload` | Event that fires when the page has finished loading. |
| `window.scrollTo(xpos, ypos)` | Scrolls the window to a specified position. |

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<br />

<h3>window</h3>

The `window object` represents an open window in a browser. It is the global object in the browser's JavaScript environment and provides several methods that allow you to interact with the browser window.

|Method         	| Description | 
|-------------------|-------------|
| alert()	        | Displays an alert box with a message and an OK button |
| prompt()	        | Displays a dialog box that prompts the user for input |
| confirm()	        | Displays a dialog box with a message and OK/Cancel buttons |
| setInterval()	    | Repeatedly executes a function at a specified interval |
| setTimeout()	    | Executes a function after a specified delay |
| clearInterval()	    | Clears the interval set by setInterval() |
| clearTimeout()	    | Clears the timeout set by setTimeout() |
| open()	            | Opens a new browser window or a new tab |
| close()	            | Closes the current browser window |
| focus()	            | Sets focus to the current window |
| blur()	            | Removes focus from the current window |
| scrollBy()	        | Scrolls the window by a specified number of pixels |
| scrollTo()	        | Scrolls the window to a specified position |
| resizeBy()	        | Resizes the window by a specified number of pixels |
| resizeTo()      	| Resizes the window to a specified width and height |
| moveBy()	        | Moves the window by a specified number of pixels |
| moveTo()	        | Moves the window to a specified position |
| getComputedStyle()	| Returns the computed style of an element |
| matchMedia()	    | Returns a MediaQueryList object representing a CSS media query |
| requestAnimationFrame()	| Requests that the browser call a specified function to update an animation before the next repaint |
| cancelAnimationFrame()	| Cancels an animation frame request previously scheduled with requestAnimationFrame() |


<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<h3>Event listener</h3>

The `addEventListener()` method is used to attach an event listener to an element. It takes two arguments: the type of event to listen for and the function to execute when the event is triggered.

<p align='right'><a href="#top">&#8593; Back to Top</a></p>
