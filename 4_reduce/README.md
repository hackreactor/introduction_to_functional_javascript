# Part V: reduce

Before getting started, make sure that you have a JavaScript console open (like <a href="http://www.repl.it/languages/javascript" target="_blank">repl.it</a>), so you can complete these exercises.

## Exercises

Try to implement the following functions using .reduce(). If you are having trouble, try implementing them using more traditional loops and see if you can refactor to .reduce()!

1. Write a function that takes an array of numbers and returns the sum of all the numbers:

```js
var sum = function(numbers) {
  // your code here
};

sum([2, 4, 6]); // => 12
```

2. Write a function that takes an array of numbers and returns the product of all the numbers:

```js
var product = function(numbers) {
  // your code here
};

product([2, 4, 6]); // => 48
```

3. Write a function that takes an array of words and returns a sentence (single string) with all the element strings concatenated together:

```js
var stringConcat = function(strings) {
  // your code here
};

stringConcat(['Hello', 'my', 'name', 'is', 'Alexandra']); // => 'Hello my name is Alexandra'
```

4. Write a function that takes an array of users and returns an object with keys that are the users' names and values that are their email addresses:

```js
var users = [
  { fullName: 'George Washington', email: 'george@us.gov' },
  { fullName: 'John Adams', email: 'john@us.gov' },
  { fullName: 'Thomas Jefferson', email: 'thomas@us.gov' },
  { fullName: 'James Madison', email: 'james@us.gov' }
]

var createEmailObject = function(users) {
  // your code
};

createEmailObject(users); // => {
//   'George Washington': 'george@us.gov',
//   'John Adams': 'john@us.gov',
//   'Thomas Jefferson': 'thomas@us.gov',
//   'James Madison': 'james@us.gov'
// }
```

## More Practice

Take a look at the array of spell objects in spell.js (in this folder). Using that as your input data set:

1. Write a function that returns an array of all the spell names.

```js
var spellNames = function(spells) {
  // your code here
};
```

2. Write a function that returns an array of spell objects that have a level higher than 1, with each object holding the spell name and level:
{
  name: 'spell-name',
  level: 1+
}


```js
var spellNames = function(spells) {
  // your code here
};
```

## Challenge Mode

1. Implement all of the function exercises for .map() using .reduce()

2. Implement all of the function exercises for .filter() using .reduce()