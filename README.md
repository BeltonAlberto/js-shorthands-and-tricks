# Important-js-shorthands
I’ve collected this important JavaScript shorthands and techniques as a crucial reference for those who utilize Javascript in day-to-day coding.
I've been using them throughout my journey as a Javascript coder.

## 1.  Declaring Variables Shorthand
It’s good practice to declare your variable assignments at the beginning of your functions. This shorthand method can save you lots of time and space when declaring multiple variables at the same time.

#### Longhand:
```javascript
let x;
let y;
let z = 3; 
```
#### Shorthand:
```javascript
let x, y, z=3;
```
## 2.  The Ternary Operator
This is a great code saver when you want to write one-Liner `if-else`` Statements.

#### Longhand:
```javascript
const myAge = 21;
let answer;

if (myAge > 30) {
    answer = "above 30";
} else {
    answer = "below 30";
}
```
#### Shorthand:

```javascript
const answer = myAge > 30 ? "above 30" : "below 30";
```
You can also nest your `if` statement like this:
```javascript
const answer = myAge > 30 ? "above 30" : myAge < 20 ? "below 20" : "between  30 - 20";
```
Keep in mind that this kind of shorthand is meant to make the code cleaner and save code lines in simple if-else statements like the one above. Don’t overuse it, as it can make the code less readable!

## 3.  Check if an Item Is in an Array
This one is not necessarily a shorthand, as you barely save a couple of characters. But it is a way cleaner approach.

Instead of using the classic `indexOf()` method to check if an element is in the array, you can use the `includes()` method. This makes your intent very clear:

```javascript
let numbers = [1, 2, 3];
```
#### CLASSIC FORM
```javascript
const hasNumber1 = numbers.indexOf(1) > -1 // -> True
```
#### CLEANER APPROACH

```javascript
const hasNumber1 = numbers.includes(1)     // -> True
```

## 4. Check Multiple Conditions
To avoid long || chains when checking multiple conditions, you can use what you just learned in the previous tip — that is, using the includes() method instead:

```javascript
const num = 1;
```
#### LONGHAND
```javascript
if(num == 1 || num == 2 || num == 3){
  console.log("Yay");
}
```
#### SHORTHAND
```javascript
if([1,2,3].includes(num)){
  console.log("Yay");
}
```
## 5. Short-circuit Evaluation Shorthand
When assigning a variable value to another variable, you may want to ensure that the source variable is not null, undefined, or empty. You can either write a long `if` statement with multiple conditionals, or use a short-circuit evaluation.
#### Longhand:
```javascript
if (variable1 !== null || variable1 !== undefined || variable1 !== '') {
     let variable2 = variable1;
}
```
### Shorthand:
```javascript
const variable2 = variable1  || 'new';
```

## 6.  If Presence Shorthand
This might be trivial, but worth a mention. When doing “`if` checks”, assignment operators can sometimes be omitted
#### LONG FORM
```javascript
if (likeJavaScript === true)
```
#### SHORTHAND
```javascript
if (likeJavaScript)
```
## 7 .Destructuring Assignment Shorthand
This one is priceless, allow us to assign Multiple Values Using One Line.
```javascript
let num1, num2;
```
#### LONGHAND
```javascript
num1 = 10;
num2 = 100
```


###SHORTHAND
```javascript
[num1, num2] = [10, 100];
```


 ### Swap Two Variables Without a Third
This one is a classic.
This can also be used to swap two variables without a third helper:
```javascript
let x = 1;
let y = 2;
```
#### LONGHAND
```javascript
let temp = x;
x = y;
y = temp;
```


###SHORTHAND
```javascript
[x, y] = [y, x];
```



#### LONGHAND
```javascript

```


###SHORTHAND
```javascript

```



## References
1. * [Artturi Jalli](https://betterprogramming.pub/25-useful-javascript-shorthands-for-web-developers-771ac550a7ba)
2. * [Michael Wanyoike](https://www.sitepoint.com/shorthand-javascript-techniques/)
