# Objects, and the DOM

## What is an object

Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.

* **IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES:** If a variable is part of an object, it is called a property. Properties te ll us about the object, such as the name of a hotel or the number of rooms it has Each individual hotel might have a different name and a different number of rooms.

* **IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS:** If a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from the total number of rooms.

### CREATING OBJECTS USING LITERAL NOTATION

The example bellow shows how to create an object using the literal notation:

    var hotel = {
        name: 'Quay',
        rooms : 40,
        booked: 25,
        checkAvailability: function() {
            return this.rooms - this.booked;}
            } ;
            JAVASCRIPT
            var elName = document .getElementByld('hotelName');
            elName.textContent =hotel .name;
            var elRooms = document.getElementByid{'rooms');
            elRooms .textContent = hotel .checkAvailability();

## Document Object Model (DOM)

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.

The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas:

1. **MAKING A MODEL OF THE HTML PAGE:** When the browser loads a web page, it creates a model of the page in memory.

The DOM specifies the way in which the browser should structure this model using a **DOM tree**.

The DOM is called an object model because the model (the DOM tree) is made of objects. Each object represents a different part of the page loaded in the browser window.

2. **ACCESSING AND CHANGING THE HTML PAGE:**

The DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser.

### THE DOM TREE IS A MODEL OF A WEB PAGE

As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes.

* **THE DOCUMENT NODE:** Every element, attribute, and piece of text in the HTML is represented by its own DOM node. At the top of the tree a document node is added; it represents the entire page.

* **ELEMENT NODES:** HTML elements describe the structure of an HTML page. (The `<hl> - <h6>` elements describe what parts are headings; the `<p>` tags indicate where paragraphs of text start and finish; and so on.)

Relationships between the document and all of the element nodes are described using the same terms as a family tree: parents, children, siblings, ancestors, and descendants. (Every node is a descendant of the document node.)

Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in the browser.

* **ATTRIBUTE NODES:** The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree.

Attribute nodes are not children of the element thar carries them; they are part of that element. Once you access an element, there are specific JavaScript methods and properties to read or change that element's attributes. For example, it is common to change the values of cl ass attributes to trigger new CSS rules that affect their presentation.

* **TEXT NODES:** Once you have accessed an element node, you can then reach the text within that element. This is stored in its own text node.