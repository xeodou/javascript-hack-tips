### JavaScripts hack tips
This repository is a collection for some usage tips in JavaScripts.Maybe some you have used before, some you have seen in some one's code but you nevet give it a try. :) Maybe you should. 

If you want help send a PR. :)

#### 1. `~[].indexOf('value')`
`~` is **Bitwise NOT** operator, see more information [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators#Bitwise_NOT). `~1 === 0` always `true`. This is a smart way to check if an array contain something.

#### 2. `[]`
Sometimes you want use `Array.prototype`, keep in mind you can use `[]` instead. You can see the comparison [here](http://jsperf.com/array-perf-prototype-vs-literal/2), it's almost the same.

#### 3. `[].concat` or `array.slice` or `array.concat`
You can use some npm module to do deep clone, but use native function is a simple way to copy a array without reference. See why [here](http://stackoverflow.com/questions/728360/most-elegant-way-to-clone-a-javascript-object)
example:
```
var b = ['a', 'b']
var a = [].concat(b) 
// or a = b.slice()
// or a = b.concat()
// a = ['a', 'b']
a[0] = 'A'
// a = ['A', 'b']
// b = ['a', 'b']
```
