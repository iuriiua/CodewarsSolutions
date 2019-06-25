# 8 KYU

## Abbreviate a Two Word Name

Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.
The output should be two capital letters with a dot seperating them.
It should look like this:
Sam Harris => S.H
Patrick Feeney => P.F

```javascript
function abbrevName(name) {
  let b = name.split(' ');
  let c = b[0][0] + '.'+ b[1][0];
  return c.toUpperCase();
}
```
## Third Angle of a Triangle

You are given two angles (in degrees) of a triangle.
Write a function to return the 3rd.
Note: only positive integers will be tested.

```javascript
function otherAngle(a, b) {
  let third = 180 - a - b;
  return third;
}
```

## String repeat

Write a function called repeatStr which repeats the given string string exactly n times.

```javascript
function repeatStr(n, s) {
  let res = '';
  for (let i = 1; i <= n; i++) {
    res += s;
  }
  return res;
}
```

## Counting sheep...

Consider an array of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

```javascript
function countSheeps(arrayOfSheep) {
  let i = 0;
  let found = arrayOfSheep.find(function(element) {
    if (element == true) {
      i++;
    }
  });
  return i;
}
```

## Sum of positive

You get an array of numbers, return the sum of all of the positives ones.

Example [1,-4,7,12] => 1 + 7 + 12 = 20

Note: if there is nothing to sum, the sum is default to 0.

```javascript
function positiveSum(arr) {
  let sum = 0;
  for (i = 0; i <= arr.length - 1; i++) {
    if (arr[i] >= 0) {
      sum += arr[i];
    }
  }
  return sum;
};
```

## Convert a Boolean to a String

In this programming exercise, you're going to learn about functions, boolean (true/false) values, strings, and the if-statement.

A function is a block of code that takes an input and produces an output. In this example, boolean_to_string is a function whose input is either true or false, and whose output is the string representation of the input, either "true"/"True" or "false"/"False" (check the sample tests about what capitalization to use in a given language).

A common idea we often want to represent in code is the concept of true and false. A variable that can either be true or false is called a boolean variable. In this example, the input to boolean_to_string (represented by the variable b) is a boolean.

Lastly, when we want to take one action if a boolean is true, and another if it is false, we use an if-statement.

For this kata, don't worry about edge cases like where unexpected input is passed to the function. You'll get to worry about these enough in later exercises.

```javascript
function booleanToString(b) {
  if (b == true) {
    return 'true';
  } else {
    return 'false';
  }
};
```

## Remove First and Last Character

It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry with strings with less than two characters.

```javascript
function removeChar(str) {
  let newStr = str.slice(1, str.length -1);
  return newStr;
};
```

## Reversed Words

Complete the solution so that it reverses all of the words within the string passed in.

Example:

reverseWords("The greatest victory is that which requires no battle")
// should return "battle no requires which that is victory greatest The"

```javascript
function reverseWords(str) {
  let strSplit = str.split(' ')
  let newStr = [];
  for (let i = strSplit.length - 1; i >= 0; i--) {
    newStr.push(strSplit[i]);
  }
  return newStr.join(' ');
}
```

## Vowel remover

Create a function called shortcut to remove all the lowercase vowels in a given string.

Examples
shortcut("codewars") // --> cdwrs
shortcut("goodbye")  // --> gdby
Don't worry about uppercase vowels.

```javascript
function shortcut(string) {
  let res = Array.from(string);
  let letters = ["a", "e", "o", "i", "u"];
  let newArray = [];

  for (let i = 0; i < res.length; i++) {
    if (letters.includes(res[i]) === false) {
      newArray.push(res[i]);
    }
  }
  let newArrayStr = newArray.join("");
  return newArrayStr;
}
```

## Square(n) Sum

Complete the square sum function so that it squares each number passed into it and then sums the results together.

For example, for [1, 2, 2] it should return 9 because 1^2 + 2^2 + 2^2 = 9.

```javascript
function squareSum(numbers) {
  let sum = 0;
  let temp = 0;

  for (let i = 0; i < numbers.length; i++) {
    temp = numbers[i] ** 2;
    sum = sum + temp;
  }
  console.log(sum);
  return sum;
}
```

## Multiply

The code does not execute properly. Try to figure out why.

```javascript
function multiply(a, b){
  return a * b;
}
```