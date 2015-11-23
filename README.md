# tonal.transpose

[![Build Status](https://travis-ci.org/danigb/tonal.svg?branch=master)](https://travis-ci.org/danigb/tonal.transpose)
[![Code Climate](https://codeclimate.com/github/danigb/tonal.transpose/badges/gpa.svg)](https://codeclimate.com/github/danigb/tonal.transpose)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)
[![npm version](https://img.shields.io/npm/v/tonal.transpose.svg)](https://www.npmjs.com/package/tonal.transpose)
[![license](https://img.shields.io/npm/l/tonal.transpose.svg)](https://www.npmjs.com/package/tonal.transpose)
[![tonal](https://img.shields.io/badge/lib-tonal-yellow.svg)](https://www.npmjs.com/package/tonal)


`tonal.transpose` is a function to get transpose notes:

```js
var transpose = require('tonal.transpose')
distance('C3', '3m') // => 'Eb3'
```

## Install

Only via npm: `npm i --save tonal.transpose`

## Usage

#### Note transposition

The simplest usage is with a note name (pitch) and interval (the order doesn't matter):

```js
transpose('C2', '4A') // => 'F#2'
transpose('4A', 'C2') // => 'F#2'
```

#### Pitch class transposition

You can transpose pitch classes (note names without octaves), and the returned value will be a pitch class:

```js
tranpose('A', '3M') // => 'C#'
tranpose('A5', '3M') // => 'C#5'
```

#### Add intervals

If you need it you can transpose an interval:

```js
transpose('3M', '3M') // => '5A'
```

#### Transposers

Also, you can partially apply the function to get a transposer:

```js
var major3th = transpose('3M')
major3th('D') // => 'F#'
```

#### Map arrays

Partially applied transposers allows to work with arrays seamlessly:

```
['C', 'D', 'E', 'F', 'G'].map(transpose('3M')) // => ['E', 'F#', 'G#', 'A', 'B']
['1P', '3m', '5P'].map(transpose('C')) // => ['C', 'Eb', 'G']
```

#### Using different interval or pitch representations

This library can work with [pitches or intervals expressed as arrays]()

```js
```

#### More...

See [tonal](https://www.npmjs.com/package/tonal)


## License

MIT License
