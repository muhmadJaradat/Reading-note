# In memory storage

## What is a ‘call’?

call is the function invocation

## How many ‘calls’ can happen at once?

only one , because It is single-threaded. Meaning it can only do one thing at a time.

## What does LIFO mean?

Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

## Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

![](https://media.geeksforgeeks.org/wp-content/uploads/LIFO.jpg)

![](https://flaviocopes.com/javascript-event-loop/exception-call-stack.png)

## What causes a Stack Overflow?

 stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

 Here is an example:

```javascript
function callMyself(){
  callMyself();
}

callMyself();
```

The callMyself() will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.

# JavaScript error messages && debugging

## What is a ‘refrence error’?

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

`console.log(foo) // Uncaught ReferenceError: foo is not defined`

This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).

```javascript
foo = 'Hello' // Uncaught ReferenceError: foo is not defined
let foo
```

Whatever you are using (var, let or const) the fix is as simple has declaring the variable before any declaration is made.

```javascript
let foo;
foo = 'Hello'
```

## What is a ‘syntax error’?

I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

`JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`

This can be solved by just fixing the syntax, in this case the object should be a JSON.

`JSON.parse('{"foo":"bar"}')`

Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

## What is a ‘range error’?

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

```javascript
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
```

An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:

```javascript
var foo = [0, 0]
foo.length = foo.length - 2 // (or foo.length - foo.length)
foo // would log [] instead of [0, 0]
```

I prefer not to mutate my variables whenever possible (making them constants and not variables) but this is a method that is available and now you know it.

## Type errors

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

```javascript
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
```

This is probably the most frequent error in JS, trying to access a property/method thinking that bar is of the type object when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available.

The fix is simple, just make sure that bar exists before trying to access it, either by creating bar or by checking for undefined.

```
var foo = { bar: {} }
foo.bar.baz // undefined but you avoid the error
```

**OR**

```
var foo = {}
if (typeof foo.bar !== 'undefined') {
  foo.bar.baz // this will never be executed while bar does not exist
}
```

## What is a breakpoint?

will make your program stop at that point only if a condition is met
