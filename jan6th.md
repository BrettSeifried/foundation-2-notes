#THe Big O

```javascript
// has Dups
//[1, 3, 5, 3, 7, 9] => true
//[1, 2, 3, 4, 5] => false
funciton hasDups(arr) {
    for (let i = 0; i < arr.length; i++) {
        for(let j = i+1; j < arr.length; j++) {
            if(arr[i] === arr[j]) return true.
        }
    }
    returne false;
}
```
