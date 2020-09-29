VARIABLES LAB
==================
**NOTE**: *The first portion of class and the code-along covers how to do this, so you can scroll down to the bottom to see the tasks. This document is meant for a reference when needed.*

In computer science, **variables** are containers for storing data values that we can update as our program runs. We declare a variable using the `var` **once** and assign it a value using the assignment operator (`=`).

```javascript
var price1 = 5;
var price2 = 6;
price1 = 10
var total = price1 + price2; // total stores the value of 15
```

Variables can store integers, floats (decimal numbers), strings, or boolean (true/false) values. Additionally, you can store the output of mathematical operations (like the example with `total` above. The basic math operators for JavaScript are: 

Operation | Symbol|
------------ | -------------
Add| `+` | 
Subtract | `-`|
Multiply | `*`|
Divide | `/`| 
Exponent | `**`|

One of the things we often want to do is to increment or decrement a variable. For example:
```javascript
var sum = 10;
sum++;
sum++;
sum++;
```
The final value of sum is 13 as the `++` operator adds one each time it is used. The reverse is also true with the `--` operator.

Suppose we wanted to decrease (or increase) the value of a variable by a number other than one, how would we do this? We can use the `+=` or `-=` operators for this:
```javascript
var decrease = 20;
decrease -= 10;
decrease -=10;
```
The final value of `decrease` is 0 beacuse -= removes 10 from the original value twice.

`innerHTML`
--------------
Now that we have variables that store information, we want to be able to change and update our HTML page with values of our varaibles. We can accomplish this by using `innerHTML`. 

The `innerHTML` property sets or returns the HTML content of an element.
```javascript
var header = document.querySelector("#myHeader");
// Returns the HTML contained inside the html element with this ID
console.log(header.innerHTML)
```
We can also use `innerHTML` to update the HTML on a page.
```javascript
var text = document.querySelector("#text");
// Updates the text container to contain the word CLICKED when it is clicked.
text.addEventListener("click", function(){
  text.innerHTML = `<h1>CLICKED</h1>`
})
```
**NOTE**: The ` symbol is above the tab button and next to the one key. You can use normal quotation marks instead, but will not be able to style using html tags if you do.

CONCATINATION
--------------
In JavaScript, we can assign strings to a variable and use concatenation to combine the variable to another string.

To concatenate a string, we can do this in one of two ways. 
1. You can add a `+` between the strings or string variables you want to connect.
```javascript
var myPet = "seahorse";
console.log('My favorite animal is the ' + myPet + '.'); 
// This will print: My favorite animal is the seahorse.
```
2. You can also use backticks (`) and the notation ${ } with the variable name going between the brackets.
```javascript
var myPet = "seahorse";
console.log(`My favorite animal is the ${myPet}`);
// This will print: My favorite animal is the seahorse.

```
TODAY'S TASKS
--------------
1. **CHALLENGE 1**: Have the div with an id of `#text` update with the word "CLICKED" when the user clicks the div.  
![](https://media.giphy.com/media/SWVvSghZq06AwpCKLD/giphy.gif). 

2. **CHALLENGE 2**: Create a variable that contains any number. Update the second div with that variable when clicked. Bonus points if you can make it an `<h2>` and use `${}`.  
![](https://media.giphy.com/media/hWRPlCho1aQSwZR1go/giphy.gif)

3. **CHALLENGE 3**: Update the third div with your name when your mouse is over the div.  
![](https://media.giphy.com/media/QUMJz37ERU3a2Hdm1m/giphy.gif)

4. **CHALLENGE 4**: Increase a number by 1 every time the 4th div is clicked. Bonus points if you can make it an h2 and use ${}. Double triple bonus points if you can get the number to reset when the mouse LEAVES the div.
**HINT**: You will need to declare a counter variable that is updated everytime the div is clicked.  
![](https://media.giphy.com/media/JrB6MwsqVrN766OEsG/giphy.gif)

5. **CHALLENGE 5**: Decrease a number by 3 every time the mouse moves inside the 5th div.  
![](https://media.giphy.com/media/KBDyTcJJ8sNtnir4MN/giphy.gif)

6. **CHALLENGE 6**: Create two variables. One to store your age and and another to store your name. String together your name and counter variables here using concatenation when mouse is pressed on the 6th div.  
![](https://media.giphy.com/media/f9qtdLSrGRUcrDEUce/giphy.gif)