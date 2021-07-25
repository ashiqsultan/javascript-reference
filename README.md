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








