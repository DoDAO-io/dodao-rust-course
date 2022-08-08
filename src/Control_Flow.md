
# Control Flow

---

Many programming languages allow you to run some code depending on whether a condition is true, or run some code repeatedly while a condition is true. 
If expressions and loops are the most common constructs in Rust that control execution flow.

In most cases, the computer runs the code in order from the first line in the file to the last line, unless it encounters structures that alter the control flow, such as loops and conditionals.

We control the flow of our program with the following statements, in combination with relational comparison and logical operators.

* If else
* Match
* Loop
* For loop

## If Expressions
You can branch your code based on conditions using an if expression. A condition is given and then a block of code is run if the condition is met. In the event that the condition is not met, the compiler says to the machine “do not run this block."

To explore the if expression, create a new project called branches in your projects directory. Add the following code to src/main.rs:
```
fn main() {
    let number = 3;

    if number < 5 {
        println!("condition was true");
    } else {
        println!("condition was false");
    }
}
```
---

The keyword if follows a condition in all if expressions. Here, the condition checks whether the variable number is less than 5. Within curly brackets, we place the code to execute if the condition is true immediately after it.

Our program also includes an else expression, which we chose to use here, to provide an alternative block of code in case the condition is false. Unless you provide an else expression, if the condition is false, the program will skip the if block and move on.
The following output should be seen after running this code:

```
$ cargo run
   Compiling branches v0.1.0 (file:///projects/branches)
    Finished dev [unoptimized + debuginfo] target(s) in 0.31s
     Running `target/debug/branches`
condition was true
 ```

If we change the `number` to 17 we get a `condition was false` because it is not less than 5. It is a very straight forward statement.

---

### Multiple if conditions - how to evaluate them?

The two logical operators && and || allow us to evaluate more than one condition in an if statement.

Using conditional AND, you can test whether one condition and another are true. Before the code can be executed, both conditions must be met.

When AND is used to evaluate multiple conditions, the && operator is used to separate them.

```
fn main() {

    let a = 5;

    if a > 0 && a < 10 {
        println!("Both conditions are true");
    }
}
```
Due to the fact that both of our conditions are true in the example above, the code inside the if code block is executed.

It tests whether one condition or another is true by using the conditional OR. It is not necessary for both conditions to be true in order for the code to run.

The || operator is used to separate multiple conditions with OR.
```
fn main() {

    let a = 5;

    if a > 5 || a < 10 {
        println!("One of the conditions are true");
    }
}
```
---
### How to nest if, else if and else statements?

Nesting is the process of placing if statements inside other if statements. By performing the evaluations hierarchically, the compiler will start at the outer if statement and work inwards.

We nest an if statement by writing it inside the execution code block of another if statement.
```
fn main() {

    let number = 5;

    if number < 10 {
        // if outer condition proves
        // true evaluate the inner if
        if number > 0 {
            println!("Inner if statement");
        }
    }
}
```

In the example above, our outer if statement condition proves true. The compiler then evaluates the inner if statement and executes its code block if its condition proves true.

Nested if statements are used when we want to evaluate conditions only if other conditions are true.

Note that if you find yourself nesting more than 3 levels deep, you should consider finding a different method. Perhaps a loop.

---

### The conditional match statement

A single value will be compared with a list of values with the match statement. It is a bit tchnical but easy so walk with me. 

The syntax is similar to a switch statement in a language in the C family, though the syntax is different.

Taking it step by step will make it easier to understand what's going on.

1. The match statement returns a value, so we can assign the whole statement to a variable to get the result.

Example:

```  let expression_result =```

2. Now we write the match statement itself. We use the keyword match, followed by the main value we are going to compare any other values to. Finally, we define a code block.

Note that the code block is terminated with a semicolon after the closing curly brace.

Example:
```
let expression_result = match main_value {

};
```

3. Inside the code block we will write the values that we want to try and match with the main value.

First, we specify the value we want to match, followed by a => operator. Then, inside another code block, we specify the execution statements if that value matches with the main value.

Each of these values are separated with a comma, and we can have as many as we need.

The final value to match is simply an underscore. The single, standalone, underscore in a match statement represents a catch-all situation if none of the values matched to the main value. Think of it as an else statement.

Now, let’s see a practical example of the match statement.

