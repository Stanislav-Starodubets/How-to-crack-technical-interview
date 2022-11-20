# JavaScript Interview Questions

Number of questions: Total = 95; High = 50; Medium = 36; Low = 9.

## Table of Contents

### Week 1 (Questions with High priority)
Number of questions: High = 50.
Estimate: ~30m*50 = 25h / 5d = 5h per day.

| Index | No.   | Questions                                                                    | Priority |
|-------|-------|------------------------------------------------------------------------------|----------|
|       | **1** | **Data Types**                                                               |          |
| 1     | 1.1   | What are data types in javascript?                                           | High     |
|       |       | Seven primitive data types:<br/>--`number` for numbers of any kind: integer or floating-point, integers are limited by ±(253-1).<br/>--`bigint` for integer numbers of arbitrary length.<br/>--`string` for strings. A string may have zero or more characters, there’s no separate single-character type.<br/>--`boolean` for true/false.<br/>--`null` for unknown values – a standalone type that has a single value null.<br/>--`undefined` for unassigned values – a standalone type that has a single value undefined.<br/>--`symbol` for unique identifiers.<br/><br/>And one non-primitive data type:<br/>--`object` for more complex data structures.                                                                       |          |
| 2     | 1.2   | What are primitive data types?                                               | High     |
|       |       | Seven primitive data types:<br/>--`number` for numbers of any kind: integer or floating-point, integers are limited by ±(253-1).<br/>--`bigint` for integer numbers of arbitrary length.<br/>--`string` for strings. A string may have zero or more characters, there’s no separate single-character type.<br/>--`boolean` for true/false.<br/>--`null` for unknown values – a standalone type that has a single value null.<br/>--`undefined` for unassigned values – a standalone type that has a single value undefined.<br/>--`symbol` for unique identifiers.                                                                       |          |
| 3     | 1.3   | What is the differance between primitives vs objects?                        | High     |
|       |       | “primitive” because their values can contain only a single thing (be it a string or a number or whatever). In contrast, objects are used to store collections of data and more complex entities. <br/><br/>One of the fundamental differences of objects versus primitives is that objects are stored and copied “by reference”, whereas primitive values: strings, numbers, booleans, etc – are always copied “as a whole value”.                                                                       |          |
| 4     | 1.4   | What is coercion in JavaScript?                                              | High     |
|       |       | Type coercion is the process of converting value from one type to another (such as string to number, object to boolean, and so on). Any type, be it primitive or an object, is a valid subject for type coercion.                                                                       |          |
| 5     | 1.5   | Do you know what Autoboxing in JS is?                                        | High     |
|       |       | Whenever we try to access a method or property on a primitive, that primitive is wrapped into an object. That's called autoboxing. Autoboxing will connect the primitive to the related built-in prototype object.                                                                       |          |
| 6     | 1.6   | What is the difference between == and === operators?                         | High     |
|       |       | The main difference between the == and === operator in javascript is that the == operator does the type conversion of the operands before comparison, whereas the === operator compares the values as well as the data types of the operands                                                                       |          |
| 7     | 1.7   | What is undefined data type?                                                 | High     |
|       |       | The undefined datatype, whose value is undefined is used to denote an absence of a meaningful value. A variable in JavaScript that is without any value has a value of undefined.                                                                       |          |
| 8     | 1.8   | What is null value?                                                          | High     |
|       |       | The null value represents the intentional absence of any object value. The null value denotes nothingness. It is supposed to denote something that does not exist. A variable in JavaScript that has a null value is of the 'object' datatype.                                                                       |          |
| 9     | 1.9   | What does isNaN function do?                                                 | High     |
|       |       | The `isNaN()` function is used to check whether a given value is an illegal number or not. It returns true if value is a NaN else returns false. It is different from the Number.isNaN() <br/> - `Number.isNaN()` is almost identical to the function above, except it won’t try to coerce non-numbers to a number. It only returns true for the first three reasons why a NaN occurs, which are when Not a Number happens mathematically.                                                                   |          |
| 10    | 1.10  | What does NaN value mean?                                                    | High     |
|       |       | In JavaScript, NaN is short for "Not-a-Number". In JavaScript, NaN is a number that is not a legal number.                                                                       |          |
| 11    | 1.11  | What is the difference between null and undefined?                           | High     |
|       |       | `undefined` means a variable has been declared but has not yet been assigned a value <br/> `null` is an assignment value. It can be assigned to a variable as a representation of no value                                                                      |          |
|       | **2** | **Objects, Classes, Prototypal inheritance**                                 |          |
| 14    | 2.1   | How do you copy properties from one object to other?                         | High     |
|       |       | JavaScript offers standard inbuilt object-copy operations for creating shallow copies: Array.from(), Array.prototype.concat(), Array.prototype.slice(), Object.assign(), and Object.create(), spread syntax. Shallow copy can be used when we’re dealing with an object that only has properties with primitive data types (for example, strings or numbers).                                                                       |          |
| 15    | 2.2   | What are classes in ES6?                                                     | High     |
|       |       | Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes are in fact "special functions", and just as you can define function expressions and function declarations                                                                       |          |
| 16    | 2.3   | Explain how prototypal inheritance works?                                    | High     |
|       |       | In JavaScript, objects have a special hidden property [[Prototype]] (as named in the specification), that is either null or references another object. That object is called “a prototype”.<br/> When we read a property from object, and it’s missing, JavaScript automatically takes it from the prototype. In programming, this is called “prototypal inheritance”.                                                                      |          |
|       | **3** | **Context, Scope and Closure**                                               |          |
| 28    | 3.1   | How do you assign default values to variables?                               | High     |
|       |       | Default values can be set using the `OR(\|\|)`, the OR assignment `(\|\|=)`, the nullish coalescing `(??)`, or the nullish assignment `(??=)` operators. Functions allow `default values`. The default values are applied only when the provided arguments are missing or are set to undefined. The `destructuring assignment allows defaults.` The default values are applied only when the specified properties are missing or are set to undefined. The `\|\|` operator applies the default value when the provided value is falsy. The `??` operator applies the default value when the provided value is nullish.                                                                       |          |
| 29    | 3.2   | What is the difference between let, const and var?                           | High     | 
|       |       | var, let, and const are keywords that allow us to declare variables. Scope of a variable tells us where we can access this variable inside our code and where we can't. It is one of the decisive reasons for the difference between let and var and const in javascript. Hoisting provides features to hoist our variables and function declaration to the top of its scope before code execution. `var` is a nice and innocent way to declare a variable, which gets hoisted to the top of the scope. `let` and `const` are the modern ways to declare variables, which also get hoisted but don't initialize.                                                                       |          |
| 30    | 3.3   | What are the differences between undeclared and undefined variables?         | High     | 
|       |       | Undefined variable means a variable has been declared but does not have a value. Undeclared variable means that the variable does not exist in the program at all.                                                                       |          |
| 31    | 3.4   | What are global variables?                                                   | High     | 
|       |       | A global variable is a variable that is declared in the global scope in other words, a variable that is visible from all other scopes. In JavaScript it is a property of the global object.                                                                       |          |
| 32    | 3.5   | What is Hoisting?                                                            | High     |
|       |       | Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution. Inevitably, this means that no matter where functions and variables are declared, they are moved to the top of their scope regardless of whether their scope is global or local.                                                                       |          |
| 33    | 3.6   | What is scope in javascript?                                                 | High     |
|       |       | Scope in JavaScript refers to the current context of code, which determines the accessibility of variables to JavaScript. The two types of scope are local and global: Global variables are those declared outside of a block. Local variables are those declared inside of a block.                                                                       |          |
| 34    | 3.7   | What is the closure?                                                         | High     |
|       |       | A closure is a function having access to the parent scope, even after the parent function has closed                                                                       |          |
| 35    | 3.8   | How does closure implemented in the javascript?                              | High     |
|       |       | Closures or inner functions in javascript have access to its outer functions scope chain even after the outer function is returned.                                                                       |          |
| 36    | 3.9   | What is the difference between Call, Apply and Bind?                         | High     |
|       |       | `call`: binds the this value, invokes the function, and allows you to pass a list of arguments.<br/>`apply`: binds the this value, invokes the function, and allows you to pass arguments as an array.<br/>`bind`: binds the this value, returns a new function, and allows you to pass in a list of arguments.                                                                       |          |
| 37    | 3.10  | What does 'this loses context' mean?                                         | High     |
|       |       | The best was to think of this is not as an "execution context" (accurate, but unintuitive), or an "environment" (not really accurate). The way to think of this in JavaScript is as a slightly weird function parameter. Unlike a normal function parameter, it doesn't refer to whatever is between the parentheses, instead this refers to whatever is to the left of the dot. if there is nothing to the left of the dot, this becomes the global/window object                                                                       |          |
|       | **4** | **JSON**                                                                     |          |                                                                    
| 41    | 4.1   | What is JSON and its common operations?                                      | High     |
|       |       | JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax. It is commonly used for transmitting data in web applications (e.g., sending some data from the server to the client, so it can be displayed on a web page)                                                                       |          |
| 42    | 4.2   | How do you parse JSON string?                                                | High     |
|       |       | The JSON.parse() method parses a JSON string, constructing the JavaScript value or object described by the string.                                                                       |          |
| 43    | 4.3   | What is the purpose JSON stringify?                                          | High     |
|       |       | The JSON.stringify() method converts a JavaScript value to a JSON string, optionally replacing values if a replacer function is specified or optionally including only the specified properties if a replacer array is specified.                                                                       |          |
|       | **5** | **Array methods**                                                            |          |                                                                    
| 46    | 5.1   | What array methods do you know?                                              | High     |
|       |       | To add/remove elements:<br/><br/>push(...items) – adds items to the end,<br/><br/>pop() – extracts an item from the end,<br/><br/>shift() – extracts an item from the beginning,<br/><br/>unshift(...items) – adds items to the beginning.<br/><br/>splice(pos, deleteCount, ...items) – at index pos deletes deleteCount elements and inserts items.<br/><br/>slice(start, end) – creates a new array, copies elements from index start till end (not inclusive) into it.<br/><br/>concat(...items) – returns a new array: copies all members of the current one and adds items to it. If any of items is an array, then its elements are taken.<br/><br/>To search among elements:<br/><br/>indexOf/lastIndexOf(item, pos) – look for item starting from position pos, return the index or -1 if not found.<br/><br/>includes(value) – returns true if the array has value, otherwise false.<br/><br/>find/filter(func) – filter elements through the function, return first/all values that make it return true.<br/><br/>findIndex is like find, but returns the index instead of a value.<br/><br/>To iterate over elements:<br/><br/>forEach(func) – calls func for every element, does not return anything.<br/><br/>To transform the array:<br/><br/>map(func) – creates a new array from results of calling func for every element.<br/><br/>sort(func) – sorts the array in-place, then returns it.<br/><br/>reverse() – reverses the array in-place, then returns it.<br/><br/>split/join – convert a string to array and back.<br/><br/>reduce/reduceRight(func, initial) – calculate a single value over the array by calling func for each element and passing an intermediate result between the calls.<br/><br/>Additionally:<br/><br/>Array.isArray(value) checks value for being an array, if so returns true, otherwise false.                                                                       |          |
| 47    | 5.2   | What is the difference between Array.forEach() and Array.map()?              | High     |
|       |       | `forEach`: This iterates over a list and applies some operation with side effects to each list member (example: saving every list item to the database) and does not return anything. <br/>`map`: This iterates over a list, transforms each member of that list, and returns another list of the same size with the transformed members (example: transforming list of strings to uppercase). It does not mutate the array on which it is called (although the callback function may do so).                                                                      |          |
|       | **6** | **Functions**                                                                |          |                                                                    
| 52    | 6.1   | What are the lambda or arrow functions?                                      | High     |
|       |       | They are simply expressions that create functions. One of the major advantages of arrow functions in js is that it does not have it's own this value. It's this is lexically bound to the enclosing scope.                                                                       |          |
| 53    | 6.2   | What is a pure function?                                                     | High     |
|       |       | A pure function is a function which: Given the same input, always returns the same output. Produces no side effects.                                                                       |          |
| 54    | 6.3   | What is IIFE(Immediately Invoked Function Expression)?                       | High     |
|       |       | As name suggest, IIFE is a function expression that automatically invokes after completion of the definition. The parenthesis () plays important role in IIFE pattern. In JavaScript, parenthesis cannot contain statements; it can only contain an expression.                                                                       |          |
| 55    | 6.4   | What is a callback function?                                                 | High     |
|       |       | A JavaScript callback is a function which is to be executed after another function has finished execution. A more formal definition would be - Any function that is passed as an argument to another function so that it can be executed in that other function is called as a callback function.                                                                       |          |
|       | **7** | **Async JavaScript**                                                         |          |                                                                   
| 62    | 7.1   | What is a promise?                                                           | High     |
|       |       | A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.                                                                       |          |
| 63    | 7.2   | Why do we need a promise?                                                    | High     |
|       |       | Promises give us the ability to write cleaner code but reducing (or entirely removing) call-back hell.<br/>In addition, callbacks are the backbone of some new syntax features coming in ES2017, such as async functions, which allows an even cleaner way of writing code.<br/>The third thing that promises do is not immediately apparent when you first learn the syntax -- automatic error handling. Promises allow errors to be passed down the chain and handled in one common place without having to put in layers of manual error handling.                                                                       |          |
| 64    | 7.3   | List all states of a promise?                                                | High     |
|       |       | 3 possible states: fulfilled, rejected, or pending.                                                                       |          |
| 65    | 7.4   | Why do we need callbacks?                                                    | High     |
|       |       | A callback's primary purpose is to execute code in response to an event. These events might be user-initiated, such as mouse clicks or typing                                                                       |          |
| 66    | 7.5   | What is a callback hell?                                                     | High     |
|       |       | Callback Hell is essentially nested callbacks stacked below one another forming a pyramid structure. Every callback depends/waits for the previous callback, thereby making a pyramid structure that affects the readability and maintainability of the code.                                                                       |          |
| 67    | 7.6   | What is promise chaining?                                                    | High     |
|       |       | Promise chaining is a syntax that allows you to chain together multiple asynchronous tasks in a specific order. This is great for complex code where one asynchronous task needs to be performed after the completion of a different asynchronous task.                                                                       |          |
| 68    | 7.7   | What is the purpose of using setTimeout?                                     | High     |
|       |       | The global setTimeout() method sets a timer which executes a function or specified piece of code once the timer expires                                                                       |          |
| 69    | 7.8   | What is the purpose of using setInterval?                                    | High     |
|       |       | The setInterval() function is commonly used to set a delay for functions that are executed again and again, such as animations                                                                       |          |
| 70    | 7.9   | What is an event loop?                                                       | High     |
|       |       | event loop, which handles the execution of multiple chunks of your program over time, each time invoking the JS Engine.                                                                       |          |
| 71    | 7.10  | What is call stack?                                                          | High     |
|       |       | A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.                                                                       |          |
|       | **8** | **Common**                                                                   |          |                                                                    
| 74    | 8.1   | How do you validate an email in javascript?                                  | High     |
|       |       | -Define a regular expression for validating email address.<br/>-Check if the input value matches with regular expression.<br/>-If it does match, send an alert stating “valid email address”<br/>-If it doesn't match, send an alert stating “invalid email address”                                                                       |          |
| 75    | 8.2   | What are modules?                                                            | High     |
|       |       | A module in JavaScript is just a file containing related code. In JavaScript, we use the import and export keywords to share and receive functionalities respectively across different modules. The export keyword is used to make a variable, function, class or object accessible to other modules                                                                       |          |
| 76    | 8.3   | Why do you need modules?                                                     | High     |
|       |       | JavaScript modules allow you to break up your code into separate files.<br/>This makes it easier to maintain the code-base.<br/>JavaScript modules rely on the import and export statements.                                                                       |          |
| 77    | 8.4   | What is a rest parameter?                                                    | High     |
|       |       | The rest parameter syntax allows a function to accept an indefinite number of arguments as an array. Rest parameter is an improved way to handle function parameter, allowing us to more easily handle various input as parameters in a function.                                                                       |          |
| 78    | 8.5   | What is a spread operator?                                                   | High     |
|       |       | The spread operator is a new addition to the set of operators in JavaScript ES6. It takes in an iterable (e.g an array) and expands it into individual elements. The spread operator is commonly used to make shallow copies of JS objects. Using this operator makes the code concise and enhances its readability.                                                                       |          |
| 79    | 8.6   | What is nodejs?                                                              | High     |
|       |       | Node.js is an open-source, cross-platform JavaScript runtime environment and library for running web applications outside the client's browser.                                                                        |          |
|       | **9** | **Browser API**                                                              |          |                                                                    
| 87    | 9.1   | What is the difference between window and document?                          | High     |
|       |       | `Window` is the main JavaScript object root, aka the global object in a browser, and it can also be treated as the root of the document object model. You can access it as window.<br/>`window.document` or just document is the main object of the potentially visible (or better yet: rendered) document object model/DOM.<br/>Since window is the global object, you can reference any properties of it with just the property name - so you do not have to write down window. - it will be figured out by the runtime.                                                                       |          |

