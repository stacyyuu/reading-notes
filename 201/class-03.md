## Basics of HTML, CSS, & JS

### 7/14/22: Our reading today is based on HTML Lists, Control Flow with JS, and the CSS Box Model.

---

## Learn HTML: Ordered and Unordered list

1. When should you use an unordered list in your HTML document?
- You would use an `<ul>` when you want a list to not be numbered, it is automatically rendered as bullet points. 

2. How do you change the bullet style of unordered list items?
- To change the bullet style, you would use CSS. The `list-style: ;` property allows you to input a style you prefer. 

3. When should you use an ordered list vs an unorder list in your HTML document?
- You would use an `ol` in your document if you wanted to list something off, starting at the number 1 by default. 

4. Describe two ways you can change the numbers on list items provided by an ordered list?
- You can the `type` attribute to the `<ol>` tag. 
- `<ol type= "A">` creates an ordered list that is numbered with uppercase letters. (A, B, C)
- `<ol type= "a">` creates an ordered list that is numbered with lowercase letters. (a, b, c)
- `<ol type = "I">` creates an ordered list that is numbered with uppercase roman numbers. (I, II, III)
- `<ol type = "i">` creates an ordered list that is numbered with lowercase roman numbers. (i, ii, iii)

## Learn CSS: The Box Model

1. Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?
- Margin is the space around an element's border. It ontrols the space outside an element. 
- Padding is the space between an element's border and the element's content. It controls the space inside an element. 

2. List and describe the four parts of an HTML elements box as referred to by the box model.
- **Content**: area where content is displayed. Size it using properties such as inline-size and block-size or width and height. 
- **Padding**: sits around the content as white space. 
**Border**: Wraps content and any padding. 
- **Margin**: is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements. 

## Learn JS: Arrays, Operators and Expressions, Conitionals, and Loops

1. What data types can you store inside of an Array?
- **Arrays** allow you to store a list of data items under a single variable name. Generally described as "list-like objects". If we didn't have arrays, we'd have to store every item in a seperate variable. 
- It can store strings, numbers, objects, and even other arrays. 
- Arrays can also contain mixed data types. 

2. Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?

 `const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];`

 - I believe that it's not valid because the `]` is not being used correctly to place an array in another array. 
 - `const random = ['tree', 795, [0, 1, 2]]` is the proper way to place an array in another array. 
 - `null` value can be used in an array. 

3. List five shorthand operators for assignment in javascript and describe what they do.

| **Operator**            |          **Function** |
| :---: | :---: |
| `Addition +` | Adds numbers, ex. `let z = x +y;` |
| `Assignment =` | Assigns value to variable, ex. `let x = 10;` |
| `*` | Multiplies numbers |
| `-` | Subtracts numbers |
| `**` | Exponentiation, raises first operand to power of second operand, <br>ex. `let z = x ** 2;` result is `25` |
| `/`| Divides numbers |
| `%` | Division remainder|
| `++` | Increment |
| `--`| Decrement|
| `+=`| `x += y`, same as `x = x + y`|
| `let text3 = text1 + "" + text2;`| Concatenate strings |
| `let z = "Hello" + 5;`| Adds strings and numbers|



4. Read the code below and evaluate the last expression and explain what the result would be and why.

`let a = 10;
 let b = 'dog';
 let c = false;`

 `// evaluate this
 (a + c) + b;`

- The result turns out to be `'10dog`. This is because c is given a false value, which would cancel it out.


5. Describe a real world example of when a conditional statement should be used in a JavaScript program.
- A conditional statement could be used to find out if a person was of a certain age in order to be able to do something. 
- `if (age <= 21) {`<br>
    `alert('You are underage and cannot drink alcohol.')`<br>
`} else if (age >=21) {`<br>
   ` alert('You are of age and can drink alcohol.')`<br>
`} else {`<br>
    `alert('Please give valid age.')`<br>
`}`

6. Give an example of when a Loop is useful in JavaScript.
- **Loops** are useful when you want to do the same thing over and over again. 
- This helps use reduce repitition of code. 
- `for (let i = 0; i < 100; i++)` lets us run 100 iterations of the code and if we wanted to change the amount of iterations, we would just have to change one number in the code. 

## Things I want to know more about
- More practice with loops and conditionals!