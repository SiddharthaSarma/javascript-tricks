# javascript-tricks
javascript tricks

## Arrays

### Union of arrays
```javascript
let a = [1, 2, 3, 4, 5];
let b = [3, 4, 5, 6, 7];

let result = [...new Set([...a, ...b])]; // [1, 2, 3, 4, 5, 6, 7]
```

### Intersection of arrays
```javascript
let a = [1, 2, 3, 4, 5];
let b = [2, 3, 4, 6];

let result = a.filter(val => ~b.indexOf(val)); // [2, 3, 4]
 ```

### Get non intersected values
```javascript
let a = [1, 2, 3, 4, 5];
let b = [2, 3, 4, 6];

let result = a.filter(val => !~b.indexOf(val)); // [1, 5]
 ```
 
## Strings

### Reverse a string

```javascript
let str = str.split('').reverse().join('');
```
### Replace a character at a particular index

```javascript
function replaceAt(str, i, char) {
  return s.substring(0, i) + char + str.substring(i + 1);
}
```
### Remove last character in a string
```javascript

// using substring
str.substring(0, str.length - 1);

// using slice
str.slice(0, -1)
