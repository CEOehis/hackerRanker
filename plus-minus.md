# Plus Minus Challenge

[Link to Challenge}(https://www.hackerrank.com/challenges/plus-minus/problem)

## My solution

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
function minusPlus(n, arr) {
    //given an array of numbers i would do this by
    // sort the array from smallest to biggest
    // count number of items that are less than 0; equal to 0; more than 0;
    // divide item set 1 by total items; item set 2 and 3 will undergo the same;
    const arraySorted = arr.sort((a,b) => b < a);
    let positive, negative, zero;
    positive = negative = zero = 0;
    for(let i = 0; i < n; i++) {
        if(arraySorted[i] < 0) negative++;
        else if(arraySorted[i] === 0) zero++;
        else if(arraySorted[i] > 0) positive++;
    }
    
    return `${(positive / n).toFixed(6)}\n${(negative / n).toFixed(6)}\n${(zero / n).toFixed(6)}`;
}

function main() {
    var n = parseInt(readLine());
    arr = readLine().split(' ');
    arr = arr.map(Number);
    
    console.log(minusPlus(n, arr));

}
