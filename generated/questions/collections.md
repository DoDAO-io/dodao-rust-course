## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Collections
 
 
---

##### Where in the mempry are colections stored
  

- [ ]  Stack
- [ ]  Program Area
- [x]  Heap
  
Hint: NoHint
         
Explanation: Collections are dynamically sized ans tored on heap.

Sub Topics: collection_introduction
 

---

##### What is the output of the following code snippet:
 
    ``` 
        let v = Vec![1,2,3,4,5];
        let third = &v[10];

        println!(“The third element is {}”, third);
    ```
  

- [ ]  It prints None
- [ ]  It does not print anything
- [ ]  It prints 5
- [x]  It will resume in panic
  
Hint: NoHint
         
Explanation: Trying to index vector outside it boundries result in panic.

Sub Topics: collection_vector
 

---

##### What is the output of the following code snippet:
 
    ``` 
        let v = Vec![1,2,3,4,5];
        let third = v.get(2);

        println!(“The third element is {}”, third);
    ```
  

- [x]  It prints None
- [ ]  It does not print anything
- [ ]  It prints 5
- [ ]  It will resume in panic
  
Hint: NoHint
         
Explanation: Trying to index vector outside it boundries result in panic.

Sub Topics: collection_vector
 

---

##### Strings in Rust support which encoding:
  

- [x]  UTF-8
- [ ]  Unicode
- [ ]  ASCII
- [ ]  UTF-32
  
Hint: NoHint
         
Explanation: Strings in Rust support UTF-8 encoding.

Sub Topics: collection_strings
 

---

##### What is the output of the following code snippet:
 
    ``` 
        let s1 = “Hello, “;
        let s2 = “world!“;
        let s3 = s1 + &s2;

        println!(s1 is {}”, s1);
    ```
  

- [x]  Program will not compile
- [ ]  It prints Hello, 
- [ ]  It prints Hello, world!
- [ ]  It prints None
  
Hint: NoHint
         
Explanation: When using + macro first argument is moved and not accessible after that.

Sub Topics: collection_strings
 

---

##### How can strings be indexed in Rust ?
  

- [ ]  `str[1]`
- [x]  String indexing does not works in Rust
- [ ]  `str.1`
- [ ]  `str.get(1)`
  
Hint: NoHint
         
Explanation: String indexing is not allowed in Rust.

Sub Topics: collection_strings
 

---

##### Which hashmap method can be used to add an entry to map only if it does not already exists ?
  

- [ ]  `insert`
- [ ]  `push`
- [x]  `or_insert`
- [ ]  `insert_or`
  
Hint: NoHint
         
Explanation: `or_insert` will insert an entry into HashMap only if it does not already exist.

Sub Topics: collection_hashmap
 

---

##### Which of the following are methods available on Vectors ?
  

- [ ]  `len`
- [ ]  `length`
- [ ]  `replace`
- [ ]  `push`
  
Hint: NoHint
         
Explanation: Methods `len` and `push` are available on Vectors.

Sub Topics: collection_vector
 

---

##### Vectors and HashMap needs to be explicitly included in the scope.
  

- [x]  True
- [ ]  False
  
Hint: NoHint
         
Explanation: Only HashMap need to be explicitly included in the scope.

Sub Topics: collection_vector
 

---

##### Which of the following are methods available on Strings ?
  

- [ ]  `index`
- [ ]  `length`
- [ ]  `contains`
- [ ]  `trim`
  
Hint: NoHint
         
Explanation: Methods `contains` and `trim` are available on Strings.

Sub Topics: collection_vector
 
