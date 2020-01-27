# Syntax

## Different ways of defining variables:

`val`'s cannot be reassigned. These can be typed: 
`val x: Int = ...`

`var`'s can be reassigned. 

`def` -> call-by-name
`val` -> call-by-value

## Misc Syntax
semicolon: this ends line (and can use this to get multiple expressions in a line). These are automatically added to the end of every line.

In order to get multiline expressions, can use ()'s, or put an operator at the end of the line.


# {} blocks
These cordon off a block where the output value is the last expression. 

# Anonymous functions
example: 
`(x: Int) => x + 1`


# Defining functions
`val addOne = (x: Int) => x + 1`

For methods, often use `def`, e.g. 
`def add(x: Int, y: Int): Int = x + y`

a return type of `Unit` is like `void` in c++

Functions can be defined and applied consecutively: 
e.g. if `f(x)` returns a function, then `f(x)(y)` calls the result on `y`. 

Since functions are allowed to have multiple parameter lists, `f(1st param)()` is automatically translated to `g()`. 

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

Standard syntax:

* `_x` -> private 
* `x` -> getter
* `x_` -> setter

```
class Point (var x: Int, var y: Int) {
  def move(dx: Int, dy: Int): Unit = { 
    ...
  }
  override def ...
}
```

`require(boolean, "error")` is a test performed on construction
`assert` -> this checks the code of a function

The default constructor runs all the code inside the function. 
`def this(...)` defines another constructor

Any method with one parameter can be called in an *infix* manner

`unary_<symbol>` defines a unary operator
precedence is defined by the first character

# Data Types

## Lists
`val list: List[Any] = List(...)`

## Tuple
` val ing = ("a", 23)` This is a class with type `Tuple2`
Access by looking at `ing._1, ing._2`. Can also pattern match with `(name, num) = ing`

# Functions

In general, in function `def`'s, parameters are call-by value (evaluate parameter before replacing). 
But if we do `y => Int` instead of `(y: Int)`, this does call-by-name (replace before evaluating parameter)

## Map
`s.map(x => x + 2)`
or `.map(_ + `)`
Methods can be used in a map, where they are coerced to functions.

# Operators

## Booleans
* `&&` is and
* `||` is or