Example:
```
fn main() {

    let grade = "B";

    let _result = match grade {
        "A" => { println!("Fantastic, you got an A!"); },
        "B" => { println!("Great job, you got a B!"); },
        "C" => { println!("Good job, you got a C"); },
        "D" => { println!("You got a D, you passed"); },
        "F" => { println!("Sorry, you failed"); },

        _ => { println!("Unknown grade, please see the teacher"); }
    };
}
```
In the example above, we give a student a grade and store it in a variable. Then we check to see which grade score in the match statement the student’s score matches.

If the compiler finds a match on the left of the ```=>``` operator, it will execute whatever statement is on the right of the ```=>``` operator.

In this case, it matched to “B” on the left and so it printed the string “Great job, you got a B!”.

Note that we don’t use the result variable in the example above. This is simply because we don’t need to, the execution statement of the match already prints a message.

If we want to return an actual value, we specify the value instead of an action like ```println```.

Example:
```
fn main() {

    let grade = "A";

    let result = match grade {
        "A" => "Excellent!",
        "B" => "Great!",
        "C" => "Good",
        "D" => "You passed",
        "F" => "Sorry, you failed",
        _ => "Unknown Grade"
    };

    println!("Grade: {} - {}", grade, result);
}
```
In the example above, we replaced the ```println!()``` statements with simple string values.

When the compiler finds a match on the left of the``` =>``` operator, it will return the value on the right of the ```=> ```into the result variable.

This time, the compiler matched to “A” on the left, so it stored the string “Excellent!” into the result variable.

We then used it in the ```println!()``` below the match statement.

---

## Loop

Throughout our application, we will often need to execute sections of code more than once.

Instead of rewriting these sections of code, we can place them in a loop and allow Rust to automatically execute them as many times as we need.

A loop consists of the following:

#### A condition
A code block containing our execution code
The compiler will evaluate the condition and based on its results, execute the code. Then, the compiler will start again at the top of the loop code and evaluate the condition again.

This cycle of iterations continue until the condition is false, or we manually stop the loop.

Rust provides us with two types of loops:

* The while loop
* The for loop
* The indefinite while loop


The while loop will continue to execute code while its condition remains true. Once the condition proves false, the while loop will stop and the compiler will move on to any code below it.

```
fn main() {

    let mut counter = 0;

    while counter < 10 {

        println!("Counter: {}", counter);
        counter += 1;
    }
}
```

It may seem a little confusing so let’s take it step by step.

First, we set up a mutable variable called `counter`. This will help us stop the loop. Next, we specify our condition that while the counter variable value is less than 10, the loop should iterate. Inside the while code block, we print out the counter number to the console.

Lastly, we add 1 to our counter variable to indicate that the loop iterated once. When we run the example, the output shows a list of numbers from 1 to 10.

Below is the expected output

```
Counter: 0
Counter: 1
Counter: 2
Counter: 3
Counter: 4
Counter: 5
Counter: 6
Counter: 7
Counter: 8
Counter: 9
```
Every time the compiler goes through the code it prints the ``` mut counter``` and add 1 to it until it is great than 10.  

#### Infinite loops

With the while loop, there is a potential danger that the loop may never stop if we make a mistake. This is known as an infinite loop and it will significantly slow down the system until the application crashes.

Let’s use our earlier example. If we remove the code that increments the counter, the condition will always prove true because the counter will stay at 0 and never get to 10 where it’s told to stop.

This section of code will cause an infinite loop

```
fn main() {

    let mut counter = 0;

    while counter < 10 {

        println!("Counter: {}", counter);
    }
}
```
#### Repeating Code with loop

The ```loop``` keyword tells Rust to execute a block of code over and over again forever or until you explicitly tell it to stop.

As an example, change the src/main.rs file in your loops directory to look like this:

```
fn main() {
    loop {
        println!("again!");
    }
}
```

When we run this program, we’ll see again! printed over and over continuously until we stop the program manually. Most terminals support the keyboard shortcut ctrl-c to interrupt a program that is stuck in a continual loop. Give it a try:

This will be the ouput
```
again!
again!
again!
again!
^Cagain!
```

The symbol ^C represents where you pressed ctrl-c . You may or may not see the word again! printed after the ^C, depending on where the code was in the loop when it received the interrupt signal.

Fortunately, Rust also provides a way to break out of a loop using code. You can place the break keyword within the loop to tell the program when to stop executing the loop. Recall that we did this in the guessing game in the “Quitting After a Correct Guess” section of Chapter 2 to exit the program when the user won the game by guessing the correct number.

We also used continue in the guessing game, which in a loop tells the program to skip over any remaining code in this iteration of the loop and go to the next iteration.

#### Returning Values from Loops

