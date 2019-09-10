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
sumImperative([5, 10, 15]); // => 30

var sumDeclarative = function(array) {
  var result = 0;
  array.forEach(function(number) {
    result = result + number;
  });
  return result;
};
sumDeclarative([5, 10, 15]); // => 30
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
maxNumImperative([1, 2, 20, 4, 5]); // => 20

var maxNumDeclarative = function(array) {
  var max = array[0];
  array.forEach(function(number) {
    if (number > max) {
      max = number;
    }
  });
  return max;
};
maxNumDeclarative([1, 2, 20, 4, 5]); // => 20
```

3. Write a function called `min` that find the smallest number in an array of numbers and returns it.

```js
var min = function(array) {
  var min = array[0];
  array.forEach(function(number) {
    if (number < min) {
      min = number;
    }
  });
  return min;
};

min([100, 54, 73, 8, 12, 3]); // => 3
```

4. Write a function called printNames that takes an array of names and console.logs them:

```js
var printNames = function(names) {
  names.forEach(function(name) {
    console.log(name);
  });
};
printNames(['Tom', 'Jerry', 'Arnold', 'Casper']);
```

## More Practice

## Exercises

Try to write all of these exercises using .forEach() rather than `for` or `while` loops.

### Basic Requirements

1. Try the following at a console:

  ```js
  "the quick brown fox jumped over the lazy dog".split(" ");
  "Hello, world!".split("")
  "1,2,3,4,5,6".split(",")
  ```

  What is returned by `split` (You can read more about it
  [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)),
  and how does it work?

  Use `split` to write a function `longestWord` that takes a string as an
  argument and returns the longest word.

  ```js
  var longestWord = function(string) {
    var words = string.split(' ');
    var longestWord = words[0];
    words.forEach(function(word) {
      if (word.length > longestWord.length) {
        longestWord = word;
      }
    });
    return longestWord;
  };
  longestWord('Hello my name is Arnold'); // => 'Arnold'
  ```

2. Write a function `remove` that accepts an *array* and an *element*, and
   returns an array with all ocurrences of *element* removed.

  ```js
  var remove = function(array, element) {
    var removed = [];
    array.forEach(function(el) {
      if (el !== element) {
        removed.push(el);
      }
    });
    return removed;
  };
  remove([1, 3, 6, 2, 3], 3); // => [1, 6, 2]
  ```

3. Write a function `evens` that accepts an array as an argument, and returns
   an array consisting of all of the *even* numbers in that array.
  
  ```js
  var evens = function(numbers) {
    var evenNums = [];
    numbers.forEach(function(number) {
      if (number % 2 === 0) {
        evenNums.push(number);
      }
    });
    return evenNums;
  };
  evens([1, 2, 3, 4, 5, 6, 7, 8]) // => [2, 4, 6, 8];
  ```

### Exercises Continued

1. Write a function called `average` that takes an array of numbers as a
   parameter and returns the *average* of those numbers.
  
  ```js
  var average = function(numbers) {
    var sum = 0;
    numbers.forEach(function(number) {
      sum = sum + number;
    });
    return sum / numbers.length; 
  };
  average([1, 2, 3, 4, 5]) // => 3;
  ```

2. Write a function `shortestWord` that works like `longestWord`, but returns
   the *shortest* word instead.
  
  ```js
  var shortestWord = function(string) {
    var words = string.split(' ');
    var shortest = words[0];
    words.forEach(function(word) {
      if (word.length < shortest.length) {
        shortest = word;
      }
    });
    return shortest;
  };
  shortestWord('all your base are belong to us') // => 'to';
  ```

3. Write a function `countChar` that takes two arguments: any string, and a
   *character* (string of one letter), and returns the number of times that the
   character occurs in the string.
  
  ```js
  var countChar = function(string, char) {
    var occurances = 0;
    var characters = string.split('');
    characters.forEach(function(character) {
      if (character === char) {
        occurances = occurances + 1;
      }
    });
    return occurances;
  };
  countChar('hello world', 'o') // => 2;
  ```

4. Write a function `evenLengthWords` that takes an array of *strings* as an
   argument, and returns an array of just the words that have an even length.

  ```js
  var evenLengthWords = function(strings) {
    var result = [];
    strings.forEach(function(string) {
      if (string.length % 2 === 0) {
        result.push(string);
      }
    });
    return result;
  };
  evenLengthWords(['hello', 'world', 'I', 'am', 'here']) // => ['am', 'here'];
  ```

### Advanced

1. Read about the `join` method on
   [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
   and use it to implement a function that accepts a string as an argument and
   returns that string *reversed*.

  ```js
  var reverseString = function(str) {
    return str.split('').reverse().join('');
  };
  reverseString('hello') // => 'olleh';
  ```

2. Write a function `keep` that "keeps" certain elements in an array. The
   function will need to take *two* arguments, an array, and something else --
   the second argument will be what is used to determine which elements to keep.
  
  ```js
  var keep = function(array, fn) {
    var result = [];
    array.forEach(function(element) {
      if (fn(element) === true) {
        result.push(element);
      }
    })
    return result;
  };
  ```

   You should be able to use this function to write `evens`, `evenLengthWords`,
   a hypothetical `odds` function, or `oddLengthWords` *without changing the
   `keep` function*.

  ```js
  keep([1, 2, 3, 4, 5], function(el){
	  return el % 2 === 0;
  }); // => [2, 4]
  ```
