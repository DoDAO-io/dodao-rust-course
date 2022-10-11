## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Ownership and Borrowing
 
 
---

##### How many owners can a value on heap have ?  

- [ ]  2
- [x]  1
- [ ]  variable value
- [ ]  value on heap has no owner
  
Hint: NoHint
         
Explanation: Every value in Rust has exactly 1 owner.

Sub Topics: memory-allocation
 

---

##### Reference can be used to access the variable outside its scope ?  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: Variable can never be accessed outside its scope.

Sub Topics: memory-allocation
 

---

##### What is double free error ?  

- [x]  2 variables try to free same value as they go out of scope
- [ ]  Program free memory used by a variable on heap while it is in scope
- [ ]  An out of scope variable is assigned a value again
- [ ]  Same variable is used in different scopes
  
Hint: NoHint
         
Explanation: Double free error can occur in theory if 2 variable point to same value and try to free it as they go out of scope.

Sub Topics: memory-allocation
 

---

##### How many immutable references can a variable have ?  

- [ ]  1
- [ ]  2
- [x]  a variable can have any number of immutable references
- [ ]  less than 10
  
Hint: NoHint
         
Explanation: A variable can have any number of immutable references.

Sub Topics: borrowing
 

---

##### How many mutable references can a variable have ?  

- [x]  1
- [ ]  2
- [ ]  a variable can have any number of mutable references
- [ ]  references can not be mutable
  
Hint: NoHint
         
Explanation: A variable can have once 1 mutable reference, this saves it from data race condition.

Sub Topics: borrowing
 

---

##### Which of the following are true about variable passing in a function ?  

- [ ]  variable passed to a function are always cloned
- [ ]  variables on stack are copied when passed to function
- [ ]  variables on heap are moved when passed to function
- [ ]  variable passed to a function are always copied
  
Hint: NoHint
         
Explanation: Variables are moved or copied while passing to a function depending on whether they are on heap or stack respectively.

Sub Topics: borrowing
 

---

##### How can a value be accessible in a function after it is moved to another function ?  

- [ ]  by creating references to the value before passing to the function
- [ ]  a value moved to another function can never be used not in parent function
- [ ]  By creating a copy of the value before passing it to function
- [x]  by returning value from function and assigning to a new variable
  
Hint: NoHint
         
Explanation: When a value is returned from a function it is again moved to calling scope.

Sub Topics: memory-allocation
 

---

##### What is true about borrowing a variable ?  

- [ ]  borrowed variables can not be mutated
- [ ]  borrowing can be used to increase scope of the variable
- [ ]  borrowing does not changes the ownership of the variable
- [ ]  borrowing creates reference to variable whithout changing its scope
  
Hint: NoHint
         
Explanation: Borrowing can be used to create mutable or immutable references to variable without changing their scope.

Sub Topics: ownership
 

---

##### When is dangling reference created ?  

- [x]  it is not possible to create dangling references in rust
- [ ]  it is created when a references value goes out of scope
- [ ]  it is created when a references value if moved
- [ ]  it is created when value of a reference is incremented to next memory location
  
Hint: NoHint
         
Explanation: Rust does not allow creating dangling references.

Sub Topics: borrowing
 

---

##### References in Rust are always valid ?  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: It is not possible to create invalid references in Rust.

Sub Topics: borrowing
 

---

##### What is result of compiling code below ?
```
  let mut s = String::from("hello");

  {
      let r1 = &mut s;
  }

  let r2 = &mut s;
```
  

- [ ]  Code does not compiles as it is not possible to have 2 mutable references to a variable
- [ ]  Code compiles but breaks at runtime
- [x]  Code compiles successfully as 2 mutable references have different scope
- [ ]  Code does not compile as it is not possible to have a mutable reference to a string value
  
Hint: NoHint
         
Explanation: Mutable references to a variable in different scopes do not create compilation issue.

Sub Topics: borrowing, variable-scope
 

---

##### Which of the following is true about variables on stack ?  

