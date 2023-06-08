## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## OOPS(Object Oriented Programming)
 
 **Structs**        
- Structures aka structs are a group of related variable in one place and unlike an array struct can contain different data types.
- Each variable in a struct is known as a member.
- we can put all information about a users in a struct.
- Structs are similar to tuples Like tuples, the pieces of a struct can be different types. 
- Unlike with tuples, in a struct you'll name each piece of data so it's clear what the values mean.
- To define a struct, we enter the keyword struct and name the entire struct. 
- A struct's name should describe the significance of the pieces of data being grouped together.
- To define a struct, we enter the keyword struct and name the entire struct. 
- A struct's name should describe the significance of the pieces of data being grouped together.
- Inside curly brackets, we define the names and types of the pieces of data, which we call fields
- for example
  ```rust
      struct User {
           active: bool,
           username: String,
           email: String,
           sign_in_count: u64,
          }
            fn main() {}
  ```
- To use a struct after we've defined it, we create an instance of that struct by specifying concrete values for each of the fields.
- To get a specific value from a struct, we use dot notation.
- If the instance is mutable, we can change a value by using the dot notation and assigning into a particular field.
- We create an instance by stating the name of the struct and then add curly brackets containing key: value pairs, where the keys are the names of the fields and the values are the data we want to store in those fields.
- the struct definition is like a general template for the type, and instances fill in that template with particular data to create values of the type
- for example
  ```rust
    fn main() {
         let user1 = User {
             email: String::from("someone@example.com"),
             username: String::from("someusername123"),
             active: true,
             sign_in_count: 1,
           };
      }
  ```
- We can use methods on structure and this way the methods only works with the struct
- we use the 'impl' keyword to define a method within the context of a structure.
- The first parameter of a method will be always self, which represents the calling instance of the structure. 
- Lets illustrates
```rust
      //define dimensions of a rectangle
      struct Rectangle {
         width:u32, height:u32
      }

      //logic to calculate area of a rectangle
      impl Rectangle {
        fn area(&self)->u32 {
      //use the . operator to fetch the value of a field via the self keyword
        self.width * self.height
        }
      }
```
- We can create instances from other instances with Struct Update Syntax
- The syntax '..' specifies that the remaining fields not explicitly set should have the same value as the fields in the given instance.
- This help us keep a lesser code as it somehow Inherited what we want it to.
 
 **Type of Structs**        
- Structs in Rust come in three types: Structs with 
- named fields(regular),
- tuple structs, and
- unit structs.
- Regular/classic structs are the most commonly used. Each field defined within them has a name and a type, and once defined can be accessed.
- Adding pub to a field makes it visible to code in other modules, as well as allowing it to be directly accessed and modified.
- Tuple structs are similar to regular structs, but its fields have no names. They are used like tuples, with deconstruction possible.
- For accessing individual variables, the same syntax is used as with regular tuples, namely foo.0, foo.1, etc, starting at zero.
- Unit structs are most commonly used as marker. They have a size of zero bytes, but unlike empty enums they can be instantiated, making them isomorphic to the unit type ()
- Unit structs are useful when you need to implement a trait on something, but don’t need to store any data inside it.
- examples
  ```rust
      fn main() {
        struct Regular {
              field1: f32,
              field2: String,
              pub field3: bool
        }

        struct Tuple(u32, String);

        struct Unit;
        }
  ```
 
 **Destructing**        
- Destructuring is the process of breaking down items into their component parts, binding each to smaller variables.
  ```rust
    let (first, second) = (1, 2);
  ```
- Destructuring tuples is simple: just assign new variable names to each field of the tuple:
   ```rust
     struct TupleStruct(&'static str, i32);
     let my_tuple_struct = TupleStruct("foo", 123);
     let TupleStruct(foo, num) = my_tuple_struct;
  ```
- Destructuring structs is similar to destructuring tuple structs. Just use the field names:
  ```rust
      struct ArabianNights {
         name: String,
         stories: usize,
       }
      let teller = ArabianNights { 
      name: "Scheherazade".into(),
      stories: 1001 };
      {
      let ArabianNights { name, stories } = teller;
          println!("{} told {} stories", name, stories);
        }
  ```
  - Now, we access the name, and stories fields using the field names directly:
  - name instead of ArabianNights.name
  - stories instead of ArabianNights.age
  - Note that the name of the variables while destructuring should be the same as the name of the fields.
- Partial Destructing: The .. operator can be used to ignore some fields when destructuring:
  ```rust
      let ArabianNights { name, .. } = teller;
      println!("{} survived by her wits", name);
  ```
- Conditional Destructuring: Destructuring structs and tuples is infallible. However, enums can also be destructured, using the if let, while let, and match language constructs.
  ```rust
       if let Some(foo) = foo {
          println!("{:?}", foo);
        }
  ```
 
 **Intro to Enums**        
- An enum is short for enumerations. They look very similar to a struct, but are different.
- A value of the enum can match any of the variants. For this reason, an enum is sometimes called a ‘sum type’
- The set of possible values of the enum is the sum of the sets of possible values for each variant.
- The difference:
    - Use a `struct` when you want one thing AND another thing.
    - Use an `enum` when you want one thing OR another thing.
- Enums are for many choices together.
- Declaring an enum, write enum and use a code block with the options, separated by commas.
- We use the :: syntax to use the name of each variant: they're scoped by the name of the enum itself. 
- Enums are useful and more appropriate when working with IP addresses
- Two major standards are used for IP addresses: version four and version six.
- Any IP address can be either a version four or a version six address not both and this is a property that makes enums special
- An enum value can only be one of its variants
```rust
    fn main() {
        struct Ipv4Addr {
              // --snip--
        }

        struct Ipv6Addr {
            // --snip--
        }

        enum IpAddr {
         V4(Ipv4Addr),
         V6(Ipv6Addr),
            }
        }
  ```
- The code above illustrates that you can put any kind of data inside an enum variant: strings, numeric types, or structs.
- You can even include another enum!
- we're also able to define methods on enums.
- comparing enums and struct below. 
```rust
  enum Message {
     Quit,
     Move { x: i32, y: i32 },
     Write(String),
     ChangeColor(i32, i32, i32),
    }

 fn main() {}
```
- The struct equivalent is
```rust
  struct QuitMessage; // unit struct
  struct MoveMessage {
        x: i32,
        y: i32,
    }
  struct WriteMessage(String); // tuple struct
  struct ChangeColorMessage(i32, i32, i32); // tuple struct 

```
- We can also create an enum with no variants. These are known as zero-variant enums, and we cannot instantiate them.
- define below
  ```rust
      enum ZeroEnum {}
  ```
- We cannot cast zero variant enums to other types.
 
 **Option Enum and over null**        
- Option is another enum defined by the standard library.
- The Option type encodes the very common scenario in which a value could be something or it could be nothing.
- When used properly this functionality can prevent bugs that are extremely common in other programming languages.
- Rust doesn’t have the null feature that many other languages have.
- The problem with null values is that if you try to use a null value as a not-null value, you’ll get an error of some kind.
- Rust does not have nulls, but it does have an enum that can encode the concept of a value being present or absent. 
- This enum is Option<T> which is define as
```rust   
    #![allow(unused)]
    fn main() {
        enum Option<T> {
          None,
          Some(T),
          }
      }
```
- The Option<T> enum is so useful that it’s even included in the prelude; you don’t need to bring it into scope explicitly.
- Its variants are also included in the prelude: you can use Some and None directly without the Option:: prefix
- The Option<T> enum is still just a regular enum, and Some(T) and None are still variants of type Option<T>
- Example of using Option values to hold number types and string types:
```rust
    fn main() {
      let some_number = Some(5);
      let some_char = Some('e');

      let absent_number: Option<i32> = None;
    }
```
 
 **Traits**        
- A trait defines functionality a particular type has and can share with other types.
- We can use trait bounds to specify that a generic type can be any type that has certain behavior.
- To implement a trait, declare an impl block for the type you want to implement the trait for.
- The syntax is impl <trait> for <type>. 
- To define a trait, we use the trait keyword:
```rust
    trait WithName {
         fn new(name: String) -> Self;

         fn get_name(&self) -> &str;

         fn print(&self) {
           println!("My name is {}", self.get_name())
               }
          }
  ```
  -  While most traits exist to share behavior, Rust also has something called marker traits.
  - In a trait definition, we have access to a special type: Self.
  - Self is a special keyword that is only available within type definitions, trait definitions, and impl blocks.
  - We can use traits as function parameters to allow the function to accept any type that can do x, where x is some behavior defined by a trait.
  - We can also use trait bounds to refine and restrict generics, such as by saying we accept any type T that implements a specified trait.
  - Consider these two functions:
  ```rust
      use std::fmt::Debug;

      fn f(a: &Debug, b: &Debug) {
            todo!()
      }

      fn g<T: Debug>(a: &T, b: &T) {
            todo!()
      }
  ```
  - The function f will accept any two arguments that implement the Debug trait, even if they are two different types. 
  - On the other hand, g will only accept two arguments of the same type, but that type can be any type that implements Debug.
  - We can use traits as return types from functions. There are two different ways to do this: impl Trait and Box<dyn Trait>. 
  - You may want to use multiple traits together. This is what’s known as a trait combo.
  - Rust has a way to specify that a trait is an extension of another trait, giving us something similar to subclassing in other languages. we call them subtraits
  - Generics traits can do anything associated types can.
  - Although associated types constrains the implementing type to only have a single implementation of this trait. 
  - This is useful in a number of situations, such as in the Iterator and Deref traits.
  - Traits can also have associated constants. 
  - This is less common than trait methods, but is not without its uses.
  - Sometimes, implementing a trait requires implementing another trait:
  - Inherited traits looks like this
  ```rust     
    #![allow(unused_variables)]
    fn main() {
       trait Foo {
    fn foo(&self);
      }
    trait FooBar : Foo {
     fn foobar(&self);
      }
      struct Baz;

      impl Foo for Baz {
      fn foo(&self) { println!("foo"); }
        }

      impl FooBar for Baz {
      fn foobar(&self) { println!("foobar"); }
      }
    }
  ```
  - Drop trait lets us customize what happens when a value is about to go out of scope.
  - The Iterator trait implements the iterators over collections such as arrays.
  - Clone trait is for types that can make copies of themselves
  -
 
 **Traits and bounds**        
