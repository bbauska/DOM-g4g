<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>HTML DOM (Document Object Model)</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The HTML DOM (Document Object Model) is a structured representation of a 
<a href="https://www.geeksforgeeks.org/websites-apps/web-page-a-complete-overview/">
web page</a> that allows developers to access, modify, and control its content and structure using 
<a href="https://www.geeksforgeeks.org/javascript/javascript-tutorial/">
JavaScript</a>. It powers most dynamic website interactions, enabling features like real-time updates, 
form validation, and interactive user interfaces.</p>

/* <DOM-image01of02.jpg> */
/* <DOM-image02of02.jpg> */

<ul>
  <li>The HTML Document Object Model (DOM) is a tree structure, where each HTML tag becomes a node 
    in the hierarchy.</li>
  <li>At the top, the &lt;html&gt; tag is the root element, containing both &lt;head&gt; and &lt;body&gt; as child 
      elements.</li>
  <li>These in turn have their own children, such as &lt;title&gt;, &lt;div&gt;, and nested elements 
      like &lt;h1&gt;, &lt;p&gt;, &lt;ul&gt;, and &lt;li&gt;.</li>
  <li>Elements that contain other elements are labeled as container elements, while elements that 
      do not are simply child elements.</li>
  <li>This hierarchy allows developers to navigate and manipulate web page content using JavaScript 
      by traversing from parent to child and vice versa.</li>
</ul>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Structure of the HTML DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Imagine your webpage as a tree:</p>
<ul>
  <li>The document is the root.</li>
  <li>HTML tags like &lt;html&gt;, &lt;head&gt;, and &lt;body&gt; are branches.</li>
  <li>Attributes, text, and other elements are the leaves.</li>
</ul>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Requirement of DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The DOM is essential because:</p>
<ul>
  <li>Dynamic Content Updates: Without reloading the page, the DOM allows content updates (e.g., 
      form validation, AJAX responses).</li>
  <li>User Interaction: It makes your webpage interactive (e.g., responding to button clicks, form 
      submissions).</li>
  <li>Flexibility: Developers can add, modify, or remove elements and styles in real-time.</li>
  <li>Cross-Platform Compatibility: It provides a standard way for scripts to interact with web 
      documents, ensuring browser compatibility.</li>
</ul>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Working of DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The DOM connects your webpage to JavaScript, allowing you to:</p>
<ul>
  <li>Access elements (like finding an &lt;h1&gt; tag).</li>
  <li>Modify content (like changing the text of a &lt;p&gt; tag).</li>
  <li>React to events (like a button click).</li>
  <li>Create or remove elements dynamically.</li>
</ul>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Types of DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The DOM is seperated into 3 parts:</p>
<ol type="a">
  <li>Core DOM: It is standard model for all document types (All DOM implementations must support 
      the interfaces listed as "fundamental" in the code specifications).</li>
  <li>XML DOM: It is standard model for XML Documents (as the name suggests, all XML elements can be 
      accessed through the XML DOM.)</li>
  <li>HTML DOM: It is standard model for HTML documents (The HTML DOM is a standard for how to get, 
      change, add, or delete HTML elements.)</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Properties of the DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ul>
  <li>Node-Based: Everything in the DOM is represented as a node (e.g., element nodes, text nodes, 
      attribute nodes).</li>
  <li>Hierarchical: The DOM has a parent-child relationship, forming a tree structure.</li>
  <li>Live: Changes made to the DOM using JavaScript are immediately reflected on the web page.</li>
  <li>Platform-Independent: It works across different platforms, browsers, and programming 
      languages.</li>
</ul>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>The Document</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The Document interface represents a web page loaded in the browser and acts as the main entry 
point to its content. It allows developers to access and manipulate the page through the DOM tree.</p>
<ul>
  <li>The DOM tree consists of nodes like &lt;body&gt;, &lt;table&gt;, and other HTML elements.</li>
  <li>The Document interface provides global access to page information such as the URL.</li>
  <li>It enables creating, modifying, and managing elements within the web page.</li>
</ul>

/* <DOM-image03.jpg> */

<p>HTML documents served with the "text/html" content-type, also implement the HTMLDocument 
interface, whereas XML and SVG documents implement the XMLDocument interface.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="bom">The Window (BOM)</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Before getting into the window object, let’s talk briefly about another concept, BOM. The 
Browser Object Model (BOM) allows JavaScript to “talk to” the browser. Even though there are no 
official standards for the 
<a href="https://www.geeksforgeeks.org/html/browser-object-model/">Browser Object Model (BOM)</a>, 
modern browsers have implemented (almost) the same methods and properties for JavaScript 
interactivity.</p>

