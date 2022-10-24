## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## OOPS(Object Oriented Programming)
 
 
---

##### We take priority in naming struct more than tuples for which of the reason?
  

- [x]  it's clear what the values mean.
- [ ]  it's clear what the function mean.
- [ ]  it's clear what the struct mean.
- [ ]  it's clear what the tuples mean.
  
Hint: Naming clear up any misunderstanding
         
Explanation: Since structs can be a giant group of data we must know what it should contains by looking at the name

Sub Topics: structs
 

---

##### What is the keyword to start a structure in rust?
  

- [ ]  tuples
- [x]  struct
- [ ]  StruTs
- [ ]  fn
  
Hint: Nohint
         
Explanation: The standard keyword is needed to begin a structure just like fn is needed

Sub Topics: structs
 

---

##### Passing a struct to a function can be achieve with each notation
  

- [ ]  plot notation
- [ ]  not notation
- [x]  dot notation
- [ ]  rot notation
  
Hint: Nohint
         
Explanation: to access our struct

Sub Topics: structs
 

---

##### Rust also supports structs that look similar to tuples, and they are called
  

- [ ]  structs
- [x]  tuple structs
- [ ]  Major struct
- [ ]  Named structs
  
Hint: Nohint
         
Explanation: It looks like tuples with almost similar feature just as the name implies

Sub Topics: type-structs
 

---

##### which is best for creating a more complex data types?
  

- [ ]  Methods
- [ ]  Tuples
- [ ]  Array
- [x]  Structs
  
Hint: Nohint
         
Explanation: sturcts can be missed and used to pass different data and information

Sub Topics: structs
 

---

##### What is the output?
```rust
    struct Point {
       x: i32,
       y: i32,
      }

    fn main() {
         let origin = Point { x: 1, y: 0 }; // origin: Point

         println!("The origin is at ({}, {})", origin.x, origin.y);
    }
```
  

- [ ]   Point { x: 1, y: 0 }
- [ ]    x: 1, y: 0 
- [x]  The origin is at (0, 1)
- [ ]  The origin is at (1, 0)
  
Hint: We can call structs like parameter
         
Explanation: The aim here is to call the origin points from the point struct

Sub Topics: structs
 

---

##### By convention, structs begin with a ____
  

- [x]  capital letter
- [ ]  small letter
- [ ]  underscore
- [ ]  digit
  
Hint: Nohint
         
Explanation: naming convention

Sub Topics: structs
 

---

##### What method can we use to edit a struct?
  

- [x]  using the keyword mut
- [ ]  editing them on console
- [ ]  Using tuples
- [ ]  Freezing the cargo
  
Hint: Immutable data can become editable
         
Explanation: If we add the keyword mut to our struct we can edit it ar any time

Sub Topics: structs
 

---

##### What is the output?
```rust
  struct Point {
       x: i32,
       y: i32,
        }

  fn main() {
  let mut point = Point { x: 0, y: 0 };

     point.x = 5;

    println!("The point is at ({}, {})", point.x, point.y);
  }
```
  

- [ ]  compilation error
- [ ]  The point is at (5)
- [ ]  The point is at (0, 5)
- [x]  The point is at (5, 0)
  
Hint: The values in structs are immutable by default
         
Explanation: we make struct mutable and can now alter as we please

Sub Topics: structs
 

---

##### A struct can include __ to indicate that you want to use a copy of some other struct for some of the values
  

- [ ]  []
- [x]  ..
- [ ]  ??
- [ ]  {}
  
Hint: Struct Update syntax
         
Explanation: We can inherit instances of a struct and have a shorter code

Sub Topics: structs
 

---

##### what is the output?
```rust
   struct Rectangle {
      width: u32,
      height: u32,
   }

    fn main() {
      let rect1 = Rectangle {
         width: 30,
         height: 10,
        };

       println!(
         "The area of the rectangle is {} square pixels.",
          area(&rect1)
      );
    }

    fn area(rectangle: &Rectangle) -> u32 {
     rectangle.width * rectangle.height
   }

```
  

- [ ]  The area of the rectangle is 1500 square pixels.
- [ ]  The area of the rectangle is 10 square pixels.
- [ ]  The area of the rectangle is 30 square pixels.
- [x]  The area of the rectangle is 300 square pixels.
  
