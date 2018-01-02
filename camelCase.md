# camelCase problem

[link to problem](https://www.hackerrank.com/challenges/camelcase/problem)

## My solution 

```javascript
function camelcase(s) {
    // Complete this function
    //check if string is not zero, if not, create counter and set it to one, go through the string and when you find a capital letter add one to the counter
    var counter = 0;
    if (s.length > 0) counter++;
    for(var i = 0; i < s.length; i++) {
        if(s[i].charCodeAt() >= 65 && s[i].charCodeAt() <= 90) {
            counter++;
        }
    }
    return counter;
}
```
