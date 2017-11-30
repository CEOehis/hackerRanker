# Birthday Cake Candles problem

[link to problem]()

## My solution 

```
function birthdayCakeCandles(n, ar) {
    // Complete this function
    // get the total number of candles, then count the number of tallest candles. This is the result
    let tallestCandle = ar.reduce((a,b) => Math.max(a,b));
    return ar.filter(candle => candle == tallestCandle).length;
```

The solution below seemed to fail when the number of items passed in ```ar``` was very large :-/

```
function birthdayCakeCandles(n, ar) {
    // Complete this function
    // get the total number of candles, then count the number of tallest candles. This is the result
    let candlesSorted = ar.sort((a,b) => a < b);
    return candlesSorted.filter((v) => v == candlesSorted[0]).length;
}
```