- [ ]  Variables on stack can be moved
- [ ]  Variables on stack have size determined dynamically at runtime
- [ ]  Variables on stack are fixed in size
- [ ]  Variables on stack are copied
  
Hint: NoHint
         
Explanation: Variables on stack are fixed in size and follow copy symantics.

Sub Topics: memory-allocation
 

---

##### The action of creating a reference to a variable is called, what?  

- [ ]  Reverting
- [x]  Borrowing
- [ ]  Ownership
- [ ]  Reference
  
Hint: NoHint
         
Explanation: No much explanation needed

Sub Topics: borrowing
 

---

##### _____ enables Rust to make memory safety guarantees without needing a garbage collector  

- [x]  Ownership
- [ ]  Borrower
- [ ]  Validator
- [ ]  Static memory
  
Hint: NoHint
         
Explanation: Memory needs to belong to somewhere

Sub Topics: ownership
 

---

##### In Rust, memory is managed through a system of ownership and rules that the compiler checks. If any of the rules are violated, what will happen to the program?  

- [ ]  Prints the calcalution
- [ ]  Ask for memory
- [ ]  Memory is automatic assigned
- [x]  program will fail to compile
  
Hint: No memory, no calculation
         
Explanation: Memory works hand to hand with the machine

Sub Topics: ownership
 

---

##### Ownership rules, There can only be ____ owner/s at a time  

- [ ]  0
- [ ]  2
- [x]  1
- [ ]  3
  
Hint: NoHint
         
Explanation: Ownership belongs to an entity

Sub Topics: ownership
 

---

##### Complete the sentence
When the owner goes out of _____, the value will be ______.
  

- [x]  scope, dropped
- [ ]  dropped, scope
- [ ]  revert, opened
- [ ]  scope, opened
  
Hint: NoHint
         
Explanation: Owners have right and if they abandon the right it get dropped

Sub Topics: ownership
 

---

##### which statement best desribe reference?  

- [ ]  a set of rules that governs how a Rust program manages memory
- [x]  a reference is guaranteed to point to a valid value of a particular type for the life of that reference.
- [ ]  new concept for many programmers, it does take some time to get used to
- [ ]  the range within a program for which an item is valid
  
Hint: pointer
         
Explanation: point to valid value

Sub Topics: borrowing
 

---

##### The action of creating a reference to a variable is called ____  

- [ ]  Referencing
- [ ]  Ownership
- [ ]  Heaping
- [x]  Borrowing
  
Hint: NoHint
         
Explanation: creation of reference is pointer to a variable

Sub Topics: borrowing
 

---

##### What is a Scope?  

- [x]  the range within a program for which an item is valid
- [ ]  the range within a program for which an item is invalid
- [ ]  the range within a program
- [ ]  None of the above
  
Hint: NoHint
         
Explanation: 

Sub Topics: memory-allocation
 

---

##### When your code calls a function, the values passed into the function are pushed into  

- [ ]  Stack
- [x]  Heap
- [ ]  Memory
- [ ]  calldata
  
Hint: not a first in first out
         
Explanation: function are pushed in and dont have to leave first

Sub Topics: memory-allocation
 

---

##### The function's local variables get pushed onto  

- [ ]  Heap
- [ ]  Calldata
- [ ]  Function
- [x]  Stack
  
Hint: First in First out
         
Explanation: pushed accordingly

Sub Topics: memory-allocation
 

---

##### When the function is over, those values get_______ the stack.  

- [ ]  pushed in
- [x]  popped out
- [ ]  popped off
- [ ]  pushed out
  
Hint: correct term for memory allocation
         
Explanation: The right term is pop out

Sub Topics: memory-allocation
 

---

##### A problem that ownership addresses have is .  

- [x]  You can run out of space
- [ ]  You code get erased
- [ ]  You get hacked
- [ ]  Ownership can be change by outsider
  
Hint: heap memory
         
Explanation: Not cleaning up the heap data

Sub Topics: ownership
 

---

##### The main purpose of ownership is to manage ___ data  

- [ ]  Method
- [x]  Heap
- [ ]  Stack
- [ ]  Variable
  
