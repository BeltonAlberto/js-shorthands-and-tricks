# **some-Important-js-shorthands** :blush:
![TJavaScript random icon!](https://github.com/BeltonAlberto/js-shorthands-and-tricks/blob/main/image/Alecive-Flatwoken-Apps-File-Javascript.ico?raw=true)

**I’ve collected this important JavaScript shorthands and techniques as a crucial reference for those who utilize Javascript frequently. I've implemented them throughout my journey as a Javascript coder. If you're senior dev some of them may seem quite obvious though**

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
let x, y, z = 3;
```
##### Or either
```javascript
let x,
    y,
    z = 3;
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
You can also nest your `if` statements like this:
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
#### Classic Form
```javascript
const hasNumber1 = numbers.indexOf(1) > -1 // -> True
const hasNumber2 = numbers.indexOf(1) === -1 // -> False
```
#### Cleaner Approach

```javascript
const hasNumber1 = numbers.includes(1)     // -> True
```

## 4. Check Multiple Conditions
To avoid long `||` chains when checking multiple conditions, you can use what you just learned in the previous tip — that is, using the includes() method instead:

```javascript
const num = 1;
```
#### Longhand
```javascript
if(num == 1 || num == 2 || num == 3){
  console.log("Yay");
}
```
#### Shorthand
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
#### Shorthand:
```javascript
const variable2 = variable1  || 'new';
```

## 6.  If Presence Shorthand
This might be trivial, but worth a mention. When doing “`if` checks”, assignment operators can sometimes be omitted
#### Longhand
```javascript
if (likeJavaScript === true)
```
#### Shorthand
```javascript
if (likeJavaScript)
```
## 7 .Destructuring Assignment Shorthand
This one is priceless, allow us to assign Multiple Values Using One Line.
```javascript
let num1, num2;
```
#### Longhand
```javascript
num1 = 10;
num2 = 100
```
#### Shorthand
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
#### Longhand
```javascript
let temp = x;
x = y;
y = temp;
```
#### Shorthand
```javascript
[x, y] = [y, x];
```
## 8. Assign Multiple Variables to the Same Value
#### Longhand
```javascript
    let a = 10,
        b = 10,
        c = 10;
```
#### Shorthand
```javascript
    let a = b = c = 10;
```
## 9. Double Bitwise `NOT` Shorthand
Bitwise operators are one of those features you learn about in beginner JavaScript tutorials and you never get to implement them anywhere. Besides, who wants to work with ones and zeroes if you are not dealing with binary?

There is, however, a very practical use case for the Double Bitwise NOT operator. You can use it as a replacement for `Math.floor()`. The advantage of the Double Bitwise NOT operator is that it performs the same operation much faster. You can read more about Bitwise operators here.

#### Longhand
```javascript
Math.floor(4.9) === 4  //true
```
#### Shorthand
```javascript
~~4.9 === 4  //true
```
## 10. The Spread Operator
You can “spread” the elements of an array into another array by using the spread operator `(…)`. For example, let’s concatenate two arrays of numbers:
```javascript
const nums1 = [1, 2, 3];
const nums2 = [4, 5, 6];
```
#### Longhand
```javascript
let newArray = nums1.concat(nums2);
```
#### Shorthand
```javascript
newArray = [...nums1, ...nums2];
```

   ### . This syntax can also be used instead of pushing values to an array:
```javascript
let numbers = [1, 2, 3];
```
#### Longhand
```javascript
numbers.push(4);
numbers.push(5)
```
#### Shorthand
```javascript
numbers = [...numbers, 4, 5];
```
## 11. Check if an Item Is in an Array
This one is not necessarily a shorthand, as you barely save a couple of characters. But it is a way cleaner approach.

Instead of using the `indexOf()` method to check if an element is in the array, you can use the `includes()` method. This makes your intent very clear
```javascript
let numbers = [1, 2, 3];

// LONGER FORM
const hasNumber1 = numbers.indexOf(1) > -1 // -> True
const hasNumber2 = number.indexOf(1) != -1 // -> True

// CLEANER APPROACH
const hasNumber1 = numbers.includes(1)     // -> True
```

## 12. Convert String to Number
You can use the unary operator `(+)` to convert a string to a number:
#### Longhand
```javascript
const num = parseInt("1000")
```
#### Shorthand
```javascript
const num = +"1000";
```
## References
1. * [Artturi Jalli](https://betterprogramming.pub/25-useful-javascript-shorthands-for-web-developers-771ac550a7ba)
2. * [Michael Wanyoike](https://www.sitepoint.com/shorthand-javascript-techniques/)
