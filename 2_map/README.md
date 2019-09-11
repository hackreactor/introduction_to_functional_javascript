# Part III: map

Before getting started, make sure that you have a JavaScript console open (like <a href="http://www.repl.it/languages/javascript" target="_blank">repl.it</a>), so you can complete these exercises.

## Exercises

1. Write a function that takes an array of numbers and returns a new array with each number squared:

```js
var squared = function(numbers) {
  // your code here
};

squared([1, 2, 3, 4, 5]); // => [1, 4, 9, 16, 25]
```

2. Write a function that takes an array of words that are singular and returns an array of the same words pluralized:

```js
var pluralize = function(words) {

};

pluralize(['dog', 'cat', 'worm', 'kyle']); // => ['dogs', 'cats', 'worms', 'kyles']
```

3. Write a function that takes an array of artist/song objects and returns an array of strings that name the song and say who it is performed by:

```js
var songs = [
  { song: 'Phenom', artist: 'Alex Mali' },
  { song: 'Too Deep', artist: 'dvsn' },
  { song: 'Firefly', artist: 'Mura Masa' }
];

var songsBy = function(songs) {
  // your code here
};

songsBy(songs); // => ['Phenom by Alex Mali', 'Too Deep by dvsn', 'Firefly by Mura Masa']
```


4. Write a function that takes an array of user objects and returns an array of just the users' first names:

```js
var users = [
  { firstName: 'Homer', lastName: 'Simpson' },
  { firstName: 'Marge', lastName: 'Simpson' },
  { firstName: 'Bart', lastName: 'Simpson' },
  { firstName: 'Lisa', lastName: 'Simpson' },
  { firstName: 'Maggie', lastName: 'Simpson' }
];

var firstNames = function(users) {
  // your code here
};

firstNames(users); // => ['Homer', 'Marge', 'Bart', 'Lisa', 'Maggie']
```

5. Write a function that takes an array of user objects and returns an array with just the users' full names:

```js
var users = [
  { firstName: 'Homer', lastName: 'Simpson' },
  { firstName: 'Marge', lastName: 'Simpson' },
  { firstName: 'Bart', lastName: 'Simpson' },
  { firstName: 'Lisa', lastName: 'Simpson' },
  { firstName: 'Maggie', lastName: 'Simpson' }
];

var fullNames = function(users) {
  // your code here
};

fullNames(users); // => ['Homer Simpson', 'Marge Simpson', 'Bart Simpson', 'Lisa Simpson', 'Maggie Simpson']
```

6. Write a function that takes an array of user objects and returns an array of objects with just the users' full names:

```js
var users = [
  { firstName: 'Homer', lastName: 'Simpson' },
  { firstName: 'Marge', lastName: 'Simpson' },
  { firstName: 'Bart', lastName: 'Simpson' },
  { firstName: 'Lisa', lastName: 'Simpson' },
  { firstName: 'Maggie', lastName: 'Simpson' }
];

var fullNameObjects = function(users) {
  // your code here
};

fullNameObjects(users); // => [{ fullName: 'Homer Simpson' }, { fullName: 'Marge Simpson' }, { fullName: 'Bart Simpson' }, { fullName: 'Lisa Simpson' }, { fullName: 'Maggie Simpson' }]
```

7. Write a function that takes an array of arrays that contain product information, and returns an array of objects with appropriate keys:

```js
var products =  [
  ['Dark Chocolate Crunchies', 4.11, 3],
  ['Peppermint Poppers', 0.88, 1],
  ['Banana Bunches', 2.33, 2]
]

var toObject = function(products) {
  // your code here
};

toObject(products); // => [
//   { name: 'Dark Chocolate Crunchies', price: 4.11, quantity: 3 },
//   { name: 'Peppermint Poppers', price: 0.88, quantity: 1 },
//   { name: 'Banana Bunches', price: 2.33, quantity: 2 }
// ]
```

#### More Practice

Map is often used to transform a data set to be more readable or usable. Take a look at the array of spell objects in spells.js (in this folder). Using that as your input data set:

1. Clean up the data so it is more readable. Write a function that returns an array of spell objects, with each object containing the spell's name, description, and duration:
* Each spell object should look like this:
```js
{
  name: 'spell-name',
  description: 'spell-description',
  duration: 'spell-duration',
}
```

2. Write a function that returns an array of spell objects, with each object containing the spell's name and all of the classes and subclasses that can use the spell as subarrays:
* Each spell object should look like this:
```js
{
  name: 'spell-name',
  classes: ['class-name-1', 'class-name-2'],
  subclasses: ['subclass-name-1', 'subclass-name-2']
}
```