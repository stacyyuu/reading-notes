## CSS Layout

### 7/9/22: Our reading today is based on learning about CSS Flexbox. 

---

## Learn CSS - Flexbox

1. Flexbox is designed for one-dimensional content. Explain what this means.
- The Flexible Box Layout Model is a layout model that excels at taking a bunch of items which have different sizes, and returning the best layout for those items. 
-  Flex layouts have the following features:
- Can display as a row or as a column.
- Respect the writing mode of the document.
- Single line by default, but can be asked to wrap onto multiple lines.
- Items in layout can be visually reordered, away from their order in the DOM.
- Space can be distrbuted inside the items, so they become bigger and smaller according to the space available in their parent.
- Space can be distributed around items and flex lines in a wrapped layout, using the Box Alignment properties.
- Items themselves can be aligned on the cross axis. 

2. Explain the difference between the main axis and cross axis.
- The **main axis** is the one set by your `flex-direction property`. If that is `row`, your main axis is along the row. If it is `column`, your main axis is along the column. 
- Flex items move as a group on the main axis. 
- The **cross axis** runs in the other direction to the main axis. SO if `flex-direction` is `row`, the cross axis runs along the column. 
- You can do two things on the cross axis. You can move items individually or as a group so they align against each other and the flex container. Also, if you have wrapped flex lines, you can treat those lines as a group in order to control how space is assigned to those lines. 

3. How can using certain properties of flexbox negatively impact accessibility?
- You should be cautious when using any properties that reorder the visual display away from how things are ordered in the HTML document, as it can negatively impact accessibility. The `row-reverse` and the `column-reverse` values are a good example of this. 

## CSS Layout - Flexbox

1. What are some advantages of using flexbox over float?
- `floats` and `positioning` can be limiting. They are unable to achieve simple layout designs such as:
- Vertically centering a block of content inside its parent.
- Making all children of a container take up an equal amount of available width/height, regardless of how much width/height is available. 
- Making all columns in a multiple-column layout adopt the same height even if they contain a different amount of content. 

2. How does this topic connect with your long term goals?
- I would definitely incorporate a flex box in my future projects, I think it's important for a website to have ideal viewing properties.


[Back to main page](README.md)