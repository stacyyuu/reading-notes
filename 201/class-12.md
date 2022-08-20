## Readings: Chart.js, Canvas

### Our reading today is based on HTML `<canvas>` element and Chart.js.
---

## JavaScript Canvas

1. What does the `<canvas>` allow a developer to achieve?
- Allows you to draw 2D graphics using JS. Requires at least two attributes, width and height that specifies the size of canvas.

2. What is the importance of the closing `</canvas>` tag?
- `<canvas>` requires a closing tag. 
- Any content between the opening and closing tags is fallback content that will display only if the browser doesn't support the `<canvas>` element.

3. Explain what the `getContext()` method does.
- Initially, the canvas is blank. To draw something, you need to access the rendering context and use it to draw on the canvas. 
- The canvas element features the `getContext()` method that returns a render context object.
- `getContext()` takes one argument which is the type of context. For example, you use the '2d' to get a 2D rendering context object, which is an instance of the CanvasRendingContext2d interface. 
- The 2D rendering context allows you to draw shapes, text, images, and other objects. 
- It is important to check if the browser supports the `getContext()` method.

## Chart.js Documentation

1. What is Chart.js and how can it be brought into your project?
- Chart.js allows you to create simple, clean, and engaging HTML5 based JS charts. It's a free JS library.
- We will need to use a chart to display our data for items and amount of times clicked. 
- To create, you need to add a link providing CDN (Content Delivery Network).
- Then, add a `<canvas>` to where you want to draw the chart. The canvas element must have a unique id. 

2. List 3 different Chart types you can create using Chart.js.
- Line Chart
- Bar Chart
- Pie Chart
- Scatter Plot

## Easily Create Stunning Animated Charts with Chart.js

1. What are some advantages to displaying data via a chart over a table?
- Data in a chart is easier to look at and convey data quickly, but they're not always easy to create. 

2. How could Chart.js aid your previously created applications visually?
- Chart.js is a JS plugin that uses HTML5's canvas element to create charts more easily. It gives the charts animated features and allows customization. 

