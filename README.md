# shuffle-array

> Randomize the order of the elements in a given array using the [Fisher-Yates algorithm](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).

## Installation

    $ npm install shuffle-array

## Usage
```js
var shuffle = require('shuffle-array'),
    collection = [1,2,3,4,5];

shuffle(collection);

console.log(collection); // returns [4, 3, 1, 5, 2]
```

## API

### shuffle(arr, [options])
Randomizes the order of the elements in a given `array`.
- `arr` - The given array.
- [`options`] {Object} - Optional configuration options.
- [`options.copy`] {Boolean} - Sets if should return a shuffled copy of the given array. By default it's a falsy value.
- [`options.rng`] {Function} - Specifies a custom random number generator.

```js
shuffle([1,2,3,4,5]); // returns [4, 3, 1, 5, 2]

// Return a copy of the given array
shuffle([1,2,3,4,5], { 'copy': true }); // returns [4, 3, 1, 5, 2] (copied)
```

### shuffle.pick(arr, [options])
Pick one or more `random` elements from the given `array`.
- `arr` - The given array.
- [`options`] {Object} - Optional configuration options.
- [`options.picks`] {Number} - Specifies how many random elements you want to pick. By default it picks 1.
- [`options.rng`] {Function} - Specifies a custom random number generator.

```js
shuffle.pick([1,2,3,4,5]); // returns 5

// Return a random collection with 2 elements
shuffle.pick([1,2,3,4,5], { 'picks': 2 })); // returns [4, 3]
```

## Build

    npm run dist

## Test

    npm test

This is a clone of the legacy shuffle-array library that was originally built by Guille Paz.

## License
MIT license. Copyright © 2016.

