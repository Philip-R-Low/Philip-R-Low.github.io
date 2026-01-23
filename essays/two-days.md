---
layout: essay
type: essay
title: "I learned typescript in two days. I would not recommend it."
# All dates must be YYYY-MM-DD format!
date: 2026-01-22
published: true
labels:
---
<img src="../img/two-days/typescript_logo.png">
## Why would I do this to myself?
I decided to learn typescript in two days as part of an assignment for a software engineering course I am currently taking at the University of Hawaiʻi. The professors teaching this course required students to complete [FreeCodeCamp’s course on basic JavaScript and itʻs ES6 update](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/) on Saturday after the first week of class, and to have completed [W3’s quiz on TypeScript](https://www.w3schools.com/typescript/typescript_quiz.php) on Sunday. Between classes, work, and social responsibilities, I was unable to get a head start before Friday, and had already preordered a ticket to attend an event that evening (Magic the Gathering’s Lorwyn Eclipsed Pre-release). Thus with only minimal previous experience with JavaScript, I set out to learn TypeScript in two days. 
I must admit, I somewhat regret trying to rush this, however I doubt the extra day would have made the difference. After all, as Peter Norvig said in his essay [Teach Yourself Programming in Ten Years](https://norvig.com/21-days.html) "In 24 hours you won't have time to write several significant programs, and learn from your successes and failures with them." While my time was doubled, this still was no where near enough to grasp the depths of the a programming language. I suppose if I had used AI to offload anything that did not make sense, but personally I find such uses of AI to be counter-productive to actually learning. This way may have been taxing time consuming, and I know that it was not a substitute for practicing over an extended period, but I was at least able to note what I know I did not know.
## Early Confusions
The first thing in my learning process that confused me came rather early, in variable declaration. JavaScript, and by extension TypeScript give the user three different ways to assign variables: var, let, and const. Normally I would not call something short for ‘constant’ a ‘variable’ as those terms are rather diametrically opposed in my view. However, I quickly discovered that in JavaScript, non-basic types assigned with const are not actually immutable. Consider the following:
```
const list = [0, 1, 2];
list[2] = 3;
console.log(list)
```
This code would print to the console the list [0, 1, 3] instead of the list written. JavaScript does fix this by adding a freeze method for objects, and TypeScript makes a fancier alternative by allowing entire objects or individual properties/keys to be marked as read only, but this was the first indication that JavaScript, for all its popularity, is an odd language. 
To be honest, I also initially was confused on the difference between var and let. Reading FreeCodeCamp’s introduction to ES6 gives me some confidence that I now understand the difference, but leaves me wondering why it took so long to add. As I understand it, the difference here is that variables assigned with var can overwrite any variables of the same name assigned on a larger, even global scale. If that did not make sense to you, consider the following functions:
```
function sumList (list: number[]): number {
    let sum = 0;
    for (let i = 0; i < list.length; i++) {
        sum += list[i];
    }
    return sum;
}
function nestedSum (list: unknown): number {
let sum = 0;
    for (let i = 0; i < list.length; i++) {
        if (list[i] extends number[]) {
            sum += sumList(i);
        } else {
            sum += nestedSum(list[i]);
        }
    return sum;
};
```
(I apologize if it bothers anyone that the nestedSum function will cause a runtime error on the wrong input but that’s beside the point here.) It is my understanding that if the variables sum and i had been assigned with var, sumList would override the values stored under the same names nestedSum when called, causing nestedSum to be inaccurate at best, and infinitely looping at worst. 
## Getters and Setters
Another design choice of JavaScript I do not understand is the feature of getter and setter methods added in ES6. To be more specific, I don't understand how these are more useful or any different than any other method one could create. Consider the following example from [FreeCodeCamp's lesson on the topic](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-getters-and-setters-to-control-access-to-an-object):
```
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter
  get writer() {
    return this._author;
  }
  // setter
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
```
I don't see how instead calling a getter method get_writer() or getWriter() could be that much worse to type or to remember. This is not really a big deal for me I suppose, so I guess it's good for people who do see this as an improvement, and unlike some of the features like let and ~~lambda calculus~~ arrow functions, I see why this would be a later feature to add, but it has me wondering if there is something to the feature that I missed, or if it really is just, as one of my previous professors called these kinds of shortcuts, _syntax sugar_.
## TypeScript Gives Too Many Options
Moving from JavaScript to TypeScript introduced a new catagory of confusion, namely that TypeScript introducing many new features that I know I still lack the experience to differentiate from other features. The biggest of these is my confusion over the point of separating out as a different features named tuples, interfaces, type aliases. Initially I understood these to all be effectively weaker versions of classes, and while that's not quite true, I still know I do not know why one would need or want all these variations of the same sort of idea. They all remind me of my time learnign the language oCaml, which I view to be the most interesting programming language I know. For those unfamiliar with the language, which is probably most people because it's a rather obscure language, oCaml lacks the conecept of a variable. Any value in oCaml is locked in when assigned, thus to solve most problems of moderate complexity, one must rely heavily on enums, constructed types, and recursion. (Anyone concerned with the requirement of recursion should be assured, however, this lack in variable makes recursive depth easier to handle upon interpretation.)
