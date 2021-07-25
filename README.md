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