Hint: simple area of a rectangular but with structs
         
Explanation: we create a struct to store values of the rectangle and called it later

Sub Topics: structs
 

---

##### Which of the following is not a type of struct?
  

- [ ]  Unit structs
- [ ]  tuples structs
- [x]  Method structs
- [ ]  Regular/classic structs
  
Hint: Type of struct
         
Explanation: Method is a function, we can implement a method to a struct but its not a type of struct

Sub Topics: type-structs
 

---

##### The most common type of structs is
  

- [x]  Regular/classic
- [ ]  Regulated
- [ ]  Rectangle
- [ ]  Tuples
  
Hint: the type of struct you see everytime
         
Explanation: Classic struct can have all the data we need unlike the other type

Sub Topics: type-structs
 

---

##### To make a struct public, we can add ___ keyword
  

- [ ]  Public
- [ ]  Pub
- [x]  pub
- [ ]  publi
  
Hint: to make it accessible to the public
         
Explanation: Without the pub keyword other functions outside the scope will not be able to call it

Sub Topics: type-structs
 

---

##### What type of struct is used below?
```rust
    struct Color(i32, i32, i32);
    struct Point(i32, i32, i32);

    fn main() {
      let black = Color(0, 0, 0);
       let origin = Point(0, 0, 0);
    }
```
  

- [ ]  Unit
- [ ]  Regular
- [ ]  tuplet
- [x]  tuples
  
Hint: its variable are nameless
         
Explanation: Notice they have a type of field and not a name

Sub Topics: type-structs
 

---

##### What kind of struct is declared below?
```rust
    struct Electron;

    fn main() {
       let x = Electron;
     }
```
  

- [ ]  Regular
- [x]  Unit
- [ ]  Tuples
- [ ]  Array
  
Hint:  it's like an empty tuple
         
Explanation: Unit struct don't have any fields

Sub Topics: type-structs
 

---

##### How can a tuples be destructed?
  

- [x]  assign variable names to fields
- [ ]  assign already declared names to fields
- [ ]  seperate with names and comma
- [ ]  Create a struct and call it
  
Hint: destruct means breaking down item
         
Explanation: naming each fields in the tuples since its anonymous

Sub Topics: destruct
 

---

##### Destructing a struct is done via
  

- [x]  using the field names
- [ ]  calling the field names
- [ ]  declaring the field names
- [ ]  asigning the field names
  
Hint: Destruct of a struct is similar to the destruct of a tuple
         
Explanation: Using the field name so we directly call the variable with using the dot notation

Sub Topics: destruct
 

---

##### What is the symbol use to replace field we dont want when destructing?
  

- [ ]  ?
- [x]  ..
- [ ]  ::
- [ ]  {}
  
Hint: patial destructing
         
Explanation: it helps create a more clean code and ignore data you don't want to call at this particular time

Sub Topics: destruct
 

---

##### what feature allows the creation of a type which may be one of a few different variants.
  

- [ ]  structur
- [x]  enums
- [ ]  methods
- [ ]  tuples
  
Hint: it can be one or more data types
         
Explanation: Enum uses OR in its method, meaning different of same variant is possible

Sub Topics: enums
 

---

##### what kind of function is this?
```rust
    fn main() {
      enum Message {
          Write(String),
      }
    let m = Message::Write("This is Rust enum constructor".to_string());
    }
```
  

- [x]  enum constructor
- [ ]  Structs function
- [ ]  Methods
- [ ]  function
  
Hint: we called the enum like a function
         
Explanation: we can use this simpler method instead of creating another function

Sub Topics: enums
 

---

##### Rewrite the code below using an enum constructor
```rust
      fn bye(x: String) -> Message {
         Message::Write(x)
      }

       let x = bye("Bye, world".to_string());
      }
```
  

- [ ]  Not possible
- [ ]  let m = Message::Write('Hello, world'.to_string());
- [ ]  need to add enum to the end
- [x]   fn main() { enum Message { Write(String), } let m = Message::Write( 'Hello, world'.to_string()); }
  
Hint: You can get rid of the function bye
         
