
# Control Flow

---

Many programming languages allow you to run some code depending on whether a condition is true, or run some code repeatedly while a condition is true. 
If expressions and loops are the most common constructs in Rust that control execution flow.

In most cases, the computer runs the code in order from the first line in the file to the last line, unless it encounters structures that alter the control flow, such as loops and conditionals.

We control the flow of our program with the following statements, in combination with relational comparison and logical operators.

* if
* else if
* else
* match

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

