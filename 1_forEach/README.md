# Part II: forEach

Before getting started, make sure that you have a JavaScript console open (like <a href="http://www.repl.it/languages/javascript" target="_blank">repl.it</a>), so you can complete these exercises.

## Exercises

1. Refactor the following imperative code to be declarative by using the `forEach()` native array method instead of a `for` loop:

```js
var sumImperative = function(array) {
  var result = 0;
  for (var i = 0; i < array.length; i++) {
    result = result + array[i];
  }
  return result;
};

var sumDeclarative = function(array) {
  // your code here
};
```

2. Refactor the following imperative code to be declarative by using the `forEach()` native array method instead of a `for` loop:

```js
var maxNumImperative = function(array) {
  var max = array[0];
  for (var i = 0; i < array.length; i++) {
    if (array[i] > max) {
      max = array[i];
    }
  }
  return max;
};

var maxNumDeclarative = function(array) {
  // your code here
};
```

3. Write a function called `min` that find the smallest number in an array of numbers and returns it.

```js
var min = function(array) {
  // your code here
};

min([100, 54, 73, 8, 12, 3]); // => 3
```

4. Write a function called printNames that takes an array of names and console.logs them:

```js
var printNames = function(names) {
  // your code here
};

printNames(['Tom', 'Jerry', 'Arnold', 'Casper']);
```

