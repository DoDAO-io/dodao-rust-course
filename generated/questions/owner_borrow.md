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

##### How manu immutable references can a variable have ?  

- [ ]  1
- [ ]  2
- [x]  a variable can have any number of immutable references
- [ ]  less than 10
  
Hint: NoHint
         
Explanation: A variable can have any number of immutable references.

Sub Topics: borrowing
 

---

##### How manu mutable references can a variable have ?  

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
 
