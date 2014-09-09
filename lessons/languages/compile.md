#MHS Robotics Club: Languages#

Most languages can be compiled to Javascript with tools dedicated for that task. There are some languages, however, which cannot be run alone, but HAVE to be compiled to Javascript.

Their main goals are to take out the worst parts of Javascript, and make writing code easier.

<b>Coffeescript</b><br/>
Arguably the most popular compiling language, it is intended to make difficult tasks easier.

An example of Coffeescript code:
```coffeescript
even_nums = (i for i in [0..10] when i % 2 == 0)
odd_nums = (i for i in [0..10] when i not in even_nums)

console.log even_nums ## prints '0, 2, 4, 6, 8'
console.log odd_nums ## prints '1, 3, 5, 7, 9'
```

Versus Javascript:
```javascript
(function() {
  var even_nums, i, odd_nums,
    __indexOf = [].indexOf || function(item) { for (var i = 0, l = this.length; i < l; i++) { if (i in this && this[i] === item) return i; } return -1; };

  even_nums = (function() {
    var _i, _results;
    _results = [];
    for (i = _i = 1; _i <= 10; i = ++_i) {
      if (i % 2 === 0) {
        _results.push(i);
      }
    }
    return _results;
  })();

  odd_nums = (function() {
    var _i, _results;
    _results = [];
    for (i = _i = 1; _i <= 10; i = ++_i) {
      if (__indexOf.call(even_nums, i) < 0) {
        _results.push(i);
      }
    }
    return _results;
  })();

  console.log(even_nums);

  console.log(odd_nums);

}).call(this);
```

<b>Typescript</b><br/>
Made by Microsoft, Typescript aims to make debugging easier, and to enforce safety at compile time (catching mistakes).

<b>Livescript</b><br/>
A very functional compiling language, it too is aimed at simplifying Javascript. 

In this example, the function `increment` is defined and executed:

```livescript
add = (x, y) --> x + y
add 11, 9       ##=> 20
increment = add 1
increment 11    ##=> 12
```