<ul>
  <li>Now, the window object basically represents the browser window.</li>
  <li>All global JavaScript objects, functions, and variables automatically become members of the window object.</li>
  <li>Even the document object (of the HTML DOM) is a property of the window object.</li>
</ul>

```
window.document.getElementById(“header”);
```

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>The Object</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>All of the properties, methods, and events available for manipulating and creating web pages 
are organized into objects inside dom (for example, the document is itself an object that 
represents the document itself, the table an object that implements the special HTMLTableElement 
DOM interface for accessing HTML tables, and so forth).</p>

<ul>
  <li>The modern DOM is built using multiple APIs that work together.</li>
  <li>The core DOM defines the objects that fundamentally describe a document and the objects 
    within it.</li>
  <li>This is enhanced and expanded upon need.</li>
  <li>For example, the HTML DOM API adds support for representing HTML documents to the core 
    DOM.</li>
</ul>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>The Interface</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>In the HTML DOM, an interface is like a blueprint that defines the properties and methods available for different types of elements. For example, a<table> element uses the HTMLTableElement interface, which gives it special table-specific methods like insertRow(). Most elements inherit features from more general interfaces like Element and Node, allowing you to interact with them easily using JavaScript.</p>

/* <DOM-image04.jpg> */

<p>It shows how different types of HTML elements are related through interfaces, from general to 
more specific:</p>

<ul>
  <li>EventTarget is the base interface from which most DOM nodes inherit. It allows elements to 
    listen for and respond to events.</li>
  <li>Node extends EventTarget and represents any single point in the document tree—such as 
    elements, text, or comments.</li>
  <li>Document is a specialized type of Node that acts as the entry point to the entire DOM tree 
    (i.e., the web page).</li>
  <li>HTMLElement extends Node and represents any HTML element (like &lt;div&gt;, &lt;p&gt;, etc.).</li>
  <li>HTMLTableElement is a more specific type of HTMLElement tailored for &lt;table&gt; elements, 
    giving it extra table-related methods like insertRow().</li>
</ul>

<blockquote>
Note: The HTMLTableElement interface provides special properties and methods (beyond the regular HTMLElement object interface it also has available to it by inheritance) for manipulating the layout and presentation of tables in an HTML document.
</blockquote>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Accessing data from DOM</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>JavaScript uses the DOM to access the document and its elements in the webpage using the API for the 
<a href="https://developer.mozilla.org/en-US/docs/Web/API/Document">document</a> or <a href="https://developer.mozilla.org/en-US/docs/Web/API/Window">window</a>.

<p>For example, the standard DOM specifies that 
the getElementsByTagName the method in the code below must return a list of all the &lt;p&gt; 
elements in the document:</p>

```
const paragraphs = document.getElementsByTagName("p");
// paragraphs[0] is the first <p> element
```

<p>Similarly, we can also access HTML elements by:</p>
<ul>
  <li>id : var x = document.getElementById(“intro”); (Only one element gets returned with this method)</li>
  <li>class name: var x = document.getElementsByClassName(“intro”);</li>
  <li>CSS selectors: var x = document.querySelectorAll(“p.intro”);</li>
  <li>HTML elements by HTML object collections:</li>
</ul>
<br>

```
document.anchors.length;
document.forms.length;
document.images.length;
document.links.length;
document.scripts.length;
```

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>DOM Data Types</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>When working with the DOM (Document Object Model), there are different types of data or 
building blocks used behind the scenes. Here’s what they mean in everyday terms:</p>
<ul>
  <li>Document: Think of it as the entire webpage. It's like the starting point or the big box 
    that holds everything you see on a website.</li>
  <li>Node: Anything on the webpage—like a heading, paragraph, image, or even some hidden parts—
    is called a node. It’s like a small part or piece of the whole page.</li>
  <li>Element: This is a specific type of node. It represents actual tags you write in HTML, like 
    &lt;div&gt;, &lt;p&gt;, or &lt;img&gt;. These are the visible parts of the page.</li>
  <li>NodeList: Imagine you ask the page to give you all the buttons or all the paragraphs—it gives 
    you a list of those items. That list is called a NodeList. It's like a group of nodes stored 
    together.</li>