Explanation: enums create instances of each variants thereby shorten the code

Sub Topics: enums
 

---

##### What logical operator is more realted to enum?
  

- [ ]  AND
- [x]  OR
- [ ]  NOT
- [ ]  WITH
  
Hint: enum is the opposite of struct
         
Explanation: enum can be of one or same variant unlike struct

Sub Topics: enums
 

---

##### in Rust language, we can use 'Option<T>'enums to fulfil what ____ feature does in other languages
  

- [ ]  Compile
- [ ]  Calldata
- [ ]  struct
- [x]  null
  
Hint: it is replaced with a sub-enums feature in Rust in returning
         
Explanation: null is used to return nothing, we can use Option<T> enum which carry the comcept of null 

Sub Topics: option-enums
 

---

##### What is the syntax of Option<T> enum carrying the null concept?
  

- [x]  "
   enum Option<T> {
    None,
     Some(T),
 }"

- [ ]  enums-opt<T>
- [ ]  Option<T>
- [ ]  option<t>
  
Hint: It should return nothing
         
Explanation: The concept of null was created as a enum and it has nothing to return

Sub Topics: option-enums
 

---

##### An enums with no varians is called
  

- [x]  zero-variant enums
- [ ]  none-variant enums
- [ ]  no-variant enums
- [ ]  null-variant enums
  
Hint: it should return zero value but as a enum
         
Explanation: it is an empty enum and they cannot be instantiated. 

Sub Topics: enums
 

---

##### Below is the syntax of enums
```rust
    Enums name_of_enum{
      variant_1,
      variant_2,
      .
      .
      variant_n
    }
```
  

- [ ]  True
- [x]  False
  
Hint: enums syntax
         
Explanation: You can have many variants and also follow the proper naming style

Sub Topics: enums
 

---

##### An enum is sometimes called a sum type because
  

- [ ]  it is better than struct
- [x]  A value of the enum can match any of the variants
- [ ]  it contain many different variants
- [ ]  can be used as functions
  
Hint: Matching variant
         
Explanation: Enum values are the sum of the sets of values for each variant.

Sub Topics: enums
 

---

##### What is the output?
```rust
      enum Month_name {
        January,
        February,
        March,
        April,
        }
      fn main() {
        let apr = Month_name :: January;
        let feb = Month_name :: February;
        let mar = Month_name :: March;
        let jan = Month_name :: April;

         println!("{:?}",jan);
      }
```
  

- [ ]  January
- [ ]  Feburary
- [ ]  March
- [x]  April
  
Hint: showing how enums are declared and called
         
Explanation: we can simply call a data from enum into a function using ::

Sub Topics: enums
 

---

##### A ____ is a collection of methods defined for an unknown type: Self
  

- [ ]  Enums
- [x]  trait
- [ ]  tuples
- [ ]  structs
  
Hint: It is a language feature that communicate with the rust compiler about functionality
         
Explanation: it has similar feature as interface to java or abstract classes to C++

Sub Topics: trait
 

---

##### Traits can be implemented for ____ data type.
  

- [ ]  private
- [ ]  immutable
- [ ]  mutable
- [x]  any
  
Hint: it can be implemented easily
         
Explanation: it is like an extension for functionality and can be used everywhere

Sub Topics: trait
 

---

##### what is the output?
 ```rust
     struct Dog {
         name: String,
         age: u32, 
         owner: String
         }


     // Implementing an in-built trait ToString on the Dog struct
     impl ToString for Dog {
       fn to_string(&self) -> String{
         return format!("{} is a {} year old dog who belongs to {}.", self.name, self.age, self.owner);
         }
       }

     fn main() {
        let dog = Dog{name: "Fred".to_string(), age: 3, owner: "Mary".to_string()};
           println!("{}", dog.to_string());
         }
 ```
  

- [ ]  Fred is a dog who belongs to Mary.
- [x]  Fred is a 3 year old dog who belongs to Mary.
- [ ]  compilation error
- [ ]  Mary dog is 3 years old
  
Hint: Implementing a trait and inbuilt ToString method
         
Explanation: it was implemented on the dog struct and help us added more meaning to out program

Sub Topics: trait
 

