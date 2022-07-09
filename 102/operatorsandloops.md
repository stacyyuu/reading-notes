# JavaScript: Operators and Loops
**6/25/22** 
### Today, in Code 102 we learned how how to use Operators and Loops in JavaScript. 

---
# <u>OPERATORS</u>:
<br>
**Assignment Operators**: Assigns a value to its left operand based on the value of its right operand. 

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

| **Bitwise Assignment Operator**            |          **Function** |
| :---: | :---: |
| `&=` | AND |
| `|` | OR |
| `^=` | XOR |
| `<<` | Left shift|
| `>>` | Right shift |
| `>>>` | Unsigned right shift |


| **Logical Assignment Operator**            |          **Function** |
| :---: | :---: |
| `&&=` | AND |
| `||=` | OR |
| `??=` | XOR |

**Comparison Operators**: Compares its operands and returns a logical value based on whether the comparison is true. Operands can be numerical, string, logical, or object values. 
- Strings are compared based upon standard lexicographical ordering, using Unicode values. In most cases, if two operans are not of the same type, JS attempts to convert them into appropriate type of comparison. Generally results in comparing the operands numerically. The sole exceptions are the strict operators. 

| **Comparsion Operator**  |          **Function** |
| :---: | :---: |
| `==` | Equal to, returns `true` if operands are equal |
| `===` | Strict equal, returns `true` if operands are equal and same type |
| `!=` | Not equal |
| `!==` | Strict not equal |
| `>` | Greater than |
| `<`| Less than |
| `>=` | Greater than or equal to|
| `<=` | Less than or equal to |
| `?`| Ternary operator |

<br>
<br>
# <u>LOOPS</u>:

**Loops** offer a quick and easy way to do something repeatedly, for some number of time. 

1. `for` statement: repeats until specified condition evaluates false. Similar to Java and C `for` loop. 
- `for ([initialExpression]; [conditionExpression]; [incrementExpression])` <br>
 | `statement`
- The initializing expression `initialExpression`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
- The `conditionExpression expression` is evaluated. If the value of `conditionExpression` is true, the loop statements execute. Otherwise, the `for` loop terminates. (If the `conditionExpression` expression is omitted entirely, the condition is assumed to be true.)
- The `statement` executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.
- If present, the update expression incrementExpression is executed.
- Control returns to Step 2.
<br>
<br>
2. `do.. while` statement: repeats until a specified condition evaluates false. 
- `do`<br>
    |  `statement`<br>
`while (condition);`
- `statement` is always executed once before the condition is checked. (To execute multiple statements, use a block statement `({ ... })` to group those statements.)
- If `condition` is `true`, the statement executes again. At the end of every execution, the condition is checked. When the condition is `false`, execution stops, and control passes to the statement following `do...while`.
<br>
<br>
3. `while` statement: executes its statements as long as a specified condition evaluates `true`. 
- `while (condition)` <br>
  `statement`
- If the *`condition`* becomes `false`, `statement` within the loop stops executing and control passes to the statement following the loop.
- The condition test occurs *before* `statement` in the loop is executed. If the condition returns `true`, `statement` is executed and the *`condition`* is tested again. If the condition returns `false`, execution stops, and control is passed to the statement following `while`.
- To execute multiple statements, use a block statement `({ ... })` to group those statements.
<br>
<br>
4. `labeled` statement: provides statement with an identifer that lets you refer to it elsewhere in a program. You can use a label to identify a loop, then use `break` or `continue` statements to indicate whether a program should interupt loop or continue its execution. 
- `label :` <br>
   `statement`
- The value of `label` may be any JavaScript identifier that is not a reserved word. The `statement` that you identify with a label may be any statement.
<br>
<br>

[Back to main page](README.md)