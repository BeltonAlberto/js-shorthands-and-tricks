# Important-js-shorthands
I’ve collected this important JavaScript shorthands and techniques as a crucial reference for those who utilize Javascript in day-to-day coding.
I've been using them throughout my journey as a Javascript coder.

## 1. The Ternary Operator
This is a great code saver when you want to write one-Liner `if-else`` Statements.

### Longhand:
```javascript
const myAge = 21;
let answer;

if (myAge > 30) {
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
const answer = myAge > 30 ? "above 30" : myAge < 20 ? "below 20" : "between  30 - 20";
```
Keep in mind that this kind of shorthand is meant to make the code cleaner and save code lines in simple if-else statements like the one above. Don’t overuse it, as it can make the code less readable!

## References
1. * [Artturi Jalli](https://betterprogramming.pub/25-useful-javascript-shorthands-for-web-developers-771ac550a7ba)
2. * [Michael Wanyoike](https://www.sitepoint.com/shorthand-javascript-techniques/)
