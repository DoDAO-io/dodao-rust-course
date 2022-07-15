## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Blockchain Basics
 
 
---

##### What is the output of the following code snippet:
 
    ``` 
        fn main() {
          let x = 12;
          println!("The value of x is: {x}");
          x = 8;
          println!("The value of x is: {x}");
        } 
    ```
  

- [ ]  The value of x is: 8
- [ ]  Error: the variable x is mutable
- [ ]  The value of x is: 12
- [x]  Error: the variable x is immutable
  
Hint: NoHint
         
Explanation: Error would occur, because the variable x isn't set as mutable so it's value can't be changed.

 

---

##### Space taken by a Character data type in rust is  

- [ ]  1 byte
- [x]  4 bytes
- [ ]  8 bytes
- [ ]  16 bytes
  
Hint: It doesn't use ASCII values
         
Explanation: Rust's char type is four bytes in size and represents a Unicode Scalar Value, which means it can represent a lot more than just ASCII.

 

---

##### Rust is a Dynamically typed language.  

- [ ]  True
- [x]  False
  
Hint: Does the compiler need to know the data type at compile time?
         
Explanation: It is statically typed

 

---

##### Select the incorrect declaration statement  

- [ ]  let mut x: u32 = 20;
- [ ]  let mut x: i32 = -20;
- [x]  let mut x: u32 = -20;
- [ ]  let mut x = 20;
  
Hint: NoHint
         
Explanation: It is declared as an unsigned integer, but the value is negative

 

---

##### Suppose you declared a variable as u8 and then assigned it a value of "257". What would be the output if it’s compiled with a "`“--release” flag?`"  

- [ ]  257
- [ ]  Error: Integer Overflow
- [ ]  0
- [x]  1
  
Hint: NoHint
         
Explanation: After 255 the digits start rolling back to 0, 1 and so on

 

---

##### Are Tuples in rust dynamic in nature?
"Eg:-" 
``` 
  let tup: (i32, f64, bool) = (500, 6.4, true); 
```
  

- [ ]  Yes
- [x]  No
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Select the correct statements for the two String     types(“String” and “&str”).
 "a. “Strings” are immutable in nature and cannot be modified. "
 "b. “&str” is a primitive data type, whereas “String” is implemented in the standard library."
 "c. To read a file into the strings, we use the read_to_string() method."
  

- [ ]  Only a
- [ ]  Both a & b
- [x]  Both b & c
- [ ]  None of the above
  
Hint: NoHint
         
Explanation: Strings are mutable in nature

 

---

##### Which among the following is not an acceptable keyword in rust?  

- [ ]  let
- [x]  var
- [ ]  impl
- [ ]  mut
  
Hint: NoHint
         
Explanation: var is not a keyword in rust

 

---

##### Which of the following brackets are used as placeholders in rust?  

- [x]  {}
- [ ]  [ ]
- [ ]  ( )
- [ ]  < >
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Constants in rust can be defined in which scope?  

- [ ]  Global
- [ ]  Method
- [ ]  Local
- [x]  All of the above
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Which of the following are the scalar data types present in rust?  

- [x]  integers, floating-point numbers, booleans, characters
- [ ]  integers, signed numbers, unsigned numbers, booleans, characters
- [ ]  integers, strings, signed numbers, unsigned numbers, booleans
- [ ]  integers, floating-point numbers, strings, booleans
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### The compound data types supported by rust are-  

- [ ]  Arrays, Lists, Red-Black Trees
- [ ]  Arrays, Lists, Vectors
- [x]  Arrays, Tuples
- [ ]  Arrays, Maps
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Which are valid array declarations in rust? 
``` 
       let mut arr : {i64, 3} = [2,3,5];
       let mut arr : {3,3};
       let mut arr = [2,3,5];
 ```
  

- [ ]  Both a & b
- [ ]  Both b & c
- [ ]  Only a
- [x]  All a, b, & c
  
Hint: Look for the wrong declaration format, you may or may not find it
         
Explanation: No explanation

 

---

##### Which of the following has low memory usage, const or static?  

- [x]  const
- [ ]  static
- [ ]  depends upon the data type
- [ ]  both have the same memory usage
  
Hint: How many of these can we update?
         
Explanation: Constant doesn't uses any extra heap memory to update

 

---

##### To use dynamic-sized variables, which of the following should be used?  

- [ ]  Arrays & Tuples
- [ ]  List all the data types
- [x]  ?Sized
- [ ]  Dynamic-Sized variables not supported in rust
  
Hint: No hint
         
Explanation: No explanation

 

---

##### What is the importance of the “type” keyword in rust?  

- [ ]  used for dynamic-sized data type
- [ ]  used to create a template
- [ ]  used for user-defined data type
- [x]  used to set an alias of another type
  
Hint: Used for another types.
         
Explanation: Sets an alias of another type.

 

---

##### What is the importance of Cargo in rust?  

- [ ]  Collection of rust libraries
- [ ]  Modules Package manager
- [x]  Build system and Package manager
- [ ]  Used to create and build UI projects in rust
  
Hint: What is npm used for?
         
Explanation: No explanation

 

---

##### How to print the data type of a variable in rust?  

- [x]   `std::any::type_name` 
- [ ]   `variable.type_name()` 
- [ ]   `std::intrisic::type_name` 
- [ ]   `std::variable::type_name` 
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Which type cast preserves the mathematical value in all cases?  

- [x]  i32 as i64
- [ ]  i64 as i32
- [ ]  usize as u64
- [ ]  f64 as f32
  
Hint: NoHint
         
Explanation: Because they can handle both signed and unsigned values, and are typecasted in one data type only.

 

---

##### Which of the following cannot be destructed further into smaller segments?  

- [ ]  Tuples
- [x]  Traits
- [ ]  Arrays
- [ ]  Structs
  
Hint: Think of the structures they're built upon 
         
Explanation: No explanation

 

---

##### Which comment syntax is not legal?  

- [x]  <//>
- [ ]  /* */
- [ ]  //!
- [ ]  //
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Values of the array can be deleted.  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: Values can be updated, but can't be deleted

 

---

##### How do you initialize every element of an array of size 5 with 0?  

- [ ]  `let mut arr : {i32;5} = {5;0};`
- [x]  `let mut arr : {i32;5} = {0;5};`
- [ ]  `let mut arr : {5;i32} = {5;0};`
- [ ]  `let mut arr : {5;i32} = {0;5};`
  
Hint: Look at the declarations, don't get confused by the order while declaring
         
Explanation: The first argument is the integer you want to initialize an element with, and the second argument tells the end posistion till where you want to pre-initialize.

 

---

##### Tuples in rust are  

- [x]  finite heterogeneous compound data types
- [ ]  finite homogeneous compound data types
- [ ]  infinite heterogeneous compound data types
- [ ]  infinite homogeneous compound data types
  
Hint: NoHint
         
Explanation: They can handle and store different data types

 

---

##### "What would be the output of the following code snippet?
   ```
       " Fn main( ) {	"
          "let mut dodao_io = (""Do"", 69, ""DAO"", 420);"
          "println!(""{} "", dodao_io );"
          "println!(""at 0 index = {} "", gfg.0 );"
        "} "

  ```"
  

- [ ]  ("Do", 69, "DAO", 420) & Do
- [ ]  ("Do", 69, "DAO", 420) only
- [x]  Compilation Error
- [ ]  ("Do", 69, "DAO", 420) & “Do”
  
Hint: No Hint
         
Explanation: The first print statement should've had {;?}

 

---

##### What is the process of temporarily making a variable mutable known as?  

- [ ]  Pseudo-mutability
- [ ]  Foreshadowing
- [x]  Shadowing
- [ ]  Overshadowing
  
Hint: NoHint
         
Explanation: No explantion

 

---

##### Which of the following is an example of suffix annotation?  

- [ ]  let a_int: i64 = 20;
- [ ]  let a_int = i6420;
- [x]  let a_int = 20i64;
- [ ]  None of the above
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### A. println!("1 + 2 = {}", 1u32 + 2);
B. println!("1 - 2 = {}", 1u32 + 2);
  

- [x]  Only A compiles
- [ ]  Only B compiles
- [ ]  Both A & B compile
- [ ]  None of them complies
  
Hint: Solution being Positive or Negative might make a difference
         
Explanation: Here, when initialized, 1 is set as unsigned 32 integer u32. In statement A, it works because  1+2=3, and it's positive. But, 1-2=(-1) and as they were unsigned integers, so they cannot hold a negative value, so this statement doesn't compile


 

---

##### What is the output of the following code
"``` println!("{}", 1_00u32 + 2_0); ```"
  

- [ ]  Compilation Error
- [ ]  Runtime Error
- [ ]  3
- [x]  120
  
Hint: NoHint
         
Explanation: 1_000u32 is similar as 100 of u32 type.

 

---

##### String in standard library has more functionalities coded into it than string slice?  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### What is the output of the following code
  " ```fn main() {
    let first_string = "This is some string ".to_string();
    let second_string = "Let's add some Data";

    let final_string = first_string + &second_string;

    println!("First string is: {}", first_string);   
    println!("Second string is: {}", second_string);

    println!("Finally we have: {}", final_string);
}
``` "
  

- [ ]  Only 1st print statement shows an output
- [ ]  Only 1st and 2nd print statement shows an output
- [ ]  All the 3 string statements show an output
- [x]  Error occurs
  
Hint: NoHint
         
Explanation: Syntatical Error in the code snippet

 

---

##### Which of the following operator is used by string slices to reference?  

- [x]  &
- [ ]  %
- [ ]  #
- [ ]  *
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Select the incorrect statement from the following  

- [ ]  Once you get a string slice from a string, then you cannot really                 modify that String anymore
- [ ]  Using slices to work with Strings allows us to add an extra                       security measure.
- [ ]  If you attempt to create a string slice in the middle of a                        multibyte character, your program will exit with an error
- [x]  String Slice mutably borrows the String itself
  
Hint: Nohint
         
Explanation: No explanation

 

---

##### What will happen at the runtime if overflow occurs?  

- [x]  Panic and crashes the program
- [ ]  Garbage values will be output
- [ ]  Those values are ignored and the output is as expected
- [ ]  Overflow is handled already by rust, so it doesn’t occur
  
Hint: NoHint
         
Explanation: The memory stack is full and overflows, so a default panic occurs                 and the program crashes

 

---

##### Character literals are specified using double quotes, as opposed to               single quotes which stand for string literals.  

- [ ]  True
- [x]  False
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Strings size is not known at compile time  

- [x]  True
- [ ]  False
  
Hint: hint
         
Explanation: explanation

 

---

##### "```  fn main() {
          let mut x = 2.0; 
      
          x: i32= 3.0; 
      }
 ```"
  

- [ ]  The code compiles without errors
- [ ]  The code has errors because of immutability
- [x]  The code has errors because of illegal type conversion
- [ ]  The code has errors because of no print and return statements
  
Hint: type declaration
         
Explanation: i32 is intialized as a float data type

 

---

##### If you want to store boolean values with the provision of adding more             values at runtime, the most suitable way would be to use  

- [ ]  Arrays
- [ ]  Tuples
- [x]  Vectors
- [ ]  bool type Variables
  
Hint: Statically and Dynamic in nature
         
Explanation: Vector is a Dynamic nature

 

---

##### BOOLEAN is a type of data type that basically gives a tautology or                fallacy.  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### What are the categories in which keywords are divided in rust?  

- [ ]  Weak
- [ ]  Strict
- [ ]  Reserved
- [x]  All of the above
  
Hint: NoHint
         
Explanation: No explanation

 

---

##### Which of the following can be used as a variable name in rust?  

- [ ]  crate
- [ ]  match
- [ ]  await
- [x]  tuple
  
Hint: NoHint
         
Explanation: Rest are keywords in rust

 

---

##### Identify the wrong set of rust keywords  

- [ ]  async, await, where, use
- [ ]  Move, return, mut, while
- [ ]  union, dyn, try, abstract
- [x]  become, box, do, incur
  
Hint: hint
         
Explanation: explanation

 

---

##### Rust variable names can start with  

- [x]  Letter, underscore
- [ ]  Letter, digits
- [ ]  Underscore, digits
- [ ]  All of the above
  
Hint: hint
         
Explanation: explanation

 

---

##### q What is the result of the following calculation in rust "1.0/0.0"
  

- [ ]  A positive number
- [x]  A negative number
- [ ]  An unsigned number
- [ ]  None of the above
  
Hint: hint
         
Explanation: explanation

 

---

##### In Rust, every value has its data type. The data type tells the compiler what kind of value it is and how to use it.  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: No explanation

 
