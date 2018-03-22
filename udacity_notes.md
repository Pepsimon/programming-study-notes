# The DOM and Accessing Elements.

**The DOM stands for Document Object Model. The DOM is parsed by the browser.**


First the browser gets the HTML and then it runs the characters through a process where it converts each character to tokens.

These tokens are:

- *DOCTYPE*
- *start tag*
- *end tag*
- *comment*
- *character*
- *end-of-file*

These tokens are then converted to Nodes, and finally the DOM is created in a tree-like structure by converting the nodes. This Document object is not a part of the javaScript language, but is expected to be freely accessible through javaScript.

"a tree structure that captures the content and properties of the HTML and all the relationships between the nodes

the DOM is the full, parsed representation of the HTML"

### Node

The Node is a blueprint that contains all the information about properties and methods. These properties and methods are then passed on to the elements that are created (node elements). These element nodes are created from the Element interface which is a descendant of the Node interface, hence it inherits all the properties and methods from the Node and passes them on to the nodes.

### Element

When a node is created it inherits properties and methods from its parent, the Element interface which is a descendant of the Node.

Read more about [Web API's](https://developer.mozilla.org/en-US/docs/Web/API)

### Accessing Elements

The document object has methods on it that helps us access the different elements in the DOM.

 First we look at `document.getElementById()`. This method helps us get an element who's `id = ''` is set to some chosen id. This method returns a single item, and is called on the document object.

Returning multiple elements we can use `document.getElementsByClassName()` and `document.getElementsByTagName()`.

Using the `getElementsByClassName()`, you provide the method a parameter that matches some class name you have assigned to your elements, and then it will return a list with those elements. This list is not an array, and will not have the same methods on it as an array object would have. This method is also available on the Element nodes.

Using the `getElementsByTagName()` will return all elements in your object that has the tag name e.x (`div`). And return them as a list. Same as the `getElementsByClassName`.

If you want to select elements the way we select them in CSS, we can use `querySelector()`.  When using this method, you pass in a string that's just like a CSS selector:

`document.querySelector('#header_one')`
`document.querySelector('.list_item')`

The `querySelector()` method only returns one element from the DOM. If you want to return several elements, use the `querySelectorAll()` method, here you get back a list of matched elements.

`document.querySelectorAll('div') // Returns a list with all <div> elements`

NB. When we get back a list from these methods, the list we get back is a NodeList. This list has some methods on it for iterating over these elements e.x `forEach` and the `for` loop.
[NodeList on MDN](https://developer.mozilla.org/en-US/docs/Web/API/NodeList)

Read more about querySelector at [MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)
