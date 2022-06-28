# Programming with JavaScript
**6/27/22** 
### Today, in Code 102 we were introduced to Functions and Operators used in JavaScript 

---

**Control Flow**: Order in which the computer executes statements in script. Code runs in order from first line in the file to last, unless the computer runs across structures that change the control flow, such as conditionals and loops (extremely frequent).

**Functions**: Block of code deisgned to perform a particular tasks. Executed when "something" involes it (calls it).
`function myFunction(p1, p2) {` <br>
 `return p1 * p2;   // The function returns the product of p1 and p2` <br>
`}`

**Function Syntax**: Defined with `function` keyword, followed by a name, followed by paratheses (). Function names can contain letters, digits, underscores, and dollar signs (same rules as variables). The paratheses can contain paramenter names separated by commas:
<br>`function name(parameter 1, parameter 2, parameter 3) {` <br>
`// code to be executed` <br>
`}`
- Function **parameters** are listed inside the parentheses ().
- Function **arguments** are the **values** received by the function when it is invoked. 
- Inside the function, the arguments (the parameters) behave as local variables. 
- Similar to Procedure or Subroutine in other programming languages. 

**Function Invocation**: Code inside the function will execute when "something" **invokes** (calls) the function:
- When an event occurs (user clicks a button).
- When it is invoked (called) from JS code. 
- Automatically (self invoked). 
- Using () operator invokes the function, otherwise it will return the function object instead of result. 

**Function Return**: When JS reaches `return` statement, the function will stop executing. 
- If function was invoked from statement, JS will "return" to execute code after invoking statement. 
- Functions often compute a **return value**. Return value is "returned" back to "caller":
<br>`let x = myFunction(4, 3);   // Function is called, return value will end up in x` <br>
`function myFunction(a, b) {`<br>
 ` return a * b;             // Function returns the product of a and b` <br>
`}`
<br>The result in x will be `12`.

**Why Functions?**:
- You can reuse code: Define code once and use it many times. 
- You can use the same code many times with different arguments, to produce different results. 

**Functions as Variable Values**: Functions can be used the same way as variables, in all types of formulas, assignments, and calculations. 
<br> `let text = "The temperature is " + toCelsius(77) + " Celsius";`

**Local Variables**: Variables declared within JS function, become **LOCAL** to the function. Local variables can only be accessed from within the function. 
<br> `function myFunction() {` <br>
  `let carName = "Volvo";`

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

| **Comparsion Operator**            |          **Function** |
| :---: | :---: |
| `==` | Equal to |
| `===` | Equal to and equal type |
| `!=` | Not equal |
| `!==` | Not equal to and not equal type|
| `>` | Greater than |
| `<`| Less than |
| `>=` | Greater than or equal to|
| `<=` | Less than or equal to |
| `?`| Ternary operator |

| **Logical Operator**            |          **Function** |
| :---: | :---: |
| `&&` | Logical and |
| `||` | Logical or |
| `!` | Logical not |

<br> Bit operators work on 32 bits numbers. Any numeric operand in the operation is converted to a 32 bit number. The result is converted back to a JS number. 

| **Bitwise Operator**            |          **Function** |
| :---: | :---: |
| `&` | AND |
| `|` | OR |
| `~` | NOT |
| `^` | XOR |
| `<<` | Left shift|
| `>>` | Right shift |
| `>>>` | Unsigned right shift |


[Back to main page](README.md)