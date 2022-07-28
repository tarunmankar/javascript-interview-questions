# JavaScript Interview Questions #

**1. What are the primitive data types in JS?**<br>
**Ans:** There are 7 primitive data types:
- string
- number
- boolean
- undefined
- null
- symbol (introduce in ES6)
- bigint (introduce in ES8)

---
**2. What is the difference between a variable that is: null, undefined or undeclared?**<br>
**Ans:** In JavaScript, undefined is a type, whereas null an object. It means a variable declared, but no value has been assigned a value. Whereas, null in JavaScript is an assignment value. You can assign it to a variable.

---
**3. What is the difference between while and do-while loops in JavaScript?** <br>
**Ans:** A while loop is a control flow statement that allows code to be executed repeatedly based on a given Boolean condition. The while loop can be thought of as a repeating if statement.

*Syntax:*
```
while (boolean condition)
{
`   `loop statements...
}
```
do while loop is similar to while loop with the only difference that it checks for the condition after executing the statements, and therefore is an example of Exit Control Loop.

*Syntax:*
```
do
{
`    `statements..
}
while (condition);
```
---
**4. What language constructions do you use for iterating over object properties and array items?**<br>
**Ans:**  for loop, for..in, foreach..in, map, reduce etc.

---
**5. What are IIFEs and explain with an example where they can be used?**<br>
**Ans:** An Immediately-invoked Function Expression (IIFE for friends) is a way to execute functions immediately, as soon as they are created. IIFEs are very useful because they don't pollute the global object, and they are a simple way to isolate variables declarations.

---
**6. What are the promises and how do they work?**<br>
**Ans:**  A promise is an object that may produce a single value sometime in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.

```
const wait = time => new Promise((resolve) => setTimeout(resolve, time));
wait(3000).then(() => console.log('Hello!')); // 'Hello!'
```
---
**7. Explain event delegation.**<br>
**Ans:** Event delegation refers to the process of using event propagation (bubbling) to handle events at a higher level in the DOM than the element on which the event originated. It allows us to attach a single event listener for elements that exist now or in the future.

---
**8. Explain how this works in JavaScript. Can you give an example of one of the ways that working with this has changed in ES6?**<br>
**Ans:** In JavaScript, the this keyword refers to an object. Which object depends on how this is being invoked (used or called). The this keyword refers to different objects depending on how it is used: In an object method, this refers to the object.

---
**9. Explain how prototypal inheritance works.**<br>
**Ans:** The Prototypal Inheritance is a feature in javascript used to add methods and properties in objects. It is a method by which an object can inherit the properties and methods of another object. Traditionally, in order to get and set the [[Prototype]] of an object, we use Object. getPrototypeOf and Object.

---
**10. What is a closure, and how/why would you use one?**<br>
**Ans:** A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function.

```
function init() {
var name = 'Mozilla'; // name is a local variable created by init
function displayName() {
      // displayName() is the inner function, a closure
      console.log(name); // use variable declared in the parent function
  }
 displayName();
}
init();
```
---

**11. Can you describe the main difference between the Array.forEach() loop and Array.map() methods and why you would pick one versus the other?**<br>
**Ans:** The forEach() method does not create a new array based on the given array. The map() method creates an entirely new array.

---
**12. What's a typical use case for anonymous functions?** <br>
**Ans:**  An anonymous function is a function that does not have any name associated with it. Normally we use the function keyword before the function name to define a function in JavaScript, however, in anonymous functions in JavaScript, we use only the function keyword without the function name.

---
**13. What's the difference between host objects and native objects?**<br>
**Ans:**  Native objects are objects that adhere to the specs, i.e. "standard objects". Host objects are objects that the browser (or other runtime environment like Node) provides.

---
**14. Explain the difference between: function Person(){}, var person = Person(), and var person = new Person()?**<br>
**Ans:** Technically speaking, function Person(){} is just a normal function declaration. The convention is to use PascalCase for functions that are intended to be used as constructors. var person = Person() invokes the Person as a function, and not as a constructor. var person = new Person() creates an instance of the Person object using the new operator, which inherits from Person.prototype.

---
**15. Explain the differences on the usage of foo between function foo() {} and var foo = function() {}**<br>
**Ans:** Normal Function or Function Declaration: Here foo is the function name.

```
function foo() {
    // Function Body
} 
```
Anonymous Function or Expression Function: Here the function is stored in the variable foo using var.
```
var foo = function() {
      // Function Body
}
```
---
**16. Can you explain what Function.call and Function.apply do? What's the notable difference between the two?**<br>
**Ans:**   The call() method takes arguments separately.
`         `The apply() method takes arguments as an array.

