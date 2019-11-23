# Syntax

## Different ways of defining variables:

`val`'s cannot be reassigned. These can be typed: 
`val x: Int = ...`

`var`'s can be reassigned. 

# {} blocks
These cordon off a block where the output value is the last expression. 

# anonymous functions
example: 
`(x: Int) => x + 1`


# Defining functions
`val addOne = (x: Int) => x + 1`

For methods, often use `def`, e.g. 
`def add(x: Int, y: Int): Int = x + y`

a return type of `Unit` is like `void` in c++

# Classes
```
class A (param:String, paramtwo: String) {
  ...
}
```

**case classes** are immutable classes. 
**object**: single instance of its definition. 

to create a new object, use `new`, e.g.: 
```
class User {...}
val user1 = new User
```