- Trait and lifetime bounds provide a way for generic items to restrict which types and lifetimes are used as their parameters.
- Bounds can be provided on any type in a where clause. 
- There are also shorter forms for certain common cases:
  * Bounds written after declaring a generic parameter: fn f<A: Copy>() {} is the same as fn f<A> where A: Copy () {}.
  * In trait declarations as bounds on associated types: trait A { type B: Copy; } is equivalent to trait A where Self::B: Copy { type B; }
- Bounds on an item must be satisfied when using the item
- Bounds that don't use the item's parameters or higher-ranked lifetimes are checked when the item is defined. 
- Lifetime bounds can be applied to types or to other lifetimes. 
- The bound 'a: 'b is usually read as 'a outlives 'b. 'a: 'b means that 'a lasts at least as long as 'b, so a reference &'a () is valid whenever &'b () is valid.
- Type bounds may be higher ranked over lifetimes. 
- These bounds specify a bound that is true for all lifetimes. 
- We can also specify multiple trait bounds to a generic type using the + symbol.
```rust
    impl<K: Hash + Eq, V> HashMap<K, V, RandomState>
```
- We can also combine traits to create a new traits.
- Debug is implemented by most standard library types and is a very convenient way to get a developer-friendly string representation of your types
- Defining Display for your own types is straightforward but needs to be explicit, since the compiler cannot reasonably guess what the output format must be (unlike with Debug)
- The write! macro is a relative of our friend println! where the first parameter is anything that implements Write
- Any type that implements Display automatically implements ToString
- Default is easy to implement for your own structs, providing the type of each field implements Default
- An important pair of traits is From/Into.
- From (and its mirror image Into) describe how distinct types are converted into each other
- Copy, Clone, and Sized bounds are also checked for certain generic types when using the item, even if the use does not provide a concrete type.
- Clone describes how a new value of the same type can be created.
- To clone a string involves allocating that buffer and copying the original bytes into it. 
- Copy is a marker trait (there are no methods to implement) which says that a type may be copied by just moving bits
- ? is only used to relax the implicit Sized trait bound for type parameters or associated types.
 
 **Polymorphism using trait objects**        
- polymorphism gives us the ability to present a single interface for potentially many different concrete types
- There are several practical advantages to using polymorphism, but one of the biggest is code re-use.
- Polymorphism allows us to create functions that accept any type, as long as those types exhibit certain behaviors or properties that we need them to have.
- There are two primary ways, and both of these have trade-offs to consider when it comes to performance as well as binary size:
    - Static Dispatch - this approach leverages generics (also called parametric polymorphism) and (usually) trait bounds to provide the flexibility we need while still maintaining full type safety, and without requiring a lot of duplicate code
    - Dynamic Dispatch - this approach uses “trait objects” to punt the decision of which type is required to satisfy some kind of polymorphic interface to runtime.
- we can define a generic type in the function signature, and then reference that type for one of the parameters:
  ```
    fn static_dispatch<T: Growler>(t: T) {
           t.growl();
        }
  ```
- Dynamic dispatch can be characterized as the opposite of static dispatch.
- Where static dispatch choses to create copies of all functions that use generic parameters and store these in the binary, dynamic dispatch choses to store only a single copy, but then calculates the necessary concrete implementation at runtime.
- In Rust, this approach leverages “Trait Objects” to achieve polymorphism
- Trait bounds is an optional constraint you can add to generic parameters.
- Trait objects actually cannot be used with generics at all, and instead are the required method for performing dynamic dispatch in Rust
 
 