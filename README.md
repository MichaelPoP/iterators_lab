# Iterators Lab

### Description

In the iterators lab we will be continuing our exploration of
iterators. We have a series of challenges that require you to use the
iterators we discussed in class. We will try to use various testing
methods to verify that your code is working.

### Phase-1

Research the following term and summarize your findings on it two to
three sentences:

* `higher-order function` -->A function is considered 'higher-order' when it's inputs or outputs include 
another function. Higher- order functions are different from standard functions (first-class functions) because they deal with possibilities over 'actions' rather than just values like in the standard case. 


Update this README with a description of each of the following and an
example you've created:
_________________________________________________________________________________________________________________________
* `forEach`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
=>(SYNTAX > arr.function(callback[, thisarg])
>forEach() will execute a given method on 'each' element of an array.
EXAMPLE___
var foods = ["burritos", "chips", "candy", "marshmallows];
foods.forEach(function (junk) {
    console.log("I like " + junk )
});
"I like burritos"
"I like chips"
"I like candy"
"I like marshmallows"
_________________________________________________________________________________________________________________________
* `map`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
=>SYNTAX > arr.map(callback[, thisArg])
>map() will create a new array using the results of a function that is applied to every element in a given array.
EXAMPLE___
var names = ["Michael", "Chris", "Chip", "Sue", "Scott"];
var UpperCased = names.map(function (family) {
    return family.toUpperCase();
});
console.log(UpperCased);

>["MICHAEL", "CHRIS", "CHIP", "SUE", "SCOTT"]
_________________________________________________________________________________________________________________________
* `filter`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
=>SYNTAX > arr.filter(callback[, thisArg])
>filter() will create a new array and fill it only with elements that remain after a selective function is applied.
EXAMPLE___
var desertAnimals = ["snake", "owl", "javelina", "roadrunner", "hummingbird", "rabbit", "coyote", "gilamonster"];

var even = function (animal) {
    return animal.length % 2 === 0;
};
var odd = function (animal) {
  return animal.length % 2 !== 0;  
};

var evenNames = desertAnimals.filter(even);
var oddNames = desertAnimals.filter(odd);

console.log(evenNames);["javelina", "roadrunner", "rabbit", "coyote"]
console.log(oddNames);["snake", "owl", "hummingbird", "gilamonster"]
_________________________________________________________________________________________________________________________
* `reduce`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
=>SYNTAX > arr.reduce(callback[, initialValue])
>reduce() will take an array and reduce it to a single value by running a function against an accumulator (a variable that that modifies values in some way other than counting) always from left to right.
EXAMPLE ____
var strings = ["anti", "disest", "ablish", "ment", "arian", "ism"];

names.reduce(function (prev, next) {
     return prev + next;
});
>antidisestablishmentarianism
_________________________________________________________________________________________________________________________
* `some`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
=>SYNTAX > arr.some(callback[, thisArg])
>some() will take an array and use a function to test all of the elements in the array to see if some of them return a true value (this is a boolean method).
EXAMPLE___
var numbers = [2, 4, 6, 8, 35];

numbers.some(function isEven(numbers) {
   return numbers % 2 === 0;
});
>true
_________________________________________________________________________________________________________________________
* `every`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
=>SYNTAX arr.every(callback[, thisArg])
>every() will apply a given function against all the elements in an array but does not mutate the array itself.
var nums= [13, 43, 5, 7, 33, 12, 66];
nums.every(function isSmallEnough(num) {
    return num <= 15;
});
>false

_________________________________________________________________________________________________________________________

Use the notes provided to help guide you explanation.

### Phase-2

* Run `npm install` from the `iterators_lab` directory.
* Looks at the tests we've written in the `test` folder. Run the tests
  with `npm test` (also from the `iterators_lab` directory). They
  should all fail.
* Get all of the tests to pass by writing the necessary code in
  `src/iterators.js`.

### Phase-3

Refactor the following code using `map` to make only one call to the `map` function versus the two below.


```
var myNumbers = [ -1, 2, -3, 4, -5, 6];

var square = function(num) {
	return num * num;
};

var sqrRoot = function(num) {
	return Math.sqrt(num);
};

return myNumbers.map(square, sqrRoot);



//var sqrNumbers = map(myNumbers, square);
//var absNumbers = map(sqrNumbers, sqrRoot);
```