Hint: memory
         
Explanation: heaping data means its not organized and ownership is one way to know what data is which

Sub Topics: memory-allocation
 

---

##### What line mark the end of the scope of s?
```rust
    fn main() {
     {                      // line 1
      let s = "hello";   // line 2
      // do stuff with s // line 3
      }                      // line 4
    }
```
  

- [ ]  Line 1
- [ ]  line 2
- [ ]  line 3
- [x]  line 4
  
Hint: No longer in use
         
Explanation: The program is done and no longer needs s

Sub Topics: memory-allocation
 

---

##### What is the special annotation in Rust that we can place on types that are stored on the stack, as integers  

- [ ]  Clone
- [x]  Copy trait
- [ ]  Boolean type
- [ ]  Validators
  
Hint: Stack-Only Data
         
Explanation: variables that use it do not move, but rather are trivially copied,

Sub Topics: memory-allocation
 

---

##### what is the output?
```rust
     fn main() {
       let s1 = String::from("hello");
       let len = calculate_length(&s1);
       println!("The length of '{}' is {}.", s1, len);
      }
     fn calculate_length(s: &String) -> usize {
       s.len()
      }
 ```
  

- [ ]  The length of 'hello' is 6
- [x]  The length of 'hello' is 5
- [ ]  The length of 'string' is 6
- [ ]  None of the above
  
Hint: length of string
         
Explanation: calculate_length function have a reference to an object as a parameter instead of taking ownership of the value

Sub Topics: borrowing
 

---

##### The opposite of referencing?  

- [ ]  Borrowing
- [ ]  Ownership
- [ ]  non-referencing
- [x]  dereferencing
  
Hint: uses of *
         
Explanation: It does the opposite of referencing

Sub Topics: borrowing
 

---

##### The result of the program below is
```rust
    fn main() {
     let s = String::from("hello");
     change(&s);
    }
    fn change(some_string: &String) {
       some_string.push_str(", world");
    }
```
  

- [x]  Error: cannot borrow
- [ ]  hello world
- [ ]  Ownership denied
- [ ]  Borrowed data is too big
  
Hint: tried to borrow
         
Explanation: some_string` has a `&` reference

Sub Topics: borrowing
 

---

##### The reason for invalidating the original reference after moving the value is to prevent ____  

- [ ]   double error.
- [x]   double free error.
- [ ]   free error.
- [ ]   moving error.
  
Hint: Nohint
         
Explanation: self explanatory

Sub Topics: ownership
 

---

##### How many strict rules does ownership follow and what happen when they are violated?  

- [ ]  There are 2 rules and it ignore them
- [ ]  There are 3 rules and it ignore them
- [ ]  There are 2 rules, compiler fails when they are violated
- [x]  There are 3 rules, compiler fails when they are violated
  
Hint: violation of these rules confuse the compiler
         
Explanation: fail to follow the rules, compiler fails simple

Sub Topics: ownership
 

---

##### At any given time, you can have either _____ reference or ______ references.  

- [ ]  two mutable, any number of immutable
- [x]  one mutable, any number of immutable 
- [ ]  any number of mutable, one immutable
- [ ]  one immutable, any amount of mutable
  
Hint: mutable reference
         
Explanation: 

Sub Topics: borrowing
 

---

##### What is a dangling pointer?  

- [x]  a pointer that references a location in memory that may have been given to someone else
- [ ]   a pointer in that it’s an address we can follow to access the data stored at that address
- [ ]  Both definitions are correct
- [ ]  None of the above
  
Hint: dangling reference
         
Explanation: No explanation

Sub Topics: borrowing
 

---

##### The ownership system is a prime example of a _____  

- [ ]  discounted-cost abstraction
- [ ]  paid-cost abstraction
- [ ]  cheap-cost abstraction
- [x]  zero-cost abstraction
  
Hint: Rust has a focus on safety and speed.
         
Explanation: abstractions cost as little as possible in order to make them work

Sub Topics: ownership
 

---

##### A stack follows a __________ order  

- [ ]  first in first out
- [x]  last in first out
- [ ]  last in last out
- [ ]  first in last out
  
Hint: Nohint
         
Explanation: like a can of pringles

Sub Topics: memory-allocation
 

---

##### The exact size of such a string cannot be determined at compile time
This implies what?
  

- [x]  Heap allocation are best fit for string
- [ ]  Stack allocation works best
- [ ]  we wait for compiler to decide
- [ ]  we can store on both
  
Hint: Nohint
         
Explanation: string are not scalar

Sub Topics: memory-allocation
 

---

##### which is not a way to transfer ownership?  

- [ ]  Passing value to a function.
- [ ]  Returning value from a function.
- [ ]  Assigning value of one variable to another variable
- [x]   calling the owner's Id and claiming it
  
Hint: Nohint
         
Explanation: Each data can have only one owner at a time.

Sub Topics: ownership
 

---

##### What is the output?
```rust
    fn main(){
    // a list of nos
    let v = vec![10,20,30];
    print_vector(&v); 
    println!("Printing the value from main() v[0]={}",v[0]);
    }
    fn print_vector(x:&Vec<i32>){
     println!("Inside print_vector function {:?}",x);
    }
