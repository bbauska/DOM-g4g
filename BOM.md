The Browser Object Model (BOM) in JavaScript helps to interact with the browser, not just the 
webpage. While the DOM handles the content of the page, BOM gives you control over things like 
the browser window, the URL, and the history. This means you can do things like resize the 
window, go back and forth in the browser history, or even find out what browser the user is 
using. In short, BOM helps JavaScript work with the browser to make web pages more interactive.


Browser Object Model Types
Here are the main parts of the Browser Object Model (BOM)

Object	Description
window	Represents the browser window, controlling aspects like size and location, and serves as the global object.
navigator	Provides details about the user's browser and operating system.
location	Manages the current URL, allowing for retrieval and modification of the web address.
screen	Offers information about the user's screen, such as its width and height.
history	Provides access to the browser's session history, enabling navigation through the user's browsing history.
Let's see each part of the Browser Object Model in more detail.

1. Window Object
The window object is the main object in the BOM, representing the browser window or tab itself. It's the top-level object, and everything else in the browser is contained within it.


window.alert('Hello, World!');
console.log(window.innerWidth); 
The window object provides methods like alert(), confirm(), and prompt().
It also gives you access to other important objects, such as document, navigator, screen, location, and history.