</ul>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Commonly Used DOM Methods</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<table>
  <tr style="align:center">
    <th>Methods</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>getElementById(id)</td>
    <td><a href="https://www.geeksforgeeks.org/html/html-dom-getelementbyid-method/">getElementById(id)</a> method is used to select an element by its unique ID.</td>
  </tr>
  <tr>
    <td>getElementsByClassName(class)</td>
    <td><a href="https://www.geeksforgeeks.org/javascript/html-dom-getelementsbyclassname-method/">getElementsByClassName(class)</a> method retrieves all elements that share a given class name.</td>
  </tr>
  <tr>
    <td>querySelector(selector)</td>
    <td><a href="https://www.geeksforgeeks.org/html/html-dom-queryselectorall-method/">querySelector(selector)</a> method returns the first element that matches the specified selector.</td>
  </tr>
  <tr>
    <td>createElement(tag)</td>
    <td><a href="https://www.geeksforgeeks.org/javascript/html-dom-createelement-method/">createElement(tag)</a>  method is used to create a new HMTL element dynamically.</td>
  </tr>
  <tr>
    <td>appendChild(node)</td>
    <td><a href="https://www.geeksforgeeks.org/html/html-dom-appendchild-method/">appendChild(node)</a> method adds a child node to an existing element.</td>
  </tr>
  <tr>
    <td>remove()</td>
    <td><a href="">remove() method is called to remove an element from the DOM.</a></td>
  </tr>
  <tr>
    <td>addEventListener(event,fn)</td>
    <td><a href="">addEventListener(event,fn)</a> method attaches an event handler function to an element.</td>
  </tr>
</table>

<p>Example: We use HTML element id to find the DOM HTML element.</p>

```
<html>
<body>
  <h2>GeeksforGeeks</h2>
  <!-- Finding the HTML Elements by their Id in DOM -->
  <p id="intro">
    A Computer Science portal for geeks.
  </p>
  <p>
    This example illustrates the <b>getElementById</b> method.
  </p>
  <p id="demo"></p>
  <script>
    const element = document.getElementById("intro");
    document.getElementById("demo").innerHTML =
      "GeeksforGeeks introduction is: " + element.innerHTML;
  </script>
</body>
</html>
```

<p>Example: This describes the representation of the HTML elements in the tree structure.</p>

```
<table>
  <ROWS>
    <tr>
      <td>Car</td>
      <td>Scooter</td>
    </tr>
    <tr>
      <td>MotorBike</td>
      <td>Bus</td>
    </tr>
  </ROWS>
</table>
```

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Understanding HTML Table Structure through DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>This image visually represents how &lt;table&gt; contains &lt;tr&gt; (rows), which contain 
&lt;td&gt; (cells), and how each cell can hold content like "Car", "Scooter", etc., making it a 
clear example of HTML DOM structure for tables.</p>

/* <DOM-image05.jpg> 8?

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Misunderstandings About the DOM</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ul>
  <li>It is not a binary description where it does not define any binary source code in its 
    interfaces.</li>
  <li>It is not used to describe objects in XML or HTML whereas the DOM describes XML and HTML 
    documents as objects.</li>
  <li>It is not represented by a set of data structures; it is an interface that specifies object representation.</li>
  <li>It does not show the criticality of objects in documents i.e it doesn't have information 
    about which object in the document is appropriate to the context and which is not.</li>
</ul>

<p>filename: index.html</p>

```
<html>
<head></head>
<body>
  <label>Enter Value 1: </label>
  <input type="text" id="val1" />
  <br />
  <br />
  <label>Enter Value 2: </label>
  <input type=".text" id="val2" />
  <br />
  <button onclick="getAdd()">Click To Add</button>
  <p id="result"></p>
  <script type="text/javascript">
    function getAdd() {
      // Fetch the value of input with id val1
      const num1 = Number(document.getElementById("val1").value);
      // Fetch the value of input with id val2
      const num2 = Number(document.getElementById("val2").value);
      const add = num1 + num2;
      console.log(add);
      // Displays the result in paragraph using dom
      document.getElementById("result").innerHTML = "Addition : " + add;
      // Changes the color of paragraph tag with red
      document.getElementById("result").style.color = "red";
    }
  </script>
</body>
</html>
```

<p>...the end</p>