```
  

- [ ]  Inside print_vector function [20, 30] Printing the value from main() v[0] = 10 
- [x]  Inside print_vector function [10, 20, 30] Printing the value from main() v[0] = 10
- [ ]  The compilations fails
- [ ]  Error occurs at line 3
  
Hint: passing reference
         
Explanation: No explantion, follow the code

Sub Topics: borrowing
 

---

##### Functions can also modify borrowed variables using ____ to them, before returning ownership.  

- [x]  mutable references 
- [ ]  immutable references 
- [ ]  * operand
- [ ]  None of the above
  
Hint: Nohint
         
Explanation: following the borrowing and referencing structure

Sub Topics: borrowing
 

---

##### ___ is the property of a program where memory pointers always used to point to valid memory of the correct type and size.  

- [ ]  Ownership safety
- [ ]  memory validation
- [ ]  Ownership validation
- [x]  Memory safety
  
Hint: nohint
         
Explanation: It is important you understand the concept of ownership or you might create an unsafe memory

Sub Topics: memory-allocation
 

---

##### An unsafe memory may lead to a crash, unexpected output and _____  

- [ ]  compiler shutdown
- [x]  Data leakage
- [ ]  Memory crashes
- [ ]  Nonr of the above
  
Hint: reduce security
         
Explanation: it lead to leakage of values because it points to invalid address

Sub Topics: memory-allocation
 

---

##### A mutable reference is prefixed with  

- [x]  &mut
- [ ]  *mut
- [ ]  +mut
- [ ]  &%mut
  
Hint: mut and an operand
         
Explanation: none

Sub Topics: borrowing
 

---

##### Rust is a ____ programming language, so how values are stored is essential to how the language behaves.  

- [ ]  Object
- [ ]  Model
- [ ]  Static
- [x]  system
  
Hint: Nohint
         
Explanation: it is not an object oriented language

Sub Topics: memory-allocation
 

---

##### Rust uses a -_____ to enforce its ownership rules and ensure that programs are memory safe.  

- [ ]  data checker
- [x]  borrow checker
- [ ]  Check warner
- [ ]  Compiler
  
Hint: A checker
         
Explanation: RUst needs an enforcer to verify all rules are followed

Sub Topics: ownership
 

---

##### If a reference is invalid the data can be dropped using a construct called _____.  

- [x]  lifetimes
- [ ]  runtimes
- [ ]  borrow checker
- [ ]  FIFO
  
Hint: how long a variable exists
         
Explanation: start on variable creation and end on variable destruction

Sub Topics: borrowing
 

---

##### What kind of error does violating an ownership rules gives  

- [ ]  Compiler error
- [ ]  Runtime error
- [ ]  Lifetimes error
- [x]  Panic error
  
Hint: it confuses the compiler
         
Explanation: No explanation

Sub Topics: ownership
 
