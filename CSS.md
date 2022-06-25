# CSS
**6/25/22** 
### Today, in Code 102 we learned how to use CSS to customize the design of our webpage. 

---

**CSS** (Cascading Style Sheets) allows you to customize and design your website. It allows you to control exactly how HTML elements look like in the browser, presenting your markup using whatever design you like. 
- **Document**: Text file structured using markup language -- HTML being most common. 
- **Presenting**: Converting the document into a form usable by your audience. 
- CSS is a **rule-based** language -- the rules are defined by specifying groups of styles that should be applied to particular elements or groups of elements on the webpage. <br>
    Ex. `h1 {
        color : ; 
        font-size : ;
    }`
- CSS rule opens with a **selector**. This *selects* the HTML element that is going to be styled. In this case it is the level one heading (`<h1>`).
- Next, there's a set of curly brackets, {     }.
- Inside the brackets will be one ore more **declarations**, which take the form of **property** and **value** pairs. A property includes color (in above example) and the value includes the color you choose. 
- CSS language is broken down into **modules**.

**How to Add CSS**:
- **External CSS**
    - Change the look of entire website by changing one fily
    - Each HTML page must include reference to the external style sheet inside the `<link>` element, inside the `<head>` section. 
    - Ex. `<html>`<br>
`<head>`<br>
`<link rel="stylesheet" href="mystyle.css">`<br>
`</head>`<br>
`<body>`<br>
`<h1>This is a heading</h1>`<br>
`<p>This is a paragraph.</p>`<br>
`</body>`<br>
`</html>`

[Back to main page](README.md)