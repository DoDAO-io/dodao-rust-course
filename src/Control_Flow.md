
# Control Flow

---

Many programming languages allow you to run some code depending on whether a condition is true, or run some code repeatedly while a condition is true. 
If expressions and loops are the most common constructs in Rust that control execution flow.

In most cases, the computer runs the code in order from the first line in the file to the last line, unless it encounters structures that alter the control flow, such as loops and conditionals.

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