### Week 2 (Questions with Medium priority)
Number of questions: Medium = 36.
Estimate: ~30m*36 = 18h / 5d = 3h 36m per day.

| Index | No.   | Questions                                                                    | Priority |
|-------|-------|------------------------------------------------------------------------------|----------|
|       | **1** | **Data Types**                                                               |          |
| 12    | 1.12  | Explain what a Symbol is in JavaScript?                                      | Medium   |
|       | 1.1   | answer                                                                       |          |
| 13    | 1.13  | How do you check whether a string contains a substring?                      | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **2** | **Objects, Classes, Prototypal inheritance**                                 |          |
| 18    | 2.4   | How do you check if a key exists in an object?                               | Medium   |
|       | 1.1   | answer                                                                       |          |
| 19    | 2.5   | What is the main difference between Object.values and Object.entries method? | Medium   |
|       | 1.1   | answer                                                                       |          |
| 20    | 2.6   | How can you get the list of keys of any object?                              | Medium   |
|       | 1.1   | answer                                                                       |          |
| 21    | 2.7   | What is a WeakSet?                                                           | Medium   | 
|       | 1.1   | answer                                                                       |          |
| 22    | 2.8   | What are the differences between WeakSet and Set?                            | Medium   | 
|       | 1.1   | answer                                                                       |          |
| 23    | 2.9   | What is a WeakMap?                                                           | Medium   | 
|       | 1.1   | answer                                                                       |          |
| 24    | 2.10  | What are the differences between WeakMap and Map?                            | Medium   | 
|       | 1.1   | answer                                                                       |          |
| 25    | 2.11  | What is the difference between proto and prototype?                          | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **3** | **Context, Scope and Closure**                                               |          |
| 38    | 3.11  | What are the problems with global variables?                                 | Medium   | 
|       | 1.1   | answer                                                                       |          |
| 39    | 3.12  | That is the Funarg problem?                                                  | Medium   |
|       | 1.1   | answer                                                                       |          |
| 40    | 3.13  | How does 'this' work in the arrow functions?                                 | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **4** | **JSON**                                                                     |          |
| 44    | 4.4   | Why do you need JSON?                                                        | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **5** | **Array methods**                                                            |          |
| 48    | 5.3   | What is the purpose of the array slice method?                               | Medium   |
|       | 1.1   | answer                                                                       |          |
| 49    | 5.4   | What is the purpose of the array splice method?                              | Medium   |
|       | 1.1   | answer                                                                       |          |
| 50    | 5.5   | List arrays methods, that mutate source array?                               | Medium   |
|       | 1.1   | answer                                                                       |          |
| 51    | 5.6   | List arrays methods, that return new array?                                  | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **6** | **Functions**                                                                |          |
| 56    | 6.5   | What is a first class function?                                              | Medium   |
|       | 1.1   | answer                                                                       |          |
| 57    | 6.6   | What is a first order function?                                              | Medium   |
|       | 1.1   | answer                                                                       |          |
| 58    | 6.7   | What is a Higher order function?                                             | Medium   |
|       | 1.1   | answer                                                                       |          |
| 59    | 6.8   | What is a unary function?                                                    | Medium   |
|       | 1.1   | answer                                                                       |          |
| 60    | 6.9   | What is the currying function?                                               | Medium   |
|       | 1.1   | answer                                                                       |          |
| 61    | 6.10  | What is an anonymous function?                                               | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **7** | **Async JavaScript**                                                         |          |
| 72    | 7.11  | What does promise.all method do?                                             | Medium   |
|       | 1.1   | answer                                                                       |          |
| 72    | 7.12  | What is the differance between promise.all and promise.allSettled?           | Medium   |
|       | 1.1   | answer                                                                       |          |
| 73    | 7.13  | What is the purpose of race method in promise?                               | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **8** | **Common**                                                                   |          |
| 80    | 8.7   | What is a strict mode in javascript?                                         | Medium   |
|       | 1.1   | answer                                                                       |          |
| 81    | 8.8   | What are PWAs?                                                               | Medium   |
|       | 1.1   | answer                                                                       |          |
| 82    | 8.9   | What is memoization?                                                         | Medium   |
|       | 1.1   | answer                                                                       |          |
| 83    | 8.10  | How do you encode an URL?                                                    | Medium   |
|       | 1.1   | answer                                                                       |          |
| 84    | 8.11  | How do you decode an URL?                                                    | Medium   |
|       | 1.1   | answer                                                                       |          |
|       | **9** | **Browser API**                                                              |          |
| 88    | 9.2   | How do you get the current url with javascript?                              | Medium   |
|       | 1.1   | answer                                                                       |          |
| 90    | 9.3   | What is a Fetch API?                                                         | Medium   |
|       | 1.1   | answer                                                                       |          |
| 94    | 9.4   | How to open two-way interactive session between browser and server?          | Medium   |
|       | 1.1   | answer                                                                       |          |
| 95    | 9.5   | How to abort async operation?                                                | Medium   |
|       | 1.1   | answer                                                                       |          |

