# Array Functions
## Loops
### array.forEach()
Loops over each element in array
```
array.forEach((element, index, array) => { ... } )
```
### array.map() 
Returns modified array
```
const map01 = array.map(x => x * 2);
```
### array.filter() 
Returns an array of items which passes the test condition in the callback function.
```
const result = array.filter((item,index,array) => item > 6);
```
### for...of
```
for (const element of array1) {
  console.log(element);
}
```
## Manipultaion
### Slice
- array.slice(startIndex, endIndex)
- does not mutate the array
- returns the sliced array
```
array.slice(2,3); // ["r"]
```
### Splice 
- array.splice(startIndex, deleteCount)
- array.splice(startIndex, deleteCount, optional: elements to replace the removed place)
- Mutates the array
- returns the removed element
```
array = [1,2,3,4,5,6,7,8,9]
array.splice(2,4,1,2,3) // returns [3, 4, 5, 6]
console.log(array) // prints [1, 2, 1, 2, 3, 7, 8, 9]
```
### Shift
Removes element from start
```
array.shift()
```
### UnShift
Adds element at the beginning of an array. can take any number of elements
```
array.unshift(element0, element1, ... , elementN)
```
### Pop
Remove one element from the end of array
### Push
Adds elements to the end of array
```
array.push(element0, element1, ... , elementN)
```
## Get and Set
### array.includes(value)
Returns Boolean. Checks wehether the array has the value or not.
### indexOf()
Returns the first index at which a given element can be found in the array, or -1 if it is not present.
```
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];
console.log(beasts.indexOf('bison')); // expected output: 1
// start from index 2
console.log(beasts.indexOf('bison', 2)); // expected output: 4
console.log(beasts.indexOf('giraffe')); // expected output: -1
```
### lastIndexOf()
Returns the last index an element is present in array
```
const animals = ['Dodo', 'Tiger', 'Penguin', 'Dodo'];
console.log(animals.lastIndexOf('Dodo')); // prints 3
```
### Get Last item
```
const beast = ['ant', 'bison', 'camel', 'duck', 'bison'];
// method 1
beast[beast.length-1]
// method 2
beast.slice(-2) // returns last two elements of array. -1 means last element of array and so on
```
### find() Find first element by condition
The find() method returns the value of the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, undefined is returned.
```
const array1 = [5, 12, 8, 130, 44];
const found = array1.find(element => element > 10); // 12
```
### some()
The some() method tests whether at least one element in the array passes the test implemented by the provided function.
``` 
const array = [1, 2, 3, 4, 5];
// checks whether an element is even
const even = (element) => element % 2 === 0;
console.log(array.some(even));
// expected output: true
```
### every()
The every() method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
```
const isBelowThreshold = (currentValue) => currentValue < 40;
const array1 = [1, 30, 39, 29, 10, 13];
console.log(array1.every(isBelowThreshold));
// expected output: true
```

# Object Functions
## Loop over an object
### for...in
The for...in statement iterates over all enumerable properties of an object that are keyed by strings (ignoring ones keyed by Symbols), including inherited enumerable properties.
```
const object = { a: 1, b: 2, c: 3};

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}
// expected output:
// "a: 1"
// "b: 2"
// "c: 3"

```

## Get all keys of an Object as Array
```
const obj = {a:1,b:2,c:3}
Object.keys(obj)  // ["a", "b", "c"]
```

## Get all values of an Object as Array
```
const o = {a:1,b:2,c:3}
Object.values(obj)  // [1,2,3]
```

## Add a new property to Object
```
const obj = {a:1,b:2,c:3}
obj.d = 4
console.log(obj) // {a: 1, b: 2, c: 3, d: 4}
```

## Delete a property from Object
```
const obj = {a:1,b:2,c:3}
delete obj.c
console.log(obj) // {a: 1, b: 2}
```