---
**17. Explain Function.prototype.bind.**<br>
**Ans:** prototype. bind() The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

---
**18. What's the difference between feature detection, feature inference, and using the UA string?**<br>
**Ans:** Feature detection checks a feature for existence, e.g.:

```
if (window.XMLHttpRequest) {
        new XMLHttpRequest();
}
```

Feature inference checks for a feature just like feature detection, but uses another function because it assumes it will also exist, e.g.:

```
if (document.getElementsByTagName) {
     element = document.getElementById(id);
}
```

Checking the UA string is an old practice and should not be used anymore. You keep changing the UA checks and never benefit from newly implemented features, e.g.:

```
if (navigator.userAgent.indexOf("MSIE 7") > -1){
     //do something
}
```
---

**19. Explain "hoisting".**<br>
**Ans:** Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables or classes to the top of their scope, prior to execution of the code. Hoisting allows functions to be safely used in code before they are declared.

---
**20. Describe event bubbling.**<br>
**Ans:** Event bubbling is a type of event propagation where the event first triggers on the innermost target element, and then successively triggers on the ancestors (parents) of the target element in the same nesting hierarchy till it reaches the outermost DOM element or document object (Provided the handler is initialized).

---
**21. Describe event capturing.**<br>
**Ans:** Event capturing is one of two ways to do event propagation in the HTML DOM. In event capturing, an event propagates from the outermost element to the target element. It is the opposite of event bubbling, where events propagate outwards from the target to the outer elements. Capturing happens before bubbling.

---
**22. What's the difference between an "attribute" and a "property"?.** <br>
**Ans:** An attribute is a quality or character ascribed to or considered to belong to, or be inherent in, a person or thing. A property is a quality or characteristic belonging to a person or thing, with its original use implying ownership, and also either being essential or special.

---
**23. What are the pros and cons of extending built-in JavaScript objects?**<br>
**Ans:** Extending Object.prototype is troublesome, since this is the "mother object". Extending the Object constructor itself isn't as bad, but not the best practice. The best solution, just create your own namespace:

var MY = {};
MY.clone = function(){};

---
**24. What is the difference between == and ===?**<br>
**Ans:** == Return true only if the two operands are equal while === returns true only if both values and data types are the same for the two variables.

---
**25. Explain the same-origin policy with regards to JavaScript.**<br>
**Ans:** The same-origin policy is a critical security mechanism that restricts how a document or script loaded by one origin can interact with a resource from another origin. It helps isolate potentially malicious documents, reducing possible attack vectors.

---
**26. Why is it called a Ternary operator, what does the word "Ternary" indicate?**<br>
**Ans:** The name ternary refers to the fact that the operator takes three operands. The condition is a boolean expression that evaluates to either true or false.

---
**27. What is strict mode? What are some of the advantages/disadvantages of using it?**<br>
**Ans:** Strict mode throws more errors and disables some features in an effort to make your code more robust, readable, and accurate.

---
**28. What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?**<br>
**Ans:** <br>
***Advantages of JavaScript*** :

- Speed. Client-side JavaScript is very fast because it can be run immediately within the client-side browser. Unless outside resources are required, JavaScript is unhindered by network calls to a backend server.
- Simplicity. JavaScript is relatively simple to learn and implement.
- Popularity. JavaScript is used everywhere on the web.
- Interoperability. JavaScript plays nicely with other languages and can be used in a huge variety of applications.
- Server Load. Being client-side reduces the demand on the website server.
- Gives the ability to create rich interfaces.

***Disadvantages of JavaScript :***
- **Client-Side Security:** Because the code executes on the users’ computer, in some cases it can be exploited for malicious purposes. This is one reason some people choose to disable Javascript.
- **Browser Support:** JavaScript is sometimes interpreted differently by different browsers. This makes it somewhat difficult to write cross-browser code.

---
**29. What tools and techniques do you use debugging JavaScript code?**<br>
**Ans:** Developer tools in modern web browsers. 
Every modern browser has tools available within it to debug code.
- The hackable debug tool — debugger.
- Node.
- Postman for debugging requests and responses.
- ESLint.
- JS Bin.
- JSON Formatter and Validator.
- Webpack.

---
**30. Explain the difference between mutable and immutable objects.**<br>
**Ans:** Objects whose value can change are said to be mutable. Objects whose value is unchangeable once they are created are called immutable.

