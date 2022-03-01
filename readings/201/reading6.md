# Daily Reading 6 Notes

[Back to the table of contents](../README.md)

## Online Reading 1: "Problem Domain"

Problem Domain is in essence the familiarity you have with the system, and thus how quickly you can understand problems with it. On the site, the writer talks about always teaching the same basic conceptually simple program, one that manages each user's protein intake. Because it's easy to understand what's going on, and what this is for, it's easy to identify problems and solve them. Even returning to the same project with a new problem skips having to learn the problem domain and figure out what's going on and why. Fixes can take an incredibly long time without an understanding of the underlying system.

## Online Reading 2: "Primitives vs Object References"

Primitive values are types provided by JS, and they're immutable. Immutable means you cannot change their value, only reassign it to something else. Accessing the first letter of "snow" and changing it to a "k" won't actually do anything because the value is, as mentioned before, immutable. Objects on the other hand, have mutable values. Arrays are objects for example, and we can change what the values in an array are directly. It's still an array!

The big difference other than mutability vs immutability is accessing it. When you have a var assigned to something, anything you do with the var will be entirely about what that var's value is. But when you have a var assigned to an object, You're not referencing that object's value `{whatever: "this is"}` but rather it's memory position. So what does that mean? I'll show an example to finish us off for this section:

```js
  let emptyArray = [];
  //primitive value
  let primitive = 5;
  //non primitive value
  let object = {name: "John the Object"};
  //this line adds 5 to the array. Makes sense
  emptyArray.push(primitive);
  //this line adds the object to the array, not it's values. You can access the object in the array and work with its values, though!
  emptyArray.push(object);
```

## JS Chapter 3: "Object Literals"

Model of an Object:

```js
  let hotel = {
    //these are properties of the hotel, accessed with hotel.name
    //can also access with hotel['name']
    name: 'Quay:',
    rooms: 40,
    booked: 25,
    gym: true,
    roomTypes: ['twin', 'double', 'suite'],
    //this is a method, accessed with hotel.checkAvailability()
    //can also call with hotel['checkAvailability']()
    checkAvailability: function() {
      return this.rooms - this.booked;
    }
  };
```

## JS Chapter 5: "Document Object Model"

A DOM tree is the model of a web page. While we use HTML to create DOM trees, we can interact with built or unbuilt DOM trees with js, which lets us modify websites with js scripts. The tree is made up of objects, that hold children objects as properties in themselves. An unordered list has children of list items, and those have text nodes inside them. Speaking of which, there are two special nodes:

* Text Node: Cannot have children, represents text inside of an html tag.
* Attribute Node: Not children of the parent node to the attribute's node, and doesn't have children itself. It's linked to one node as that node's attributes. You can modify this node to modify how the node it's linked to's appearance on the webpage.

Nodes have nextSibling and previousSibling as object properties to get the next and previous nodes.

### Methods for working with DOM

Keep in mind these must be called from the document object itself. These are methods after all!

* getElementById(id): Gets the element by what it's ID is on the DOM.
* querySelector(selector): Gets the first element that matches a css selector.
* getElementsByClassName(className): Gets all elements with the specified class name.
* querySelectorForAll(selector): Same as querySelector() but instead of first match, all matches.
* createElement(tagName, options): Makes a new element for the page. Note you have to then add it to the DOM tree as something's child.
* createTextNode(string): Makes a new text node with specified text. See above, you must make it someone's child.
* node.appendChild(target): Appends whatever "node" is to "target".
* node.removeChild(target): Same as above, but the opposite.
* node.hasAttribute(): returns whether it has an attribute.
* node.getAttribute(attr): returns the attribute queried.
* node.setAttribute(attrName, attrValue): sets the attrName's value to a new one (attrValue). 