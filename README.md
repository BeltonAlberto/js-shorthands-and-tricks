# Important-js-shorthands
I’ve collected this important JavaScript shorthands and techniques as a crucial reference for those who utlize Javascript in day-to-day coding language and 
I've been using them throughout my journey as a developer.

## 1. The Ternary Operator
This is a great code saver when you want to write an if..else statement in just one line.

### Longhand:
```javascript
const myAge = 21;
let answer;

if (myage > 30) {
    answer = "above 30";
} else {
    answer = "below 30";
}
```
### Shorthand:

```javascript
const answer = myAge > 30 ? "above 30" : "below 30";
```
You can also nest your `if` statement like this:
```javascript
const answer = myage > 30 ? "above 30" : myAge < 20 ? "below 20" : "between  30 - 20";
```
