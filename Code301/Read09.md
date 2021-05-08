# FUNCTIONAL PROGRAMMING

## What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

### Pure functions

So how do we know if a function is pure or not? Here is a very strict definition of purity:

* It returns the same result if given the same arguments (it is also referred as deterministic)

* It does not cause any observable side effects

**It returns the same result if given the same arguments**

Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate `radius * radius * PI`:

```javascript
let PI = 3.14;

const calculateArea = (radius) => radius * radius * PI;

calculateArea(10); // returns 314.0
```

Why is this an impure function? Simply because it uses a global object that was not passed as a parameter to the function.

Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object.
Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result. Let's fix it!

```javascript
let PI = 3.14;

const calculateArea = (radius, pi) => radius * radius * pi;

calculateArea(10, PI); // returns 314.0
```

Now we’ll always pass thePI value as a parameter to the function. So now we are just accessing parameters passed to the function. No `external object`.

**It does not cause any observable side effects**

Examples of observable side effects include modifying a global object or a parameter passed by reference.

Now we want to implement a function to receive an integer value and return the value increased by 1.

```javascript
let counter = 1;

function increaseCounter(value) {
  counter = value + 1;
}

increaseCounter(counter);
console.log(counter); // 2
```

We have the `counter` value. Our impure function receives that value and re-assigns the counter with the value increased by 1.

**Observation**: mutability is discouraged in functional programming.

We are modifying the global object. But how would we make it pure? Just return the value increased by 1. Simple as that.

```javascript
let counter = 1;

const increaseCounter = (value) => value + 1;

increaseCounter(counter); // 2
console.log(counter); // 1
```

## What are the benefits of a pure function?

The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:

* Given a parameter `A` → expect the function to return value `B`

*Given a parameter `C` → expect the function to return value `D`

A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.

```javascript
let list = [1, 2, 3, 4, 5];

const incrementNumbers = (list) => list.map(number => number + 1);
```

## What is immutability?

immutability is Unchanging over time or unable to be changed.

![](https://miro.medium.com/max/735/0*MGlzHgISuw0dXwsf)

When data is immutable, its **state cannot change after it’s created**. If you want to change an immutable object, you can’t. Instead, **you create a new object with the new value**.

In Javascript we commonly use the for loop. This next for statement has some mutable variables.

```javascript
var values = [1, 2, 3, 4, 5];
var sumOfValues = 0;

for (var i = 0; i < values.length; i++) {
  sumOfValues += values[i];
}

sumOfValues // 15
```

For each iteration, we are changing the i and the sumOfValue state. But how do we handle mutability in iteration? Recursion!

```javascript
let list = [1, 2, 3, 4, 5];
let accumulator = 0;

function sum(list, accumulator) {
  if (list.length == 0) {
    return accumulator;
  }

  return sum(list.slice(1), accumulator + list[0]);
}

sum(list, accumulator); // 15
list; // [1, 2, 3, 4, 5]
accumulator; // 0
```

So here we have the sum function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each "iteration" we will add the value to the total accumulator.

## Referential transparency

![](https://miro.medium.com/max/735/0*K0VAbQjAwmKZb1at)

```javascript
const square = (n) => n * n;
```

This pure function will always have the same output, given the same input.

```javascript
square(2); // 4
square(2); // 4
square(2); // 4
// ...
```

Passing 2 as a parameter of the square function will always returns 4. So now we can replace the square(2) with 4. That's it! Our function is `referentially transparent`.

Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

**pure functions + immutable data = referential transparency**