One of the uses of a loop is to retry an operation you know might fail, such as checking whether a thread has completed its job. You might also need to pass the result of that operation out of the loop to the rest of your code. To do this, you can add the value you want returned after the break expression you use to stop the loop; that value will be returned out of the loop so you can use it, as shown here:

```
fn main() {
    let mut counter = 0;

    let result = loop {
        counter += 1;

        if counter == 10 {
            break counter * 2;
        }
    };

    println!("The result is {result}");
}
```
Before the loop, we declare a variable named counter and initialize it to 0. Then we declare a variable named result to hold the value returned from the loop. On every iteration of the loop, we add 1 to the counter variable, and then check whether the counter is equal to 10. When it is, we use the break keyword with the value counter * 2. After the loop, we use a semicolon to end the statement that assigns the value to result. Finally, we print the value in result, which in this case is 20.

Loop Labels to Disambiguate Between Multiple Loops
If you have loops within loops, break and continue apply to the innermost loop at that point. You can optionally specify a loop label on a loop that we can then use with break or continue to specify that those keywords apply to the labeled loop instead of the innermost loop. Loop labels must begin with a single quote. Here’s an example with two nested loops:

```
fn main() {
    let mut count = 0;
    'counting_up: loop {
        println!("count = {count}");
        let mut remaining = 10;

        loop {
            println!("remaining = {remaining}");
            if remaining == 9 {
                break;
            }
            if count == 2 {
                break 'counting_up;
            }
            remaining -= 1;
        }

        count += 1;
    }
    println!("End count = {count}");
}
```
The outer loop has the label 'counting_up, and it will count up from 0 to 2. The inner loop without a label counts down from 10 to 9. The first break that doesn’t specify a label will exit the inner loop only. The break 'counting_up; statement will exit the outer loop. This code prints:


```
count = 0
remaining = 10
remaining = 9
count = 1
remaining = 10
remaining = 9
count = 2
remaining = 10
End count = 2
```
### For Loop

A for expression is a syntactic construct for looping over elements provided by an implementation of std::iter::IntoIterator. If the iterator yields a value, that value is matched against the irrefutable pattern, the body of the loop is executed, and then control returns to the head of the for loop. If the iterator is empty, the for expression completes.

An example of a for loop over the contents of an array:
```
fn main() {
let v = &["apples", "cake", "coffee"];

for text in v {
    println!("I like {}.", text);
}
}
```
An example of a for loop over a series of integers:


```
let mut sum = 0;
for n in 1..11 {
    sum += n;
}
assert_eq!(sum, 55);
```
A for loop is equivalent to a loop expression containing a match expression as follows:

```
'label: for PATTERN in iter_expr {
    /* loop body */
}
```
---

# Error Handling

Errors are inevitable in software, so Rust has a number of features to help you deal with them. When an error occurs, Rust requires you to acknowledge it and take action before your code can be compiled. By requiring this requirement, you ensure that you will discover errors before deploying your code to production and that they will be handled appropriately.

There are two major categories of errors in Rust: recoverable and unrecoverable. Typically, we want to notify the user of a recoverable error, such as a file not found error, and then retry the operation. The program should be immediately stopped if an unrecoverable error occurs, such as accessing a location beyond the end of an array.

It is common for languages to handle both kinds of errors in the same way, using mechanisms such as exceptions. Rust doesn’t have exceptions. Instead, it has the type Result<T, E> for recoverable errors and the panic! macro that stops execution when the program encounters an unrecoverable error. This chapter covers calling panic! first and then talks about returning Result<T, E> values. Additionally, we’ll explore considerations when deciding whether to try to recover from an error or to stop execution.
## Panic

### Unrecoverable Errors with panic!
When the panic! macro executes, your program will print a failure message, unwind and clean up the stack, and then quit. We’ll commonly invoke a panic when a bug of some kind has been detected and it’s not clear how to handle the problem at the time we’re writing our program.

Let’s try calling panic! in a simple program:
Filename: src/main.rs
```

This code panics!
fn main() {
    panic!("crash and burn");
}
```

If we run this code this is what we get

```
$ cargo run
   Compiling panic v0.1.0 (file:///projects/panic)
    Finished dev [unoptimized + debuginfo] target(s) in 0.25s
     Running `target/debug/panic`
thread 'main' panicked at 'crash and burn', src/main.rs:2:5
```
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
The call to panic! causes the error message contained in the last two lines. The first line shows our panic message and the place in our source code where the panic occurred:
