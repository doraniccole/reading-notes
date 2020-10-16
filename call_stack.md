Definitions for Flash Cards:
call stack:mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.If the stack takes up more space than it had assigned to it, it results in a "stack overflow" function:code snippet that can be called by other code or by itself, or a variable that refers to the function. When a function is called, arguments are passed to the function as input, and the function can optionally return a value. A function in JavaScript is also an object. name is an identifier included as part of a function declaration or function expression. The function name's scope depends on whether the function name is a declaration or expression.anonymous function:function without a function name. Only function expressions can be anonymous, function declarations must have a name// When used as a function expression

`(function () {});
// or using the ECMAScript 2015 arrow notation
() => {};named function: function with a function name// Function declaration
function foo() {};
// Named function expression
(function bar() {});
// or using the ECMAScript 2015 arrow notation
const foo = () => {};inner function is a function inside another function (square in this case)outer function: is a function containing a function (addSquares in this case)function addSquares(a,b) {
   function square(x) {
      return x * x;
   }
   return square(a) + square(b);
};`

`//Using ECMAScript 2015 arrow notation
const addSquares = (a,b) => {
   const square = x => x*x;
   return square(a) + square(b);
};recursive function is a function that calls itselffunction loop(x) {
   if (x >= 10)
      return;
   loop(x + 1);
};`

`//Using ECMAScript 2015 arrow notation
const loop = x => {
   if (x >= 10)
      return;
   loop(x + 1);
}; Immediately Invoked Function Expressions:(IIFE) is a function that is called directly after the function is loaded into the browser’s compiler. The way to identify an IIFE is by locating the extra left and right parenthesis at the end of the function’s definition// Declared functions can't be called immediately this way
// Error (https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)
/*
​function foo() { 
    console.log('Hello Foo'); 
}();
*/`

`// Function expressions, named or anonymous, can be called immediately
(function foo() {
    console.log("Hello Foo");
}());

(function food() {
    console.log("Hello Food");
})();`

(() => console.log('hello world'))();DebuggingTo debug your JS code, the easiest and maybe the most common way its to simplyconsole.log()the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).Chrome testing In Order:testing is automatically called since it’s an IIFE (immediately Invoked Function Expression);obj variable is declared with the function add (using ES6 shorthand for functions in objects, it would be the same having var obj = { add: add } ;the function add is called from the obj variable with two strings has parameters, there are added which makes them “12” in this scenario and then split is called before returning [“1”, “2”];the function add is called again, this time with number, the values are added making it 3 but then, split (which is not available for number type variables) is called which makes an error being thrown;Call stackThe red part of our first example represents the call stack, which is the path that your program has taken to reach the point were you set a breaking point or were you have an errorTypes of error messages:Reference error:This is as simple as when you try to use a variable that is not yet declared you get this type os errors.'console.log(foo) // Uncaught ReferenceError: foo is not defined'This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).`foo = 'Hello' // Uncaught ReferenceError: foo is not definedlet foo`Whatever you are using (var, let or const) the fix is as simple has declaring the variable before any declaration is made.`let foo;foo = 'Hello'` Syntax errorsI know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.`JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`This can be solved by just fixing the syntax, in this case the object should be a JSON.`JSON.parse('{"foo":"bar"}')`Range errorsTry to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.`var foo= []foo.length = foo.length -1 // Uncaught RangeError: Invalid array length`An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:`var foo = [0, 0]foo.length = foo.length - 2 // (or foo.length - foo.length)foo // would log [] instead of [0, 0]`Type errorsLike the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.`var foo = {}foo.bar // undefinedfoo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined`The fix is simple, just make sure that bar exists before trying to access it, either by creating bar or by checking for undefined.`var foo = { bar: {} }foo.bar.baz // undefined but you avoid the error`or`var foo = {}if (typeof foo.bar !== 'undefined') {  foo.bar.baz // this will never be executed while bar does not exist}`Tools to avoid runtime errors:quokka to evaluate your code as you typeeslint to make sure your style guide is consistency and it will grab you an error or two along the way andFor those of you looking to make JS a more strong typed experience you can check out stuff like TypeScript (like I said in a previous article, when learning I rather avoid libraries that abstract the core language so I wouldn’t recommend this last one when starting). 
