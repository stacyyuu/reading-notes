# JavaScript
**6/25/22** 
### Today, in Code 102 we learned how to use JavaScript to add functions to our pages. 

---

**JavaScript** is a lightweight, interpreted, or just-in-time complied programming language with first-class functions (when functions in a language are treated like any other variable). <br>

**Variables** are containers for storing data (storing data values). All JavaScript variables must be identified with unique names. The unique names are called **identifiers**. General rules for naming:
- Can contain letters, digits, underscores, and dollar signs.
- Must begin with a letter. 
- Can also begin with $ and _.
- Case sensitive. 
- Reserved words (like JS keywords) cannot be used as names.

Ex. Short names: x, y. Descriptive names: age, sun, totalVolume)

**Four ways to declare a variable**:
1. Using `var`
    - Used in JavaScript code from 1995-2015. Must be used to run in older browser. 
2. Using `let`
    - If you think the value of a variable can change, use `let`.
3. Using `const`
    - General rule is to always declare variables with `const`. These are constant values and cannot be changed. `let` and `const` were added to JS in 2015.
4. Using `nothing`

**Assignment operator**: Equal sign (=) assigns the value and is not an "equal to" operator. 

**Types of variables**:
- **Numbers**: Whole numbers, like 30 (also called integers) or decimals, like 2.56 (also called floats or floating point numbers). Quotes are not included when declaring. 
    - Ex. `let myAge = 17;`
- **Strings**: Pieces of text. Needs to be wrapped in single or double quote marks. 
    - Ex. `let dolphinGoodbye = "So long and thanks for all the fish";
- **Booleans**: True/False values. Used to test a condition, after which code is run as appropriate. 
    - Ex. `let test = 6 < 3;` This will return `false`.
- **Arrays**: Single object that contains multiple values enclosed in square brackets and separated by commas. 
    - Ex. `let myNameArray = ["Stacy","Janaee","Marie"];` <br>
    `let myNumberArray = [10, 15, 25];`
- **Objects**: Structure of code that models a real-life object. 
    - Ex. `let cat = {name: "Maru", breed: "British Shorthair"};`<br>
    To retreive the information stored in the object, you can use the syntax: `cat.name`.


    [Back to main page](README.md)