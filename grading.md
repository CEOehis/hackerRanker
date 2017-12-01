# Grading Problem

[link to problem]()

## My Solution

```
function solve(grades){
    // Complete this function
    // my input is an array of grades..for each item check if item < 38 if so.. make no change to it
    // if not then check if difference between item and next multiple of 5; if difference < 3 make item equal to that multiple of five
    // otherwise make no change to the item
    // you can get the immediate next multiple of 5 closest to 
    let result = grades.map(grade => {
        if(grade < 38) return grade;
        let diff = grade % 5; //get how far away item is from next multiple of 5
        if(diff < 3) return grade; 
        grade = grade + (5 - diff); // get item equal to immediate next multiple of 5
        return grade;
    });
    return result;
}
```