---

##### The _____ keyword is primarily used to define implementations on types
  

- [ ]  self
- [x]  impl
- [ ]  Tostring
- [ ]  All of the above
  
Hint: you just to shorten the word and you get the keyword
         
Explanation: To implement some functionality for a type

Sub Topics: trait
 

---

##### What is the syntax for returning a trait-implementing value of some type from position
  

- [x]  impl Trait
- [ ]  trait
- [ ]  tup
- [ ]  pub
  
Hint: It is a keyword just like the impl but for traits
         
Explanation: implementation keyword can be used on trait as well which is especially useful in the context of closures and iterators

Sub Topics: trait
 

---

##### What trait lets us customize what happens when a value is about to go out of scope?
  

- [ ]  supertrait
- [ ]  iterator
- [ ]  Clone
- [x]  Drop
  
Hint: Nohint
         
Explanation: drop trait functionality is almost always used when implementing a smart pointer

Sub Topics: trait
 

---

##### which other feature restrict types and lifetimes to be used as parameters?
  

- [ ]  impl
- [x]  lifetime bounds
- [ ]  struct
- [ ]  supertraits
  
Hint: The other feature that can do this is trait
         
Explanation: we use it to ensure that references are valid as long as we need them to be

Sub Topics: trait-bounds
 

---

##### In a generic function, methods from Trait can be called on
  

- [x]  Ty values
- [ ]  Trait values
- [ ]  option values
- [ ]  assosiated values
  
Hint: Nohint
         
Explanation: its the rule

Sub Topics: trait-bounds
 

---

##### Which of the following is not a bound?
  

- [ ]  Copy
- [ ]  Clone
- [ ]  Sized
- [x]  tuples
  
Hint: type of bounds, notice the odd one out
         
Explanation: its not a bound it is more similar to struct

Sub Topics: trait-bounds
 

---

##### ? is only used alongside _____ bound to relax the implicit for type parameters
  

- [x]  Sized trait
- [ ]  Sized struct
- [ ]  clone trait
- [ ]  copy trait
  
Hint: It has a limit and ? help relax it
         
Explanation: This help create a relaxed sized with is not the same as an unsized trait

Sub Topics: trait-bounds
 

---

##### The code below is
```rust
      fn main() {
        pub trait Summarizable {
            fn summary(&self) -> String;
     }
    }
```
  

- [x]  A definition of a Summarize trait 
- [ ]  Implemantation of Summarize trait
- [ ]  Calling of Summarize trait
- [ ]  Summarize trait method
  
Hint: definiting a trait
         
Explanation: defining a trait is different from implementation of a trait

Sub Topics: trait
 

---

##### What feature allow us to presents a single interface for different types of concrete?
  

- [x]  polymorphism
- [ ]  tuples
- [ ]  trait
- [ ]  lifetimes
  
Hint: The ability to present data in different form
         
Explanation: to create more flexible APIs and more control by reusing code

Sub Topics: polymorphism
 

---

##### What options for polymorphism exist in Rust?
  

- [ ]  Copy and clone
- [ ]  Static and clone
- [x]  Static and Dynamic
- [ ]  Clone and dynamic
  
Hint: Nohint
         
Explanation: polymorphism can become complex and Rust only implemented what are needed

Sub Topics: polymorphism
 

---

##### While static dispatch choses to create copies of all functions, dynamic dispatch choses to store _____
  

- [ ]  two copies
- [x]  only a single copy
- [ ]  copies that are public
- [ ]  dynamic copies
  
Hint: Nohint
         
Explanation: It store as a dynamic which is a single generics copy

Sub Topics: polymorphism
 

---

##### Dynamic dispatch is also known as
  

- [ ]  Clone dsispatch
- [ ]  Trait
- [x]  parametric polymorphism
- [ ]  Maker
  
Hint: Nohint
         
Explanation: it is known as parametric becasue it uses leverage

Sub Topics: polymorphism
 

---

##### What is a trait ubder another trait called?
  

- [ ]  subclass
- [x]  Subtraits
- [ ]  mintrait
- [ ]  Traitpointer
  
Hint: one trait act like a parent
         
Explanation: The trait

Sub Topics: trait
 
