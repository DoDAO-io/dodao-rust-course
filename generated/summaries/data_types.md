## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Blockchain Basics
 
 **Typed language**        
- Dynamically-Typed Languages
  * Dynamically-typed languages are the languages where the interpreter assigns variables a data type at runtime based on the variable's value at that time.
  * Some Examples of Dynamically Typed Languages are:- JavaScript, Python, Perl, Ruby, etc.

- Statically-Typed Languages
  * Statically-typed languages are the languages where variable types are known at compile time i.e. the type checking is done at compile time.
  * Some examples of Statically-Typed Languages are:- C++, Rust, C, Java, etc.

- Rust is a Statically-Typed Language
 
 **Value Types**        
- Scalar Types
  * A scalar type represents a single value. Rust has four primary scalar types: integers, floating-point numbers, Booleans, and characters.

  - Integers
    * An integer is a number without a fractional component.
    * An integer can be of the following sizes:- 8-bit, 16-bit, 32-bit, 64-bit, 128-bit, arch.
    * Integers can be either signed or unsigned. Signed and unsigned refer to whether it’s possible for the number to be negative—in other words, whether the number needs to have a sign with it (signed) or whether it will only ever be positive and can therefore be represented without a sign (unsigned).
    * Integers can be declared using keyword let, and explicitly defining the variable size and it's type of signed or unsigned integer.
    * For example, we can declare a 64-bit signed and 32-bit unsigned integer in the following ways respectively :- 
    ```
        1. let mut x: i64 = -20;
        2. let mut x: u32 = 20;
    ```
    * The isize and usize types depend on the architecture of your build, which is denoted in the table as “arch”: 64 bits if you’re on a 64-bit architecture and 32 bits if you’re on a 32-bit architecture.
    * The number literals that can be multiple numeric types allow a type suffix, such as `20u32`, to designate the type. Number literals can also use `_` as a visual separator to make the number easier to read, such as `1_000` , which will have the same value as if you had specified `1000`.
    - Integer Overflow
      * Let’s say you have a variable of type u8 that can hold values between 0 and 255. If you try to change the variable to a value outside of that range, such as 256, integer overflow will occur, which can result in one of two behaviors:- 
        1. When you’re compiling in `debug` mode, Rust includes checks for integer overflow that cause your program to panic at runtime if this behavior occurs.
        2. When you’re compiling in release mode with the `--release` flag, Rust does not include checks for integer overflow that cause panics. Instead, if overflow occurs, Rust performs two’s complement wrapping.

  - Floating-Point Types
    * Floating-Point Types are number with the decimal points.
    * Floating-point types are f32 and f64, which are 32 bits and 64 bits in size, respectively.
    * All the Floating-Point Types are signed.
    * The default Floating-Point Type is of 64-bit.
    * The `f32` type is a single-precision float, and `f64` has double precision.
    * We can declare a float type variable in the following ways:- 
     ```
        fn main() {
              let x = 2.0; // f64
              let y: f32 = 3.0; // f32
        }
      ```
  - Boolean Type
    * There are two possible constant values:- True & False.
    * Booleans are one byte in size.
    * They are declared using the keyword 'bool'.

  - Character Type
    * Character Data Type doesn't use ASCII values like other programming languages but uses Unicode Scalar Value.
    * It uses 4 bytes i.e. 32 bits of space for each character rather than 1 byte because of Unicode Scalar Values.
    * We can use many more types of characters in rust, like, Chinese, emojis, etc.

- Compound Data Types
  * Compound types can group multiple values into one type. The two primitive compound types in rust are: Tuples and Arrays.

  - Tuples
    * A tuple is a general way of grouping together a number of values with a variety of types into one compound type.
    * Tuples have a fixed length: once declared, they cannot grow or shrink in size.
    * Tuples are created by a comma seperated List.
    * Each position in the tuple has a type, and the types of the different values in the tuple don’t have to be the same.
    * For Example:- 
      ```
        fn main() {
          let tup: (i32, f64, u8) = (500, 6.4, 1);
        }
      ```
    * We can access a tuple element directly by using a period `(.)` followed by the index of the value we want to access
    * The tuple without any values has a special name knows as "unit".
    * "unit's" value and its corresponding type are both written () and represent an empty value or an empty return type. 
    * Expressions implicitly return the unit value if they don’t return any other value. 

  - Arrays
    * Arrays are a collection of multiple values, stored in a single entity.
    * Unlike a tuple, every element of an array must have the same data type.
    * Arrays in Rust have a fixed length, i.e. they are not dynamic in nature by default.
    * Arrays are useful when you want your data allocated on the stack rather than the memory heap.
    * For Example:- 
      ```
        fn main() {
            let a: [i32; 5] = [1, 2, 3, 4, 5];
        }
      ```
      Here, i32 is the type of each element. After the semicolon, the number 5 indicates the array contains five elements.
    *  We can access elements of an array using indexing, like this:
      ```
        fn main() {
            let a = [1, 2, 3, 4, 5];
        
            let first = a[0]; // outputs 1
            let second = a[1]; // outputs 2
        }
      ```
 
 **Variables**        
- Variables and Mutability
  * In Rust, variables are immutable in nature by default.
  * When a variable is immutable, once a value is bound to a name, you can’t change that value
  * To make the variables mutable, we use the keyword:- `mut`.
  * For Example:-
    ```
      fn main() {
          let mut x = 5;
          println!("The value of x is: {x}");
          x = 6;
          println!("The value of x is: {x}");
      }
    ```
- Constants
  * Constants are values that are bound to a name and are not allowed to change, i.e. they are also immutable.
  * Usage of keyword `mut` isn't allowed with constants.
  * Constants are immutable by default, and also they’re always immutable.
  * We declare constants using the `const` keyword instead of the `let` keyword, and the type of the value must be annotated.
  * Constants can be declared in any scope, including the global scope, making them useful for values that many parts of code need to know about.
  * Constants may be set only to a constant expression, not the result of a value that could only be computed at runtime.
  * For Example:-
    ```
      const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
    ```
 
 **Keywords**        
- Strict Keywords
  * These keywords can only be used in their correct contexts. They cannot be used as the names of: Items, Variables and function parameters, etc.
  * For Example:- ` mut, break, else, continue, return, impl, etc. ` 

- Reserved Variables
  * These keywords aren't used yet, but they are reserved for future use. They have the same restrictions as strict keywords.
  * For Example:- ` abstract, try, do, final, typeof, etc. `

- Weak Keywords
  * These keywords have special meaning only in certain contexts.
  * For example, it is possible to declare a variable or method with the name `union`.
 
 **Bit Manipulation**        
- Bit Mnipulation is strictly done by rust compilers for storing data in variables, for two's compliment and many other purposes.
 
 **Strings**        
- String
  * A String is stored as a vector of bytes `(Vec<u8>)`.
  * It is guaranteed to always be a valid `UTF-8` sequence. 
  * String is heap allocated, growable and not null terminated.

- &str
  * `&str` is a slice `(&[u8])` that always points to a valid UTF-8 sequence.
  * It can be used to view into a String, just like `&[T]` is a view into `Vec<T>`.
 
 **Package Manager**        
- Cargo is the Rust package manager. 
 
 