### Week 3 (Questions with Low priority)
Number of questions: Low = 9.
Estimate: ~30m*9 = 4h 30m / 5d = 54m per day.

| Index | No.   | Questions                                                                    | Priority |
|-------|-------|------------------------------------------------------------------------------|----------|
|       | **2** | **Objects, Classes, Prototypal inheritance**                                 |          |
| 26    | 2.12  | How do you create an object with prototype?                                  | Low      |
|       | 1.1   | answer                                                                       |          |
| 27    | 2.13  | What is a proxy object?                                                      | Low      |
|       | 1.1   | answer                                                                       |          |
|       | **4** | **JSON**                                                                     |          |
| 45    | 4.5   | How do you define JSON arrays?                                               | Low      |
|       | 1.1   | answer                                                                       |          |
|       | **8** | **Common**                                                                   |          |
| 85    | 8.12  | What is tree shaking?                                                        | Low      |
|       | 1.1   | answer                                                                       |          |
| 86    | 8.13  | How do you detect javascript disabled in the page?                           | Low      |
|       | 1.1   | answer                                                                       |          |
|       | **9** | **Browser API**                                                              |          |
| 89    | 9.6   | How do you detect a mobile browser?                                          | Low      |
|       | 1.1   | answer                                                                       |          |
| 91    | 9.7   | How can we draw something in the browser?                                    | Low      |
|       | 1.1   | answer                                                                       |          |
| 92    | 9.8   | How to copy value to the clipboard?                                          | Low      |
|       | 1.1   | answer                                                                       |          |
| 93    | 9.9   | How to read value from the clipboard?                                        | Low      |
|       | 1.1   | answer                                                                       |          |

