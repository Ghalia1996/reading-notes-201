#Introduction to links and anchors

**HTML offers many of the conventional publishing idioms for rich text and structured documents, but what separates it from most other markup languages is its features for hypertext and interactive documents. This section introduces the link (or hyperlink, or Web link), the basic hypertext construct. A link is a connection from one Web resource to another. Although a simple concept, the link has been one of the primary forces driving the success of the Web.

A link has two ends -- called anchors -- and a direction. The link starts at the "source" anchor and points to the "destination" anchor, which may be any Web resource (e.g., an image, a video clip, a sound bite, a program, an HTML document, an element within an HTML document, etc.)**

#Visiting a linked resource

*The default behavior associated with a link is the retrieval of another Web resource. This behavior is commonly and implicitly obtained by selecting the link (e.g., by clicking, through keyboard input, etc.).

The following HTML excerpt contains two links, one whose destination anchor is an HTML document named "chapter2.html" and the other whose destination anchor is a GIF image in the file "forest.gif":*
 Thus, for example, an author might create a table of contents whose entries link to header elements H2, H3, etc., in the same document. Using the A element to create destination anchors, we would write:
 ><H1>Table of Contents</H1>
<P><A href="#section1">Introduction</A><BR>
<A href="#section2">Some background</A><BR>
<A href="#section2.1">On a more personal note</A><BR>
...the rest of the table of contents...
...the document body...
<H2><A name="section1">Introduction</A></H2>
...section 1...
<H2><A name="section2">Some background</A></H2>
...section 2...
<H3><A name="section2.1">On a more personal note</A></H3>
...section 2.1...
*We may achieve the same effect by making the header elements themselves the anchors:*
><H1>Table of Contents</H1>
<P><A href="#section1">Introduction</A><BR>
<A href="#section2">Some background</A><BR>
<A href="#section2.1">On a more personal note</A><BR>
...the rest of the table of contents...
...the document body...
<H2 id="section1">Introduction</H2>
...section 1...
<H2 id="section2">Some background</H2>
...section 2...
<H3 id="section2.1">On a more personal note</H3>
...section 2.1...

#HTML Layout Elements
HTML has several semantic elements that define the different parts of a web page:

#HTML5 Semantic Elements	
<header> - Defines a header for a document or a section
<nav> - Defines a set of navigation links
<section> - Defines a section in a document
<article> - Defines an independent, self-contained content
<aside> - Defines content aside from the content (like a sidebar)
<footer> - Defines a footer for a document or a section
<details> - Defines additional details that the user can open and close on demand
<summary> - Defines a heading for the <details> element

#HTML Layout Techniques
There are four different techniques to create multicolumn layouts. Each technique has its pros and cons:

CSS framework
CSS float property
CSS flexbox
CSS grid
Article
Methods and Functions
Use this article as a reference sheet for JavaScript methods and functions.
Use this article as a reference sheet for JavaScript methods and functions.

Function — a set of instructions that perform a task.
Method — a set of instructions that are associated with an object.
Functions
Functions are like recipes. They can execute a set of instructions on data or variables and return the result. The beauty of functions is that they are recyclable. That is, the function can be used repeatedly without having to write the same code again.

// Define a function that prints a string
function welcomeMessage() {
  console.log('Welcome to JavaScript');
}
// Call the function
welcomeMessage();
In the example above, the welcomeMessage function is used to display Welcome to JavaScript in the console. Let’s walk through this code step-by-step:

The function keyword indicates the start of a function.
The word that follows (welcomeMessage) is the function’s name.
The empty parentheses after welcomeMessage indicate that there are no parameters, or inputs, for the function.
The code between the opening ({) and closing (}) curly braces is a set of instructions. This code will only execute when the function is called.
To call a method, you need the function’s name, a pair of parentheses, and a semicolon. In this example, the function is called with welcomeMessage();.
Let’s also consider a function that receives inputs and returns outputs:

function concatName(firstName, middleName, lastName) {
  return firstName + ' ' + middleName + ' ' + lastName;
}
Let’s walk through this example step-by-step:

The concatName function is created with three parameters (inputs): firstName, middleName, and lastName. Think of these as variables that have not been set yet.
Inside of the function, the return keyword will return the concatenation of firstName, middleName, and lastName, with spaces in between each. The return keyword terminates the function it is within, and returns a value — any code inside the function that comes after the return keyword will not be evaluated (nor executed, itself).
You can save the returned string to a variable or log it to the console when you call the function.
var concatGWC = concatName('George', 'Washington', 'Carver');
In the example above, the concatName function is called with the following arguments: 'George', 'Washington', and 'Carver'. These values are saved into the variables firstName, middleName, and lastName inside of the function. The function returns a concatenation of these three strings — the concatGWC variable stores the returned concatenated string.
In this reference sheet we have used the words parameters and arguments to reference similar, but distinctly different elements of a function and function call. What’s the difference between these words?

Parameters are fields that serve as variable names inside of a function. In the example above, firstName, middleName, and lastName are parameters.
Arguments are the values passed to the function when it is called. In the example above, 'George', 'Washington', and 'Carver' are arguments.
Methods
A method, like a function, is a set of instructions that perform a task. The difference is that a method is associated with an object, while a function is not. Let’s explore some of JavaScript’s built-in methods.

var str = 'CodeCADEMY';
var str1 = str.toLowerCase();
var str2 = str.toUpperCase();
The variable str in the example above stores the string ‘CodeCADEMY’. The .toLowerCase() and .toUpperCase() methods in the example above are called on str. Let’s talk through each line:

On the second line, the .toLowerCase() method is called on the str variable, which returns the lowercase string 'codecademy'.
On the third line, the .toUpperCase() method is called on the str variable, which returns the uppercase string 'CODECADEMY'. Notice, periods are used to call a method on an object, as in str.toLowerCase();.

<article>: The Article Contents element
The HTML <article> element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.




