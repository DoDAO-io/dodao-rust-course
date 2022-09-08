## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Control Flow & Functions
 
 
---

##### ________ is a method that allows you to, instead of handling possible errors inside the current function you're writing, to pass the error up to the caller of this function and handle the error there.
  

- [ ]  Unwrap and Expect
- [ ]  Result<T,E>
- [ ]  Panic!
- [x]  Error Propagating
  
Hint: Error handling
         
Explanation: it returns a Return to whoever is calling the function to handle it.

Sub Topics: error-handling
 

---

##### If the error is of the unrecoverable nature, the _____ macro is executed
  

- [ ]  Not to panic
- [ ]  Result<T,E>
- [x]  Panic!
- [ ]  Error P?
  
Hint: Error handling
         
Explanation: prints an error message to the screen then unwinds

Sub Topics: error-handling
 

---

##### Rust splits errors into 2 categories, Recoverable errors and
  

- [ ]  Not important errors
- [x]  Non-Recoverable errors
- [ ]  Immediate errors
- [ ]  Data Errors
  
Hint: Error handling
         
Explanation: type of errors

Sub Topics: error-handling
 

---

##### An 'if' expression is a ________ branch in program control.
  

- [ ]  Match
- [ ]  Method
- [x]  Condition
- [ ]  Office
  
Hint: if statement
         
Explanation: A statement that gets checked

Sub Topics: control-flow
 

---

##### The condition operands must have the _______ type.
  

- [ ]  String
- [x]  Boolean
- [ ]  Integer
- [ ]  Float
  
Hint: A data type
         
Explanation: The condition must be 0 or 1

Sub Topics: if-statement
 

---

##### What is the output?
```rust
    fn main() {
      let number = 8;

      if number < 9 {
        println!("condition was true");
      } else {
        println!("condition was false");
      }
    }
  ```
  

- [ ]  condition was false
- [ ]  number = 8
- [ ]  Throws error
- [x]  condition was true
  
Hint: If else
         
Explanation: The condition of 8 being lesser than 9 is correct

Sub Topics: if-statement
 

---

##### What will be the output if we run this code section?
```rust
  fn main() {
    let number = 3;

    if number {
      println!("number was three");
    }
  }
```
  

- [ ]  3
- [ ]  True
- [x]  error[E0308]: mismatched types
- [ ]  number is 3
  
Hint: Data type
         
Explanation: should be a condition

Sub Topics: if-statement
 

---

##### What is the output?
```rust
  fn main() {
    let digit = 34;
    if digit != 0 {
      println!("number was something other than zero");
    }
  }
```
  

- [ ]  Mismatched type
- [ ]  digit error
- [ ]  False
- [x]  number was something other than zero
  
Hint: Take note of the !=
         
Explanation: != is not equal to, so if the digit is not equal to zero, do the next statement

Sub Topics: if-statement
 

---

##### ____ often useful to execute a block of code more than once.
  

- [x]  Loop
- [ ]  Function
- [ ]  Result
- [ ]  Print
  
Hint: iteration
         
Explanation: more than one execution

Sub Topics: loop
 

---

##### The loop keyword tells Rust to execute a block of code over until you explicitly tell it to stop.
 What happens if you don't tell it to stop?
  

- [ ]  it stop by itself
- [ ]  It slow down
- [x]  It loops forever
- [ ]   ask you to stop it
  
Hint: Looping out
         
Explanation: loop are forever

Sub Topics: loop
 

---

##### What will happen if we run this code?
```rust
  fn main() {
    loop {
      println!("again!");
    }
  } 
```
  

- [x]  It prints again forever till you kill the terminal
- [ ]  it stops after 100 times
- [ ]  Error: couldn't run: no end
- [ ]  It end immediately
  
Hint: Looping
         
Explanation: it just loop forever

Sub Topics: loop
 

---

##### What is the value of result?
```rust
  fn main() {
    let mut counter = 0;

    let result = loop {
      counter += 1;

      if counter == 10 {
        break counter * 3;
      }
    };

    println!("The result is {result}");
  }
```
  

- [ ]  100
- [ ]  20
- [x]  30
- [ ]  40
  
Hint:  watch the declaration of result
         
Explanation: 

Sub Topics: if-else-let-statement
 

---

##### A program will often need to evaluate a condition within a loop. What keywords is best at checking the condition?
  

- [x]  For and While
- [ ]  If and Panic
- [ ]  panic and println
- [ ]  for and if
  
Hint: breaking loop
         
Explanation: 

Sub Topics: for-loop-statement
 

---

##### What is the output of this?
```rust
  fn main() {
    let mut number = 3;
    while number != 0 {
      println!("{number}!");
      number -= 1;
    }
    println!("LIFTOFF!!!");
  }
```
  

