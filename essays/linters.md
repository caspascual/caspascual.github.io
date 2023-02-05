---
layout: essay
type: essay
title: "Clean up, clean up! Everybody, everywhere!"
# All dates must be YYYY-MM-DD format!
date: 2023-02-04
published: true
labels:
  - ESLint
  - Coding Standards
---
Let’s be honest, no one likes messes. They’re problematic and an eyesore but sometimes we’re too busy with one thing to deal with them. Other times, we’re too lazy and it gets expensive to hire someone else to fix your mess. Luckily for messy programmers, however, there are free and easy tools that touch your code up a notch.

## The Virtual Janitor

These magical tools are called linters. They’re used to implement coding standards, remove those problematic formatting errors, and make it all look clean. The name originates from the original tool “Lint” which analyzed bugs and errors in the C programming language. There are numerous linters for every programming language out there. ESLint is one example of a linter made for Javascript programmers.

For a few days now, I’ve been coding Javascript with ESLint and my code has had an astounding improvement in how it looks. 

From this:
```
function sumFor(arr){
  let sum = 0;
  for (let i = 0; i<arr.length;i++){
    sum += arr[i];
  } return sum;
}
function sumWhile(arr){
  let sum = 0;
  let i = 0;
  while(i<arr.length){
    sum += arr[i];
    i++;
  } return sum;
}
function sumRecursion(arr){
  if(arr.length == 0){
    return 0;
  } return arr.pop()+sumRecursion(arr);
}
function sumTheSimpleWay(arr){
  const sum = _.reduce(arr, function(memo, num){return memo+num});
  return sum;
}

const numbers = [1, 2, 3, 4, 5];
console.log(sumFor(numbers));
console.log(sumWhile(numbers));
console.log(sumRecursion(numbers));
console.log(sumTheSimpleWay([1, 2, 3, 4, 5]));
```
To this:
```
function sumFor(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}

function sumWhile(arr) {
  let sum = 0;
  let i = 0;
  while (i < arr.length) {
    sum += arr[i];
    i++;
  }
  return sum;
}

function sumRecursion(arr) {
  if (arr.length === 0) {
    return 0;
  }
  return arr.pop() + sumRecursion(arr);
}

function sumTheSimpleWay(arr) {
  const sum = _.reduce(arr, function (memo, num) { return memo + num; });
  return sum;
}

const numbers = [1, 2, 3, 4, 5];

console.log(sumFor(numbers));
console.log(sumWhile(numbers));
console.log(sumRecursion(numbers));
console.log(sumTheSimpleWay([1, 2, 3, 4, 5]));
```
## The Positives

With ESLint, it’s been much easier to navigate my code. Everything is spaced out neatly and very readable. No more cluttered messes or having to get closer to my screen to read my code. I’m certain that my TA and professor for my ICS314 class are happy they don’t have to read ugly code anymore. 

ESLint has also made it very easy to catch errors and resolve them. It will highlight exactly where the error is and has options to automatically resolve them. Neat right? It makes things so much easier and faster to press a key bind to resolve errors rather than writing the whole line. Sure, for those with speedy fingers, it only saves a few seconds but if you make a lot of mistakes, those few seconds will build up. Those extra seconds are handy for when I’m programming on a time limit.

## The Negative

My only caveat with linters was the learning curve. If you’re a perfectionist like me, you might find it annoying to see a red error on a simple formatting error that won’t cause a compilation error. When I first used ESLint on a simple task I was doing, I found myself slowing down to fix the tiniest of formatting errors before continuing on to the next function. It felt like ESLint was just hindering my productivity.

## Final Thoughts

Once you get past that initial hurdle, linters become your best friend. You can type away on your keyboard without any worry of errors because the linter will catch and automatically fix them for you. They’re a powerful and helpful tool just like that rubber ducky on your desk.