`     `**a. What is an example of an immutable object in JavaScript?**<br>
The object being frozen is said to be immutable because the entire object state (values and   references to other objects) within the whole object is fixed. Note that strings, numbers,  and booleans are always immutable and that Functions and Arrays are objects.

`     `**b. What are the pros and cons of immutability?**<br>
Programs with immutable objects are less complicated to think about, since you don't need to worry about how an object may evolve over time. You don't need to make defensive copies of immutable objects when returning or passing to other functions, since there is no possibility an immutable object will be modified behind your back.

`     `**c. How can you achieve immutability in your own code?**<br>
Mutable objects are those whose state is allowed to change over time. An immutable value is the exact opposite — after it has been created, it can never change. Strings and Numbers are inherently immutable in javascript.

---
**31. Explain the difference between synchronous and asynchronous functions.**<br>
**Ans:** The differences between asynchronous and synchronous include: Async is multi-thread, which means operations or programs can run in parallel. Sync is single-thread, so only one operation or program will run at a time. Async is non-blocking, which means it will send multiple requests to a server.

---
**32. What is an event loop?** **What is the difference between call stack and task queue?**<br>
**Ans:** JavaScript has a runtime model based on an event loop, which is responsible for executing the code, collecting and processing events, and executing queued sub-tasks. This model is quite different from models in other languages like C and Java. A job queue is a queue of things to do (usually stored persistant) and a call stack is a stack of routines. A job would have variables assigned to it, and a call stack would be the abstract implementation. So a job could "call" a method from a call stack.

---
**33. What are the differences between variables created using let, var or const?**<br>
**Ans:**  Before the advent of ES6, var declarations ruled. There are issues associated with variables declared with var, though. That is why it was necessary for new ways to declare variables to emerge. With the ES6, they introduce let and const. Let is used when there we want to change the value of variable after a time and const is a costant in JS.

---
**34. What are the differences between ES6 class and ES5 function constructors?**<br>
**Ans:** 
- ES6 class basically does the work of defining a new object and appending functions to its prototype.
- ES5 Function constructors work and look the same but the main difference is observed when the developer uses the Inheritance property.

---
**35. Can you offer a use case for the new arrow => function syntax? How does this new syntax differ from other functions?**<br>
**Ans:** 
- Arrow functions shine best with anything that requires this to be bound to the context, and not the function itself.
- Despite the fact that they are anonymous, I also like using them with methods such as map and reduce, because I think it makes my code more readable. To me, the pros outweigh the cons.

---
**36. What advantage is there for using the arrow syntax for a method in a constructor?**<br>
**Ans:** Arrow syntax binds this to the surrounding code which makes the code simpler and shorter.

---
**37. What is the definition of a higher-order function?**<br>
**Ans:** A higher order function is a function that takes a function as an argument, or returns a function. Higher order function is in contrast to first order functions, which don’t take a function as an argument or return a function as output.

---
**38. Can you give an example for destructuring an object or an array?**<br>
**Ans:** 
```
const colorArr = ["red", "yellow", "blue", "green", "white", "black"];
const [first, second] = colorArr;
console.log(first, second);
// red, yellow
```

**39. Can you give an example of generating a string with ES6 Template Literals?**<br>
**Ans:**

```
var name = 'World';
var cname = 'javaTpoint';
console. log(`Hello, ${name}!
Welcome to ${cname}`);
```

**40. Can you give an example of a curry function and why this syntax offers an advantage?**<br>
**Ans:** 

```
const sum = x => y => x + y;
// returns the number 3

sum (2)(1);
// returns a function y => 2 + y

sum (2);
// Note that sum (2)(1); produces the same result that we would get, if we had defined it as const sum = (x,y) => x + y;, which we would call as 

sum (2, 1);
```
---

**41. What are the benefits of using spread syntax and how is it different from rest syntax?**<br>
**Ans:** Rest syntax looks exactly like spread syntax. In a way, rest syntax is the opposite of spread syntax. Spread syntax "expands" an array into its elements, while rest syntax collects multiple elements and "condenses" them into a single element.

---

**42. How can you share code between files?**<br>
**Ans:** 
- Create JavaScript files that export code in the same folder as the component importing the code. Import the code using a relative path. ...

- Create a service component (library), which is a component folder that contains one or more JavaScript files that export code.

---
**43. Why you might want to create static class members?**<br>
**Ans:** The advantage of using a static class is that the compiler can check to make sure that no instance members are accidentally added. The compiler will guarantee that instances of this class cannot be created. Static classes are sealed and therefore cannot be inherited. They cannot inherit from any class except Object.

---