- [x]  3! 2! 1! LIFTOFF!!!
- [ ]  1! 2! LIFTOFF!!!
- [ ]  error
- [ ]  LIFTOFF!!!
  
Hint: Loop while number is not zero yet
         
Explanation: we looped from 3 down 0 and broke out

Sub Topics: loop
 

---

##### Complete the sentence.
The safety and conciseness of _____ make them the most commonly used loop construct in Rust.
  

- [ ]  While loop
- [ ]  If-else
- [x]  For loop
- [ ]  While for
  
Hint: A loop statement
         
Explanation: 

Sub Topics: loop
 

---

##### The ____ function(most important function), which is the entry point of many programs.
  

- [ ]  Branch
- [ ]  Sub
- [ ]  VIP
- [x]  main
  
Hint: Function
         
Explanation: it is the functions of all function

Sub Topics: functions
 

---

##### Rust code uses snake case as the conventional style for _______ and variable names
  

- [ ]  Parameter
- [x]  Function
- [ ]  File
- [ ]  Object
  
Hint: Function naming convention
         
Explanation: letters are lowercase and underscores separate words

Sub Topics: functions
 

---

##### We define a function in Rust by entering ____ followed by a function name and a set of parentheses.
  

- [ ]  Sn
- [ ]  func
- [x]  fn
- [ ]  function
  
Hint: Declaring a function
         
Explanation: Thats the Rust keyword

Sub Topics: functions
 

---

##### What is the output?
```rust
   fn main() {
     println!("Hello, my name is John.");

     another_function();
   }

   fn another_function() {
      println!("Another function.");
   }
```
  

- [x]  Hello, my name is John. Another function
- [ ]  Another function
- [ ]  Hello, my name is John.
- [ ]   Another function Hello, my name is John.
  
Hint: Function calling
         
Explanation: You call function in the main for this example

Sub Topics: functions
 

---

##### The ___ brackets tell the compiler where the function body begins and ends.
  

- [x]  Curly
- [ ]  Square
- [ ]  Angle
- [ ]  Parentheses
  
Hint: function delaration
         
Explanation: Declaring every function in a block

Sub Topics: functions
 

---

##### What is the output?
 ```
  fn main() {
    let x = 7;
    if x == 5 {
      println!("x is five!");
    } else if x == 6 {
      println!("x is six!");
    } else {
      println!("x is not five or six :(");
    }
  }
 ```
  

