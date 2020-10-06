# Rust

## Rust Lang Book
<br/>

### Getting Started

- ! is a rust macro
- Compile ahead language - create binary and givee it to somebody else
- Packages of code are called crates

### Guessing game

- Prelude is a list of things that rust automatically imports.
- Variables are immutable by default. Use mut for mutability.
- :: in ::new means new is an associated function (static method in other languages) of string type.
- References are immutable by default. Use &mut for mutability.
- Result types are enums.
    - Ok
    - Err
        - expect for error handling

- Crates are collections of source code files (Python packages)
    - Types
        - Binary - executable
        - Library - to be used in other programs

- Traits
- match expression is made up of arms
    - arm consists of a pattern
- shadowing
    - use of same variable names for type casting


### Common programming concepts

- Variables
    - mut vs immutable
        - For example, in cases where you’re using large data structures, mutating an instance in place may be faster than copying and returning newly allocated instances. With smaller data structures, creating new instances and writing in a more functional programming style may be easier to think through, so lower performance might be a worthwhile penalty for gaining that clarity.

- Data types
    - Every value in rust is of a certain type
    - two subsets
        - stored in the stack, so dropped when variable goes out of scope
        - Scalar
            - single value
            - integers, floats, booleans, characters
        - Compound
            - tuple
                - let tup: (i32, f64, u8) = (500, 6.4, 1);
            - array

### Ownership

- Enables memory safety gurantees without garbage collector
- Managing heap data is why ownership exists
- Rules
    - Variables are owners 
    - Only one owner at a time 
    - value dropped when owner goes out of scope

- string literal vs String type
    - In case of string literal, values are hardcoded into the executable at compile, this make things faster
    - String::from requests memory from the heap
    - Memory is return when variable goes out of scope
        - drop function called by rust at closing }
        - double free error 
            - removal of two variables pointing to same memory locations.
            - solution?
                - move variable from original to the latest

- References
    - & - refer to values without taking ownership
    - borrowing
        - have functional parameters as References
    - Mutable References        
        - can only point to once piece of data
            - prevents data races at compile time
            - use scoping to overcome this
    - Slice 
  
        ``` 
        let s = String::from("hello); 
        let slice = &s[0..2];
        ```


### Structs 

- Similar to tuples but flexible, thanks to named properties.
  
``` 
struct User {
        username: String,
        email: String
      }
```

- struct update syntax - ..user1
- #[derive(Debug)] for debugging info
- methods
    - impl block
    - always has self pointing to struct
    - associated functions to generate new instance of struct


### Enums and pattern matching

```
enum IpAddrKind {
    V4,
    V6
}

```

- Option and match similar to scala
- if let for singular match patterns


### Packages, crates and modules

- 
         