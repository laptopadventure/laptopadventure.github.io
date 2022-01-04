# Daily Reading 8 Notes

[Back to the table of contents](../README.md)

## Online Reading 1: "Layout"

### Block display

Block display makes a new line, which means they don't usually sit next to eachother. If you do want them to sit next to eachother, you should consider the inline display. This is one of the two css defaults for html tags.

### Inline display

Essentially block display but it doesn't try to put the contents on a new line. This means you can use inline to wrap around words without ruining your paragraph. You know, surround text with a span that would make it bold, or bigger, etc. This is the other of the two css defaults for html tags.

### Flex display

Meant for solving one dimensional layouts, aka either horizontal or vertical filling of a container. Flexbox offers a variety of options for smartly filling the container with calculated spacing.

### Grid display

Meant for solving multi-dimensional layouts. It will map out an entire space as a grid, and each item will then take a single spot in that grid. You can then define specific items in the grid to take up more space, which can shape the container in a very open ended way. Awesome!

### Flow

When not using special display uses, your elements will display in "The Flow". Aka, they will either inline or block and they will come one after another in their html.

### Floats

We can break flow, sticking something to the left or right if we want other text to not consider it part of the flow but rather an obstruction to fill the container around.

### Multi-column lists

Last little misc section here, there are css properties for breaking up columns into however many "new lines". Very long lists can be safely cut up so they don't take too much vertical space (Difficult to build a website that is really long but only because of a single element.)

### Positioning

#### Static

Default position that is essentially how the element would normally follow the flow of the document.

#### Relative

Allows you to move the element with its origin point being from where it was. For example, if I add `top: 10px` to a relative element it will render 10 pixels below where it would normally be if it was respecting flow.

#### Absolute

Same as above, but the origin point is relative to the top right of the entire document. Basically, you're hard setting its location. Use sparingly, because you really shouldn't be doing this a lot!

#### Sticky

Sticky respects normal flow, but refuses to not be seen. A sticky element will not leave the page but rather stick around at the closest point that is still on the screen to where it should be, "sticking" around after you scroll past until you return.

#### Fixed

Fixed entirely abandons the normal flow, and acts as an absolute element to your window, which means as you scroll it will follow and always be in your view entirely outside the document itself.