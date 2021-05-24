# HTML - Lists
**HTML offers web authors three ways for specifying lists of information. All lists must contain one or more list elements. Lists may contain**
- <ul> − An unordered list. This will list items using plain bullets.

- <ol> − An ordered list. This will use different schemes of numbers to list your items.

- <dl> − A definition list. This arranges your items in the same way as they are arranged in a dictionary.


## HTML Unordered Lists
An unordered list is a collection of related items that have no special order or sequence. This list is created by using HTML <ul> tag. Each item in the list is marked with a bullet.

ExampleL :
> <!DOCTYPE html>
<html>

   <head>
      <title>HTML Unordered List</title>
   </head>
	
   <body>
      <ul>
         <li>Beetroot</li>
         <li>Ginger</li>
         <li>Potato</li>
         <li>Radish</li>
      </ul>
   </body>
   
</html>
 ## The type Attribute 
You can use type attribute for <ul> tag to specify the type of bullet you like. By default, it is a disc. Following are the possible options −

<ul type = "square">
<ul type = "disc">
<ul type = "circle">

## HTML Ordered Lists
If you are required to put your items in a numbered list instead of bulleted, then HTML ordered list will be used. This list is created by using <ol> tag. The numbering starts at one and is incremented by one for each successive ordered list element tagged with <li>.

Example
><!DOCTYPE html>
<html>

   <head>
      <title>HTML Ordered List</title>
   </head>

   <body>
      <ol>
         <li>Beetroot</li>
         <li>Ginger</li>
         <li>Potato</li>
         <li>Radish</li>
      </ol>
   </body>

</html>
 
## HTML Definition Lists
*HTML and XHTML supports a list style which is called definition lists where entries are listed like in a dictionary or encyclopedia. The definition list is the ideal way to present a glossary, list of terms, or other name/value list.

Definition List makes use of following three tags.*

<dl> − Defines the start of the list
<dt> − A term
<dd> − Term definition
  

  
 # The CSS Box Model
**In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content
>The box model allows us to add a border around elements, and to define space between elements. 

Example
Demonstration of the box model:

div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}

# Width and Height of an Element
**In order to set the width and height of an element correctly in all browsers, you need to know how the box model works.

Important: When you set the width and height properties of an element with CSS, you just set the width and height of the content area. To calculate the full size of an element, you must also add padding, borders and margins.

Example
>
This <div> element will have a total width of 350px: 

div {
  width: 320px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
Here is the calculation:
320px (width)
+ 20px (left + right padding)
+ 10px (left + right border)
+ 0px (left + right margin)
= 350px

**The total width of an element should be calculated like this:

**Total element width = width + left padding + right padding + left border + right border + left margin + right margin

**The total height of an element should be calculated like this:

**Total element height = height + top padding + bottom padding + top border + bottom border + top margin + bottom margin

# What is JavaScript?
**JavaScript ("JS" for short) is a full-fledged dynamic programming language that can add interactivity to a website. It was invented by Brendan Eich (co-founder of the Mozilla project, the Mozilla Foundation, and the Mozilla Corporation).

JavaScript is versatile and beginner-friendly. With more experience, you'll be able to create games, animated 2D and 3D graphics, comprehensive database-driven apps, and much more!

JavaScript itself is relatively compact, yet very flexible. Developers have written a variety of tools on top of the core JavaScript language, unlocking a vast amount of functionality with minimum effort. These include:

Browser Application Programming Interfaces (APIs) built into web browsers, providing functionality such as dynamically creating HTML and setting CSS styles; collecting and manipulating a video stream from a user's webcam, or generating 3D graphics and audio samples.
Third-party APIs that allow developers to incorporate functionality in sites from other content providers, such as Twitter or Facebook.
Third-party frameworks and libraries that you can apply to HTML to accelerate the work of building sites and applications.
It's outside the scope of this article—as a light introduction to JavaScript—to present the details of how the core JavaScript language is different from the tools listed above.
You can learn more in MDN's JavaScript learning area, as well as in other parts of MDN.

Decisions and Loops
Refer to previous lessons for review.
Welcome back to our tutorial, in this lesson, we will be exploring how to control the flow of your program using conditional statements and loops. Here are the concepts that we will be using:

If statements - If a condition is true, then run the code in that block.
If...Else statements - If a condition is true, then run the code in that block. Otherwise, run the code in the else block.
For loops - Run the code in this block based on a set number of iteration. This is known.
While loops - Run the code in this block while a condition is true. The number of iterations is unknown.
For this lesson, it requires 4 files:

worklog.html - This file is where we only keep our div with id worklog and we will only link to three external scripts.
Employer.js - An external script with the function Employer() class.
Employee.js - An external script with the function Employee() class.
output.js - An external script that we will use to set up our output div, our instantiations, and call functions.
In lesson 2, we have made a workers.js file. We will break this up into two files, Employer.js and Employee.js. Migrate the Employer function to Employer.js and Employee function to Employee.js and then delete the workers.js file. We want to separate the files by classes.

worklog.html
The only thing that we need to do for this file is to link the three scripts. Same process as we used in lesson 2.

output.js
Erase everything except the first two lines in this file, we will revisit this file later.

Let's get started!

Before we get started, we will need to make more assumptions and write new functions inside Employer and Employee. Both of these files should be open.

Variables
In both the Employer.js and Employee.js files, insert the following variables:

var didWork = false; //If the worker worked today
var hoursWorkedToday = 0.00; // How many hours the worker worked today
var hourlyWage = salary / 52 / 40; //The worker's hourly wage
var maxWorkHours = 8.00; // Maximum of hours that can be worked
Add the following variable in Employee.js file:

var isFullTime = true; //If the employee is full time or part time
If and If...Else statements
Recall that in lesson 2, because JavaScript is "loosely-typed", I can instantiate the Employer function without any parameters and the code continues as normal. What we would like to do in both the Employer and Employee class is require that the user inputs a name. To do this, we will need to make some decisions. This is a skeleton of the if...else statement

if (condition) {
 
} else {
 
}
Our condition should be evaluated as either true or false. Here is how we want the program to flow in the Employer function.

If the parameter is a string type, nothing happens.
Anything else, we will stop the script and throw an error. We will also alert the user showing a message.
There are three tools that you will need to accomplish this:

typeof Operator - This will return either string, number, boolean, object, function, or undefined
throw new Error() - The script will stop and will output a message to the console. The console can be accessed by hitting the F12 key.
alert() - Unlike throw new error, the message inside will display to the user in a gray message box.
*Note - You can have multiple parameters when you instantiate your Employer function, but this code cares about the first parameter, all other parameters are ignored.

We will also need 6 relational operators for our condition:

(==) - equal to - Compares two items to see if they are equal
(!=) - not equal to - Compares two items to see if they are not equal
(>) - greater than - Compares the first item to see if it is greater than the second item
(<) - less than - Compares the first item to see if it is less than the second item
(>=) - greater than or equal to - Compares the first item to see if it is greater than or equal to the second item
(<=) - less than or equal to - Compares the first item to see if it is less than or equal to the second item
We now have everything to write the if...else statement, let's do it.

if (typeof n == "string") {
 
} else {
    alert("function Employer requires a string");
    throw new Error("function Employer requires a string");
}
  
  
  
  
  
  
  
  
