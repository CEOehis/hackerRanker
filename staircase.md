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

function stairs(n) {
  //given an integer n; on first line, print n-1 spaces then n; second line print n-2 spaces then n ...last line print n-n spaces then n
    let result = '';
    for(let i = 1; i <= n; i ++) {
      result += (' '.repeat(n-i) + '#'.repeat(i) + '\n');
    }
    return result;
}

function main() {
    var n = parseInt(readLine());
    
    console.log(stairs(n));

}
```
