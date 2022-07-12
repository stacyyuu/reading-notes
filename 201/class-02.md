## Basics of HTML, CSS, & JS

### 7/11/22: Our reading today is based on learning the basics of HTML, CSS, & JS.

---

## Intro to HTML
1. Why is it important to use semantic elements in our HTML?
- A semantic element clearly defines its content to both the browser and developer.

2. How many levels of headings are there in HTML?
- There are six heading elements: `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>`

3. What are some uses for the `<sup>` and `<sub>` elements?
- **Superscript** and **subscript** are used when marking up things such as dates, chemical formula, and math equations. 
- `<sup>` element is used for superscript. Ex. Today is the 11<sup>th</sup>.
- `<sub>` element is used for subscript. Ex. H<sub>2</sub>O.

4. When using the `<abbr>` element, what attribute must be added to provide the full expansion of the term?
- `<abbr>` represents an abbreviation or acronym. `title` attribute is added to provide an expansion or description. Ex. `<abbr title = 'HyperText Markup Language'>`. 
<br>

## Learn CSS
1. What are ways we can apply CSS to our HTML?
 - **External Stylesheet**: Contains CSS in separate file with `.css` extension. Most common and useful method. 
 <br> `  <link rel="stylesheet" href="styles.css">` placed in `<head>` tag. 
 - **Internal Stylesheet**: Resides in HTML document. 
 <br> CSS is placed in a `<style>` element and contained inside `<head>` tag.
 - **Inline Styles**: CSS that affects a single HTML element. 
 <br>It is contained within a `style` attribute. <br> `<p style="color:red;">This is my first CSS example</p>`

2. Why should we avoid using inline styles?
- It is not considered best practice. 
- It is the least efficient way since it may require multiple edits in a single page. 
- It makes it more difficult to understand when CSS is mixed in HTML code. 

3. Review the block of code below and answer the following questions:
    <br>`h2 {` <br>
        `color: black;` <br>
        `padding: 5px;`<br>
        `}`
    1. What is representing the selector?
    - The second level heading. 
    2. Which components are the CSS declarations?
    - Color and padding. 
    3. Which components are considered properties?
    - Black and 5px. 
<br>

## Learn JS
1. What data type is a sequence of text enclosed in single quote marks?
- A string.

2. List 4 types of JavaScript operators.
- **Operator** is a mathematical symbol which produces results based on two value or variables. 
    - Addition `+`
    - Subtraction, Multiplication, Division `-, *, /`
    - Assignment `=`
    - Strictly equal `===`

3. Describe a real world Problem you could solve with a Function.
- A function can be used to measure temperature. The temperature will act as the input. The measurement that comes out as either C or F degrees will act as the output. 

4. An if statement checks a __ and if it evaluates to ___, then the code block will execute.
- An `if` statement checks a condition and if it evaluates to true, then the code block will execute. 
- Provides us with two choices, or outcomes. 

5. What is the use of an else if?
- Allows us to have more choices or outcomes by adding an `else` statement. 

6. List 3 different types of comparison operators.
- `===` and `!=` test if one value is identical to, or not identical to, another.
- `<` and `>` test if one value is less than or greater than another. 
- `<=` and `>=` test if one value is less than or equal to, or greater than or equal to, another.  

7. What is the difference between the logical operator && and ||?
- `&&` AND; allows you to combine two or more expressions so that they all have to individually equal true for the whole expression to equal true.
- `||` OR; allows you to combine two or more expressions so that one or more of them have to individually evaluate to true for the whole expression to return true. 

## Things I want to know more about
- How to use the logical operators. 

[Back to main page](README.md)