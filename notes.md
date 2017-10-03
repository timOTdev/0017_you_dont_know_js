## ["Up & Going" (Book 1)](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20&%20going/README.md#you-dont-know-js-up--going)
**[Table of Contents](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/toc.md)**
### [Foreword](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/foreword.md) (by [Jenn Lukas](http://jennlukas.com/)) ✔
### [Preface](https://github.com/getify/You-Dont-Know-JS/blob/master/preface.md) ✔
### [Chapter 1: Into Programming](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/ch1.md) ✔
- Code
    - Syntax is the word for computer language
    - Statements are a group of words, numbers, and operators that performs a specific task
    - There are variables, literal values, and operators
    - Programs are a collection of many statments 
    - This statement has 4 expressions: literal value, variable, arithmetic, assignment
    ```
    a = b * 2;
    ```
    - JavaScript is an interpreted language meaning it is processed each time it runs
    - Other languages are compiled beforehand
      
- Try It Yourself
    - Use developer tools in the console of your browser to practice JavaScript
    - Use console.log() instead of alert() to output your results
    - Try out code examples:
    ```
    a = 21;
    b = a * 2;
    console.log(b);
    ```
    - We can also get input from the user
    ```
    var age = prompt('Please tell me your age:');
    console.log(age);
    ```
      
- Operators
    - Operators are how we perform operations on values and variables
    - Notice the source value is usually to the left of the = sign
    - We use "var" to declare variables
    - There are many operators including:
        - Assignment 
        - Math 
        - Compound assignment
        - Increment/decrement 
        - Object property access 
        - Equality 
        - Comparison 
        - Logical
          
- Values & Types
    - Primitive values or literals in your source code:
    - String
    - Number
    - Boolean value
      
- Converting between types      
    - **Coercion** is a conversion between the primitive values
    - There is explicit and implicit coercion
      
- Code Comments
    - Write comments to make your code easier to read by humans
    - There are single-line comments (using //) and multi-line comments (using /* and */)
    - Good rules to follow:
    1. Write some comments
    2. Don't write more than 2 comments per line
    3. Comments explain the why and how, not what
      
- Variables
    - Holds values that can be changed over time
    - There's dynamic typing (weak typing) which can hold any type of value
    - There's static typing (type enforcement) which can only hold certain types of values like numbers or strings
    - String() method converts values into strings and toFixed() methods converts numbers to 2 decimals
    - Typical constants use capital letters (IE var TAX_RATE) but ES6 now has const to declare variables that doesn't change
      
- Blocks
    - Blocks are when we see code inside {...}
    - Typically in JS, you'll see this within if...else statements
    - They do not need to end with a semicolon
      
- Conditionals
    - Uses if...else, loops, or switch statements
    - Will coerce values into Booleans
      
- Loops
    - There are do...while, while...do, and for loops
    - Difference between do...while vs while...do is that do...while tests the condition after the first iteration
    - For the for loop, there is the initation, conditional, and update clauses
      
- Functions
    - Has a name that can be called to run the code inside the function
    - Functions are useful if you plan to call the code multiple times, but okay to help organize and call only once also
- Scope
    - Lexical Scope is how variables have different degree of access
    - A variable inside of a function can access anything outside of that function
    - An inner function, nested within an outer function, can also access the variable in the outer function
```
function
 outer() {
    var a = 1;

    function inner() {
        var b = 2; // we can access both `a` and `b` here
        console .log( a + b ); // 3
    }
    inner(); // we can only access `a` here
    
    console.log( a ); // 1
} 
outer();    
```    
- Practice
    - Write a program to calculate the total price of your phone purchase.  You  will  keep  purchasing  phones  (hint:  loop!)  until  you
    run out of money in your bank account. You’ll also buy accessories  for  each  phone  as  long  as  your  purchase  amount  is  below
    your mental spending threshold.
    - After  you’ve  calculated  your  purchase  amount,  add  in  the  tax,
    then  print  out  the  calculated  purchase  amount,  properly  for‐
    matted.
    - Finally, check the amount against your bank account balance to
    see if you can afford it or not.
    - You  should  set  up  some  constants  for  the  “tax  rate,”  “phone
    price,”  “accessory  price,”  and  “spending  threshold,”  as  well  as  a
    variable for your “bank account balance.”
    - You should define functions for calculating the tax and for formatting  the  price  with  a  “$”  and  rounding  to  two  decimal
    places.
    - Bonus  Challenge:
    Try  to  incorporate  input  into  this  program, perhaps with the 
    prompt(..) covered in “Input” on page 6. You
    may prompt the user for their bank account balance, for example. Have fun and be creative!
    - My code:      
    ```
    const taxRate = 0.053;
    const phonePrice = 799;
    const phoneAcc = 20;
    var subtotal = "";
    var total = "";
    var bankBalance = prompt("What is your bank balance?");
    var spendThreshold = prompt("How much are you willing to spend on your new phone?");

    function calculate() {
        subtotal = phonePrice + (phonePrice * taxRate);

        var buyAcc = prompt("You total is: $" + subtotal.toFixed(2) + ". Would you like to buy a phone case? It's $20 dollars more. (Type yes or no)");

        if (buyAcc == "yes") {
            total = subtotal + phoneAcc;
            alert("Your grand total is: $" + total.toFixed(2));
        } else {
            total = subtotal;
            alert("Okay, Your grand total is: $" + total.toFixed(2));
        }

        function priceCheck() {
            if (bankBalance > total && spendThreshold > total) {
                alert("Okay, thanks for purchasing with us. Please come back again soon!");
            } else if (bankBalance > total && spendThreshold < total) {
                alert("Sorry, doesn't look like you are willing to spend $" + total.toFixed(2) + " for the phone. Your limit is: $" + spendThreshold + ".");
            } else if (bankBalance < total && spendThreshold > total) {
                alert("You got the want ($" + total + ") but you don't got the funds ($" + bankBalance + ")!");
            } else {
                alert("You are poor. You have only have $" + bankBalance + " to your name. Go home.");
            }
        }
        priceCheck();
    }
	calculate();    
    ```      

### [Chapter 2: Into JavaScript](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/ch2.md)
- Values & Types
- Variables
- Conditionals
- Strict Mode
- Functions As Values
- this Keyword
- Prototypes
- Old & New
- Non-JavaScript
### [Chapter 3: Into YDKJS](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/ch3.md)
- Scope & Closures
- this & Object Prototypes
- Types & Grammar
- Async & Performance
- ES6 & Beyond
### [Appendix A: Thank You's!](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/apA.md)