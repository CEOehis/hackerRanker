# Min Max-Sum problem

[link to problem](https://www.hackerrank.com/challenges/mini-max-sum/problem)

## My solution

```
process.stdin.resume();
process.stdin.setEncoding('ascii');

var input_stdin = "";
var input_stdin_array = "";
var input_currentline = 0;

process.stdin.on('data', function (data) {
    input_stdin += data;
});

process.stdin.on('end', function () {
    input_stdin_array = input_stdin.split("\n");
    main();    
});

function readLine() {
    return input_stdin_array[input_currentline++];
}

/////////////// ignore above this line ////////////////////
function minMax(arr) {
    //arrange the numbers from least to max in ascending order, then sum the first four items as minimum, sum the last four items as maximum
    let arrSorted = arr.sort((a,b) => b < a); 
    let min = arrSorted.slice(0,4).reduce((sum, next) => sum + next);
    let max = arrSorted.slice(1).reduce((sum,next) => sum + next);
    return `${min} ${max}`;
}

function main() {
    arr = readLine().split(' ');
    arr = arr.map(Number);
    
    console.log(minMax(arr));
}
```