### Table of Contents by topics

| Index | No.   | Questions                                                                    | Priority |
|-------|-------|------------------------------------------------------------------------------|----------|
|       | **1** | **Data Types**                                                               |          |
| 1     | 1.1   | What are data types in javascript?                                           | High     |
| 2     | 1.2   | What are primitive data types?                                               | High     |
| 3     | 1.3   | What is the differance between primitives vs objects?                        | High     |
| 4     | 1.4   | What is coercion in JavaScript?                                              | High     |
| 5     | 1.5   | Do you know what Autoboxing in JS is?                                        | High     |
| 6     | 1.6   | What is the difference between == and === operators?                         | High     |
| 7     | 1.7   | What is undefined data type?                                                 | High     |
| 8     | 1.8   | What is null value?                                                          | High     |
| 9     | 1.9   | What does isNaN function do?                                                 | High     |
| 10    | 1.10  | What does NaN value mean?                                                    | High     |
| 11    | 1.11  | What is the difference between null and undefined?                           | High     |
| 12    | 1.12  | Explain what a Symbol is in JavaScript?                                      | Medium   |
| 13    | 1.13  | How do you check whether a string contains a substring?                      | Medium   |
|       | **2** | **Objects, Classes, Prototypal inheritance**                                 |          |
| 14    | 2.1   | How do you copy properties from one object to other?                         | High     |
| 15    | 2.2   | What are classes in ES6?                                                     | High     |
| 16    | 2.3   | Explain how prototypal inheritance works?                                    | High     |
| 18    | 2.4   | How do you check if a key exists in an object?                               | Medium   |
| 19    | 2.5   | What is the main difference between Object.values and Object.entries method? | Medium   |
| 20    | 2.6   | How can you get the list of keys of any object?                              | Medium   |
| 21    | 2.7   | What is a WeakSet?                                                           | Medium   | 
| 22    | 2.8   | What are the differences between WeakSet and Set?                            | Medium   | 
| 23    | 2.9   | What is a WeakMap?                                                           | Medium   | 
| 24    | 2.10  | What are the differences between WeakMap and Map?                            | Medium   | 
| 25    | 2.11  | What is the difference between proto and prototype?                          | Medium   |
| 26    | 2.12  | How do you create an object with prototype?                                  | Low      |
| 27    | 2.13  | What is a proxy object?                                                      | Low      |
|       | **3** | **Context, Scope and Closure**                                               |          |
| 28    | 3.1   | How do you assign default values to variables?                               | High     |
| 29    | 3.2   | What is the difference between let, const and var?                           | High     | 
| 30    | 3.3   | What are the differences between undeclared and undefined variables?         | High     | 
| 31    | 3.4   | What are global variables?                                                   | High     | 
| 32    | 3.5   | What is Hoisting?                                                            | High     |
| 33    | 3.6   | What is scope in javascript?                                                 | High     |
| 34    | 3.7   | What is the closure?                                                         | High     |
| 35    | 3.8   | How does closure implemented in the javascript?                              | High     |
| 36    | 3.9   | What is the difference between Call, Apply and Bind?                         | High     |
| 37    | 3.10  | What does 'this loses context' mean?                                         | High     |
| 38    | 3.11  | What are the problems with global variables?                                 | Medium   | 
| 39    | 3.12  | That is the Funarg problem?                                                  | Medium   |
| 40    | 3.13  | How does 'this' work in the arrow functions?                                 | Medium   |
|       | **4** | **JSON**                                                                     |          |                                                                    
| 41    | 4.1   | What is JSON and its common operations?                                      | High     |
| 42    | 4.2   | How do you parse JSON string?                                                | High     |
| 43    | 4.3   | What is the purpose JSON stringify?                                          | High     |
| 44    | 4.4   | Why do you need JSON?                                                        | Medium   |
| 45    | 4.5   | How do you define JSON arrays?                                               | Low      |
|       | **5** | **Array methods**                                                            |          |                                                                    
| 46    | 5.1   | What array methods do you know?                                              | High     |
| 47    | 5.2   | What is the difference between Array.forEach() and Array.map()?              | High     |
| 48    | 5.3   | What is the purpose of the array slice method?                               | Medium   |
| 49    | 5.4   | What is the purpose of the array splice method?                              | Medium   |
| 50    | 5.5   | List arrays methods, that mutate source array?                               | Medium   |
| 51    | 5.6   | List arrays methods, that return new array?                                  | Medium   |
|       | **6** | **Functions**                                                                |          |                                                                    
| 52    | 6.1   | What are the lambda or arrow functions?                                      | High     |
| 53    | 6.2   | What is a pure function?                                                     | High     |
| 54    | 6.3   | What is IIFE(Immediately Invoked Function Expression)?                       | High     |
| 55    | 6.4   | What is a callback function?                                                 | High     |
| 56    | 6.5   | What is a first class function?                                              | Medium   |
| 57    | 6.6   | What is a first order function?                                              | Medium   |
| 58    | 6.7   | What is a Higher order function?                                             | Medium   |
| 59    | 6.8   | What is a unary function?                                                    | Medium   |
| 60    | 6.9   | What is the currying function?                                               | Medium   |
| 61    | 6.10  | What is an anonymous function?                                               | Medium   |
|       | **7** | **Async JavaScript**                                                         |          |                                                                   
| 62    | 7.1   | What is a promise?                                                           | High     |
| 63    | 7.2   | Why do we need a promise?                                                    | High     |
| 64    | 7.3   | List all states of a promise?                                                | High     |
| 65    | 7.4   | Why do we need callbacks?                                                    | High     |
| 66    | 7.5   | What is a callback hell?                                                     | High     |
| 67    | 7.6   | What is promise chaining?                                                    | High     |
| 68    | 7.7   | What is the purpose of using setTimeout?                                     | High     |
| 69    | 7.8   | What is the purpose of using setInterval?                                    | High     |
| 70    | 7.9   | What is an event loop?                                                       | High     |
| 71    | 7.10  | What is call stack?                                                          | High     |
| 72    | 7.11  | What does promise.all method do?                                             | Medium   |
| 72    | 7.12  | What is the differance between promise.all and promise.allSettled?           | Medium   |
| 73    | 7.13  | What is the purpose of race method in promise?                               | Medium   |
|       | **8** | **Common**                                                                   |          |                                                                    
| 74    | 8.1   | How do you validate an email in javascript?                                  | High     |
| 75    | 8.2   | What are modules?                                                            | High     |
| 76    | 8.3   | Why do you need modules?                                                     | High     |
| 77    | 8.4   | What is a rest parameter?                                                    | High     |
| 78    | 8.5   | What is a spread operator?                                                   | High     |
| 79    | 8.6   | What is nodejs?                                                              | High     |
| 80    | 8.7   | What is a strict mode in javascript?                                         | Medium   |
| 81    | 8.8   | What are PWAs?                                                               | Medium   |
| 82    | 8.9   | What is memoization?                                                         | Medium   |
| 83    | 8.10  | How do you encode an URL?                                                    | Medium   |
| 84    | 8.11  | How do you decode an URL?                                                    | Medium   |
| 85    | 8.12  | What is tree shaking?                                                        | Low      |
| 86    | 8.13  | How do you detect javascript disabled in the page?                           | Low      |
|       | **9** | **Browser API**                                                              |          |                                                                    
| 87    | 9.1   | What is the difference between window and document?                          | High     | 
| 88    | 9.2   | How do you get the current url with javascript?                              | Medium   |
| 90    | 9.3   | What is a Fetch API?                                                         | Medium   |
| 94    | 9.4   | How to open two-way interactive session between browser and server?          | Medium   |
| 95    | 9.5   | How to abort async operation?                                                | Medium   |
| 89    | 9.6   | How do you detect a mobile browser?                                          | Low      |
| 91    | 9.7   | How can we draw something in the browser?                                    | Low      |
| 92    | 9.8   | How to copy value to the clipboard?                                          | Low      |
| 93    | 9.9   | How to read value from the clipboard?                                        | Low      |
