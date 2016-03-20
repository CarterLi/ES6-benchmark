# ES6-benchmark

A benchmark for some popular ES6 features in Node.js 5.9.0.

## Env

 - OS: OS X El Capitan 10.11.3
 - CPU: 2.6 GHz Intel Core i5
 - Memory: 8GB 1600 MHz DDR3
 - Node.js: 5.9.0

## Benchmark

[concat-strings.js](benchmarks/concat-strings.js)

```
template string vs use +
  18,110,057 op/s  » ${a}${b}
  141,356,943 op/s » a + b
```

[for-of-for-loop.js](benchmarks/for-of-for-loop.js)

```
for...of vs for loop
  1,380,990 op/s  » for...of
  21,700,943 op/s » for loop, i < arr.length
```

[merge-objects.js](benchmarks/merge-objects.js)

```
merge objects
  986,820 op/s    » Object.assign
  35,576,367 op/s » for...in loop and assign
```

[declear-class.js](benchmarks/declear-class.js)

```
declear a class
  177,907 op/s » Class
  333,660 op/s » use function and prototype
```

[repeat-string.js](benchmarks/repeat-string.js)

```
string.repeat() vs use +
  13,462,436 op/s  » string.repeat()
  171,555,037 op/s » use +
```

[array-like-to-array.js](benchmarks/array-like-to-array.js)

```
array like object to array
  1,769,649 op/s » Array.from
  781,458 op/s   » Array.prototype.slice.call
```

[promise-bluebird.js](benchmarks/promise-bluebird.js)

```
promise vs bluebird
  678,534 op/s   » promise
  3,063,186 op/s » bluebird
```

[var-let-const.js](benchmarks/var-let-const.js)

```
var let const
  198,028,614 op/s » let
  189,193,000 op/s » const
  831,460,321 op/s » var
```

[string-start-with.js](benchmarks/string-start-with.js)

```
string starts with
  14,774,987 op/s  » string.startsWith(value)
  115,127,611 op/s » string[0] === value
```

[define-a-funciton-with-this.js](benchmarks/define-a-funciton-with-this.js)

```
define a function with inherited this
  81,661,143 op/s » () =>
  76,874,220 op/s » function statement
```

[parse-int.js](benchmarks/parse-int.js)

```
global.parseInt() vs Number.parseInt()
  80,940,634 op/s  » Number.parseInt()
  111,509,873 op/s » global.parseInt()
```
