## HTML Links, CSS Layout, & JS Functions

### 7/18/22: Our reading today is based on HTML Links, JS Functions, & Intro to CSS Layout

---

## Learn HTML: Creating Hyperlinks

1. To create a basic link, we wrap text or other content inside what element?
- **Hyperlinks** allow us to link documents to other documents or resources, link to specific parts of documents, or make apps available at web address. 
- Text is wrapped inside a `<a>` element and using the `href` attribute. 

2. The href attribute contains what information?
- `href` is also known as **Hypertext Reference**, or **target**, that contains the web address. 
- Another attribute you may want to add to your links is `title`. 
- Title contains additional information about the link, such as which kind of information the page contains, or things to be aware of on the website. 
- `<p>I'm creating a link to` <br>
`<a href = "https://www.mozilla.org/en-US/">the Mozilla homepage` <br>
  `title = "The best place to find more information about Mozilla's` <br>
          `mission and how to contribute">the Mozilla homepage</a>.` <br>
`</p>`

3. What are some ways we can ensure links on our pages are accessible to all readers?
- Use clear link wording:
- Screen reader users like jumping from link to link on a page, and reading links out of context. 
- Search engines use link text to index target files, so it is a good idea to include keywords in your link text to effectively describe what is being linked. 
- Visual readers skin over the page and their eyes will be drawn to page features that stand out, like links. They will find descriptive link text useful. 
- **Good** link text:
- `<p><a href="https://www.mozilla.org/firefox/">`<br>
  `Download Firefox`<br>
`</a></p>`<br>
- **Bad** link text:
- `<p><a href="https://www.mozilla.org/firefox/">`<br>
  `Click here` <br>
`</a>` <br>
`to download Firefox</p>`

- Other tips:
- Don't repeat URL as part of the link text.
- Don't say 'link' or 'links to' in link text - users will already be aware it is a link because it is styled different.
- Keep link text as short as possible.
- Minimize instances where multiple copies of the same text are linked to different places. 

## CSS Layout: Normal Flow & Positioning

1. What is meant by “normal flow”?
- **Normal Flow** is the how the webpage elements lay out themselves if the layout has not been changed. 
- Elements can be changed by adjusting their position with CSS in normal flow or by removing them from it altogether. 
- Starting with a solid, well-structured document that's readable in normal flow is the best way to begin any webpage. 
- It ensures your content is readable even if the user's using a very limited browser or a device. 

2. What are a few differences between block-level and inline elements?
- **Block Level Element** has contents that fill the availabe inline space of the parent element containing it. It grows along the block dimension to accomodate it. 
 -**Inline Elements** has contents that fill to the size of just what it contains. 
 - You can't adjust inline elements by width or height - they sit inside the content of block level elements. 
 - To control the size of an inline element, it has to be set to behave like a block level element. 
 - `display: block;` or `display: inline-block`. This mixes characteristics from both. 

3. __ positioning is the default for every html element.
- **Positioning** allows you to take elements out of normal document flow and make them behave differently. 
- **Static** positioning is the default that every element gets. 
- `position: static;`
- To modify, you can use `top`, `bottom`, `left`, and `right` properties. 

4. Name a few advantages to using absolute positioning on an element.
- `position: aboslute;`
- Creates a separate layer from everything else. 
- It allows us to create isolated UI features that don't interfere with the layout of other elements on the page. 
- Ex. popup information boxes, control menus, rollover panels, UI features that can be dragged and dropped anywhere on the page. 
- `top`, `bottom`, `left`, `right` behave in a different way. They specify the distance the element should be from each of the containing element's sides. You would then add px to the positions.

5. What is a key difference between fixed positioning and absolute positioning?
- **Fixed Positioning** works exactly the same as absolute positioning, the difference being fixed usually fixes an element in place relative to the visible portion of the viewport. 
- Absolute positioning fixes an element in place relative to its nearest positioned ancestor. 
- **Sticky Positioning** is a hybrid between relative and fixed position. It allows a positioned element to act like it's relatively positioned until it's scrolled to a certain threshold, after which it becomes fixed. 

## Learn JS: Functions - Reusable Blocks of Code
1. Describe the difference between a function declaration and a function invocation.
- **Functions** allow you to store a piece of code that does a single task inside a defined block, and then you call that code whenever you need it using a single short command - rather than having to type out the same code multiple times. 
- **Declaration** defining a function or creating a function. 
- **Invocation**: After a function has been defined, you have to run it - or invoke - it. This is done by including the name of the function in code somewhere, followed by parenthesis. 
- `function myName(){}`<br>
`myName();`

2. What is the difference between a parameter and an argument?
- **Parameters** are values that need to be included inside fuction parenthesis to make sure it does its job properly. 
- Parameters are properties of a function. *Aliases* for the values that will be passed to the function. 
- **Arguments** are properties of a particular call to a function. The actual values of the function. 

## Misc: 6 Reasons for Pair Programming 
1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.
- Engaged collaboration and learning from fellow students are two benefits that will help me on my coding journey. It is always helpful to learn from other students and see the way they handle solving a certain challenge. Everyone thinks differently and there's always something new to learn from another person. There is a higher chance in finding a solution when you are working with others. 

## Things I want to know more about
- How to use functions!

[Back to main page](README.md)

