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
        - Scalar
            - single value
            - integers, floats, booleans, characters
        - Compound
            - tuple
                - let tup: (i32, f64, u8) = (500, 6.4, 1);
            - array