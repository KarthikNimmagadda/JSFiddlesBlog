---
layout: post
title: Javascript Map Method
---
Map method can be used to apply a function to a collection and return a new array. Let us consider an example.
Let's say you have four bank accounts and you want a way to double the money. Let's see how this can be achieved.

```javascript
var bankBalances = [100.9, 200.1, 300.0, 400.0];
```
The given array will only have the bank balances. The idea here is to double the bank balances and create a new array out of it.

The following code does it.

```javascript
var totalMoney = 0;
var bankBalances = [100.9, 200.1, 300.0, 400.0];
var newBalances = [];
for (var i = 0; i < bankBalances.length; i++) {
    newBalances[i] = bankBalances[i]*2;
}
alert("Array with old bank balances: " + bankBalances);
alert("Array with doubled bank balances: " + newBalances);
```

[jsfiddle](https://jsfiddle.net/karthik1239/69p4bvk7/2/)

The same output can be attained using a map.

```javascript
var bankBalances = [100.9, 200.1, 300.0, 400.0];
var newBalances = bankBalances.map(
function(currentValue) {
    return currentValue * 2;
});
alert("Array with old bank balances: " + bankBalances);
alert("Array with doubled bank balances: " + newBalances);
```
[jsfiddle](https://jsfiddle.net/karthik1239/L4fat8qd/)

The array with double the amount of bank balances. 'currentValue' is the current element in the collection.

In my next post, I will provide map methods parameters description.
Reference:
[Documentation for map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map).