- [ ]  x is five!
- [x]  x is not five or six :(
- [ ]  x is six!
- [ ]  x is seven!
  
Hint: Nested if-else statement
         
Explanation: Find the correct condition

Sub Topics: nested-if-else-statement
 

---

##### The ____ operator can only be used in functions whose return type is compatible with the value the ? is used on
  

- [x]  ?
- [ ]  ::
- [ ]  <T,E>
- [ ]  //
  
Hint: error handling operator
         
Explanation: if it is not compatiable it would not work

Sub Topics: error-handling
 

---

##### What will happen if we run this code?
```rust
  fn main() {
     panic!("crash and burn");
  }
 ```
  

- [ ]  timeout error
- [ ]  fails to compile
- [x]  it panic at crash and burn
- [ ]  print out crash and burn
  
Hint: Panic first
         
Explanation: it is not a print function

Sub Topics: error-handling
 

---

##### What is a Statement?
  

- [x]  Statements are instructions that perform some action and do not return a value
- [ ]  Statement are a library function
- [ ]  statements are the core of a program
- [ ]  Statements are instructions that perform some action and return a value
  
Hint: Statement
         
Explanation: instructions only, doesn't do any other thing

Sub Topics: functions
 

---

##### Complete the sentence
Function bodies are made up of a series of ______ optionally ending in an ______
  

- [ ]  Statement and methods
- [x]  Statement and expression
- [ ]  Expression and methods
- [ ]  Expression and Statement
  
Hint: function body
         
Explanation: They make up a function

Sub Topics: functions
 

---

##### What part of your code can be evaluate to a resulting value.
  

- [ ]  Statement
- [ ]  Function
- [x]  Expression
- [ ]  Methods
  
Hint: Function body
         
Explanation:  They are calculated 

Sub Topics: functions
 

---

##### What fragment of code is an expression here?
```rust
  fn main() {
    let y = {
      let x = 3;
      x + 1
    };

    println!("The value of y is: {y}");
  }
```
  

- [x]  { let x = 3; = x + 1 }
- [ ]  let x = 3
- [ ]  println!(The value of y is: {y});
- [ ]  fn main() 
  
Hint: not a statement
         
Explanation: it should be a computation

Sub Topics: functions
 

---

##### Which is not a control flow method?
  

- [ ]  for-loop
- [ ]  if-else
- [ ]  while-loop
- [x]  panic!
  
Hint: which can be use for iteration
         
Explanation: the odd one is use for error handling

Sub Topics: loop
 

---

##### Can a loop be inside a loop?
  

- [ ]  only when you use the Panic! method
- [ ]  No
- [x]  Yes, we break and can continue
- [ ]  Loop are statement
  
Hint: Nested loops
         
Explanation: you can break and continue with loops

Sub Topics: loop
 

---

##### Functions can return _____ to the code that calls them
  

- [x]  Values
- [ ]  function
- [ ]  statement
- [ ]  numbers
  
Hint: returns something important
         
Explanation: functions have to be called

Sub Topics: functions
 

---

##### Take a look at this little complex code, what best decribe the output?
```rust
     fn main() {
       // `n` will take the values: 1, 2, ..., 100 in each iteration
        for n in 1..101 {
          if n % 15 == 0 {
            println!("fizzbuzz");
          } else if n % 3 == 0 {
            println!("fizz");
          } else if n % 5 == 0 {
            println!("buzz");
          } else {
            println!("{}", n);
          }
       }
     }
   ```
  

- [ ]  it fails completely
- [ ]  it prints from 1 to 101
- [x]  It moves from 1 to 101, and test each number against the condition and prints out the first condition output it matches
- [ ]  The code ends because nested if statement needs break command
  
Hint: division without reminder
         
Explanation: from 1 to 101, if the remainder matches a condition it prints its output

Sub Topics: nested-if-else-statement
 

---

##### What is the output?
  ```rust
    fn main( ) {
      let strn = "DoDAOCourse";
      let fixed_string = "DDC";
      if fixed_string == strn {
        println!("Same");
      } else {
        println!("Not Same");
 	  }
    }   
 ```
  

- [ ]  Same
- [x]  Not Same
- [ ]  Error: let is not a keyword
- [ ]  DoDAOCourse
  
Hint:  Data comparision
         
Explanation: We use if and let statement to compare the strings

Sub Topics: looping-value
 

---

##### What is the output?
```rust
  fn main() {  
    n = 7;
    if n>10 { 
      println!("Greater than 10");
    } else {
      println!("Smaller than 10");
    }
  }
```
  

- [x]  Smaller than 10
- [ ]  Smaller than 7
- [ ]  Greater than 10
- [ ]  Greater than 7
  
Hint: greater than or less than
         
Explanation:  its simple enough

Sub Topics: if-statement
 

---

##### What is the output?
```rust
  fn main() {
    let n = 9;
    if n>10 {
      println!("Greater than 10");
    } else if n==10 {
      println!("Equal to 10"); 
    } else { 
      println!("Smaller than 10");
    }   
  }
```
  

- [ ]  Equal to 10
- [ ]  Greater than 10
- [ ]  Greater than 9
- [x]  Smaller than 10
  
Hint: Find the conditions that matches
         
Explanation: Iterate and find the mathematical solution

Sub Topics: if-statement
 

---

##### What is the output?
```rust
  use std::fs::File;

  fn main() {
    let f = File::open("gfg.txt");
    println!("{:?}",f);
  }
 ```
  

- [x]  Err(Os { code: 2, kind: NotFound, message: 'No such file or directory' })
- [ ]  thread 'main' panicked at 'index out of bounds:
- [ ]  Null error
- [ ]  File has been opened
  
Hint: Result error method
         
Explanation: file gfg.txt was not there

Sub Topics: result-option
 

---

##### What is the expected output?
```rust
  use std::fs::File;
  fn main() {
    // file doesn't exist
    let f = File::open("gfg.txt");
    match f {
 	  Ok(file) => {	
        println!("file found {:?}",file);
 	  },
      Err(_error) => {
        // replace it with whatever you want
        // to do if file is not found
        println!("file not found \n"); 
      }
    }
  }
```
  

- [ ]  file found 
- [x]  file not found 
- [ ]  Err(Os { code: 2, kind: NotFound, message: 'No such file or directory' })
- [ ]  Opened file
  
Hint: Result error when missing an item
         
Explanation: matches the return type of the result

Sub Topics: result-option
 

---

##### What is the output of this code?
```rust
  fn main() {
    let result = eligible(13);
    match result {
      Ok(age) => {
        println!("Person eligible to vote with age={}", age);
      }
      Err(msg) => {
        println!("{}", msg);
      }
    }
  }
  fn eligible(age: i32) -> Result<i32, String> {
    if age >= 18 {
      return Ok(age);
    } else {
      return Err("Not Eligible..Wait for some years".to_string());
    }
  }
```
  

- [x]  Not Eligible..Wait for some years
- [ ]  Person eligible to vote with 13 years
- [ ]  Error: Panicked at Err
- [ ]  Failed to compile
  
Hint: Compare the age give to the required voting age
         
Explanation: to produce an error if a person below 18 years tries to apply for voter ID

Sub Topics: result-option
 

---

##### Describe the output(best fit) 
  ```rust
    fn main() {
      let mut n = 10;
      while n != 0 {
        println!("{}", n);
        n -= 1;
      }
    }
  ```
  

- [ ]  Count up from 1 to 10
- [ ]  Print from 1 to 10
- [x]  Print out from 10 to 1
- [ ]  Count down from 10 to 1
  
Hint: loop from 10 down
         
Explanation: Counting from 10 to 1 

Sub Topics: loop
 

---

##### hat is the output?
```rust
  fn main() {
    let mut n = 1;
    while n <= 5 {
      println!("{}", n * 2);
      n += 1;
    }
  }
```
  

- [x]  2 4 6 8 10
- [ ]  1 2 3 4 5
- [ ]  1 3 6 9 11
- [ ]  2 5 
  
Hint: multiply by 2, and count to 5
         
Explanation: while n is less or requal than 5 do something

Sub Topics: loop
 

---

##### Arguments are passed after function name inside ______
  

- [x]  parenthesis
- [ ]  Curtly bracket
- [ ]  square bracket
- [ ]  Block bracket
  
Hint: Function parameter
         
Explanation: very important we put args in a bracket

Sub Topics: args
 

---

##### What does the greet function take as argument?
```rust
    fn main() {
      greet("kushwanthreddy");
    }
    fn greet(name: &str) {
       println!("hello {} welcome to geeksforgeeks", name);
    }
```
  

- [x]  name(string)
- [ ]  kushwanthreddy
- [ ]  name(integer)
- [ ]  name(boolean)
  
Hint: The greet function has name args
         
Explanation: look at the parenthesis

Sub Topics: args
 

---

##### When a semi-colon is written at the end of an expression, it turns into a ____?
  

- [ ]  Values
- [x]  Statement
- [ ]  function
- [ ]  Parameter
  
Hint: part of a function
         
Explanation: no explantion needed

Sub Topics: functions
 

---

##### What are the arguments passed in the code below?
```rust
	fn main() {
      print_sum(5, 6);
    }
   	fn print_sum(x: i32, y: i32) {
       println!("sum is: {}", x + y);
    }
 ```
  

- [ ]  x: i32, y: i32
- [ ]  x: , y:
- [ ]  32, y: i32
- [x]  5, 6
  
Hint: parenthesis
         
Explanation: we pass args inside a bracket to call them

Sub Topics: args
 

---

##### How can a function be called?
  

- [x]  function_name(argument)
- [ ]  call function_name(main)
- [ ]  let = function_name(main)
- [ ]  function_name(main)::called
  
Hint: null
         
Explanation: We call function by its name and arguments

Sub Topics: functions
 

---

##### What will happen if we run this program?
```rust
	fn main() {
 	  let number = 5;
   	  if number % 2 == 1 {
        if number % 3 == 0 {
          println!("Odd and divisible by 3");
        }
      }
    }
 ```
  

- [ ]  it prints : Odd and divisible by 3
- [ ]  it print: Odd and divisible by 5
- [ ]  Error use one if
- [x]  it prints nothing
  
Hint: after the first if, follow to the next
         
Explanation: null

Sub Topics: functions
 

---

##### We create control flow by using if,for,while statement in combination with ______ and _____
  

- [x]  relational comparison and logical operator
- [ ]  boolean and data type
- [ ]  functions and constructor
- [ ]  compiler and error
  
Hint: creating flow requires conditions and conditions are statement and reasonings
         
Explanation: null

Sub Topics: control-flow
 

---

##### What is the output?
```rust
  fn main() {
    let check_value= 200;
    if check_value < 100 {
      println!("The decision returns true !"); 
    } else {
      println!("The decision returns false!"); 
    } 
  }
```
  

- [x]  The decision returns false!
- [ ]  The decision returns true!
- [ ]  Failed to compile
- [ ]  The decision returns indecisive!
  
Hint: check the condition
         
Explanation: xomparing the number we the the greater one

Sub Topics: if-else-let-statement
 

---

##### What will happen when will run this?
```rust
 	fn main() {
      let a = [1,2,3];
      a[4] 
    }
 ```
  

- [ ]  it prints 4
- [ ]  nothing happens
- [x]  Panic! error occurs at:> a[4]
- [ ]  it prints the array
  
Hint: Panic
         
Explanation: we trying to call an index of 4 in a array of max:2 index

Sub Topics: panic-not-panic
 

---

##### A function can reduce the number of codes, which saves ____.
  

- [ ]  Values
- [ ]  Memory
- [x]  Time
- [ ]  Money
  
Hint: Function can be called from different place and we don't have to code them
         
Explanation: code reusability is important to programmers

Sub Topics: functions
 
