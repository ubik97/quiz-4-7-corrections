# Quiz 4-7 Corrections


**Quiz 4**

None: I couldn't tell what was wrong with the algorithm


**Quiz 5**

###Question 1:

*Consider the following statements.

let x = 43;
let y = "43";

if ( / missing condition / ) {
    console.log("x and y have equivalent values and data types.");
}

if ( / missing condition / ) {
    console.log("x and y have different values or different data types.");
}
Which two expressions satisfy the missing conditions above?*

The  correct answer is:
x === y
x !== y

Explanation:
The console.log statement in the first if statement states that x and y have strict equality (equal in value and data type, such as string, number, boolean, etc). The first missing condition must therefore be x === y, as this is true when x and y are equal in value and data type.

For the second if statement, the message will be logged to the console if x and y do not have equal values and data types. x !== y is the missing condition because it will return true if either the value or the data type of x and y are not equal.

###Question 2:

*Which of the following are valid relational operators in JavaScript? Select all that apply.*

Correct Answers:
I got all of them correct except for '=', which I didn't select

Explanation:
Relational operators assess the relationship (equality,  data types, greater than/less than, etc) between two values or variables. The '=' operator is clearly a relational operator because it tests whether the things be ing compared are equal in value and returns true if they are.

###Question 3:

*Which of the following are valid logical operators in JavaScript? Select all that apply.*

Correct Answer:
I got all of the correct answers, but I also selected '?' which is incorrect.

Explanation:
The question was asking for logical operators, like || or &&. '?' is a ternary operator, which means that it returns a unique predetermined value based on a given condition, like an if statement. Logical operators don't do this, they determine the logic of a condition.

###Question 10:

*Consider the following code segment, which is designed to assign a status of HR or ND to each student (given their marking period grades).

let status;
if (studentGrade >= 88) {
    status = "HR";
} else {
    status = "ND";
}
Select the ternary operator that effectively replaces the above if-else statement. Select all that apply.*

Correct Answer:
I got all of the correct answers except for: let status = (studentGrade < 88) ? "ND" : "HR";

Explanation:
This line is correct because it follows the proper syntax of a single line if statement. When the statement is true, or when studentGrade is lower than an 88, status will equal "ND", thus properly fulfilling the objective of the algorithm.

###Question 13:

*Anything written in the form a while (or do...while) loop can be achieved with an equivalent for loop and vice-a-versa.*

Correct Answer:
True

Explanation:
The main difference between a for and while loop is that the for loop is guaranteed to run, where as the while loop will not run if its condition is not true initially. A do...while loop, however, is gauranteed to run at least once. Thus, a for loop can be constructed to work the same as any do...while loop and vice-a-versa.


**Quiz 6**

##Question 6:

*Consider the following function, and its subsequent calls.

function doSomeStuff(a, b, c) {
   console.log("I need to do " + a + ", " + b + ", and " + c + "... So busy!");
}

doSomeStuff("homework", "chores", "more homework");
doSomeStuff("chores", "homework");
doSomeStuff("homework", "homework", "more homework", "oh, and chores, too");
Select the statements that will be logged to the console. Choose all that apply.*

I answered:

I need to do homework, homework, and more homework...oh, and chores, too! So busy!
  Explanation: The function doSomeStuff(a, b, c) only has 3 parameters. This means that "oh, and chores, too" will be ignored, as the function doesn't have a fourth parameter for it to fill. This answer is wrong.

I need to do chores, homework, and... So busy!
  Explanation: When one of the parameters is not filled, it will have the value undefined and will print as such. This doesn't print undefined so it is wrong.

I need to do homework, chores, and more homework... So busy!
  I got this one and it was correct.

Correct Answers:

I need to do chores, homework, and undefined... So busy!
  Explanation: This is correct because only two parameters are supplied in the second instance in which the function is called, thus the third unfilled one will have a value of undefined and will print as such.

I need to do homework, homework, and more homework... So busy!
  Explanation: This is correct because in the third instance in which the function is called, the first three prameters will be taken and printed and the fourth will be excluded.

##Question 8:

*Consider the following function.

function divide() {
    let a = Number(prompt("Enter a number."));
    let b = Number(prompt("Enter another number."));

    return a / b;
}
I want to modify the function so that it accepts as parameters the values being divided. Which of the following revisions achieves this?*

Correct Answer:
function divide(a, b) {
    return a / b;
}

Explanation:
This function will take a, b (which are presumably set as user inputs in a separate function) and then return the value of a / b.

function divide(a, b) {
    let a = Number(prompt("Enter a number."));
    let b = Number(prompt("Enter another number."));

    return a / b;
}
This is the answer I selected. It's wrong because it takes a and b as parameters and then changes their values by reprompting the user.


##Question 14:

*Consider the following code snippet.

function example(a, b, c) {
    if (a === 1) {
        if (b === 2) {
            if (c === 3) {
                var d = 4;
            }
        }
    }

    console.log(d);
}
What is the result of executing this code?*

Correct Answer:
4 or undefined will be printed to the console.

Explanation:
There are two possible scenarios: either all of the conditions of the if statements will return true and d will be set to 4 and then logged to the console, or, if any of the if statements do not return true, d will be left undefined and undefined will be logged to the console.

**Quiz 7**

##Question 8:

*Consider the following code segment.

let cars = [ "Audi", "BMW", "Mercedes", "Porsche", "Volkswagen" ];
let car = prompt("What kind of car do you drive?");

if (/* missing */) {
    console.log("You drive a German-made car.");
}
The console.log statement should only execute if the user enters a value that exists in the cars array. Which of the following are possible replacements for /* missing */ that will achieve this goal?*

Correct Answer:
cars.lastIndexOf(car) !== -1
  Explanation: This is correct because the lastIndexOf function will not return -1 when car is in the array (meaning it has an index in the array).

cars.indexOf(car) !== -1
  Explanation: This is correct because the indexOf function will also not return -1 when car is in the array.


cars.includes(car)
  I selected this answer.

##Question 13:

*Consider the following incomplete function, which is designed to accept an array of elements and print each one to the screen one-by-one.

function printAll(list) {
    /* missing */
}
Which of the following can serve as suitable replacements for /* missing */ to achieve the goal of this function? Select all that apply.*

Correct Answer:
for (let i = 0; i < list.length; i++) {
    console.log(list[i]);
}
  I got this one right.

for (let item of list) {
    console.log(item);
}
  Explanation: In this for... of loop, item is set to the value of the index of the array that is currently being iterated over. Thus in order to log the value at each index to console, you can simply log item. I was incorrect and chose the answer that used item as a counter variable in the for...of  loop (list[item]), which doesn't work because item is the value of the array at a given index, not the index itself.
