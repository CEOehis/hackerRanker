# Time conversion problem 

[link to problem]()

## My solution

```
function timeConversion(s) {
    // Complete this function
    // get hours from time; get time of day from time i.e am/pm; if am print time as is ; if pm add 12 to hours , if new hours value is 24 print hours as 00; otherwise just print time with new hours
    let hours = s.slice(0,2);
    const minutes = s.slice(3,5);
    const seconds = s.slice(6,8);
    const timeOfDay = s.slice(-2);
    
    if (timeOfDay == 'AM' && hours != '12') return `${hours}:${minutes}:${seconds}`;
    if(timeOfDay == 'PM' && hours == '12') return `${hours}:${minutes}:${seconds}`;
    hours = Number(hours);
    hours = hours + 12;
    hours = hours == 24 ? '00' : hours;
    
    return `${hours}:${minutes}:${seconds}`;
}
```
