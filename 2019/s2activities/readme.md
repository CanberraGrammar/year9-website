# JavaScript to Swift Cheat Sheet

## Declaring variables

Here are declarations for some variables in JavaScript:

```javascript
var myInt = 1;
var myString = "Hello";
var myBool = true;
var myArray = ["Hello", "World"]
var aMystery;
```

Here are the declarations for the same variables in Swift:

```swift
var myInt: Int = 1;
var myString: String = "Hello"
var myBool: Bool = true;
var myArray: Array<String> = ["Hello", "World"]
```

In fact, similar to JavaScript, you don't need to declare the data type:

```swift
var myInt = 1;
var myString = "Hello"
var myBool = true;
var myArray = ["Hello", "World"]
```

Swift has a *type inference* engine which can determine the data type based upon the inital value assigned to the variable.

However, if you need to declare a variable and it does not have an initially assigned (so the variable is initialised as `nil`), such as `aMystery` then you **must** specify the data type.

```swift
var aMystery: Int?
```

Swift is a *strongly typed* language so all variables need a specific data type, unlike JavaScript which is *weakly typed* and does not have this requirement. You might also notice the `?`. This is called an optional, and we will discuss that later.

## Variables vs. Constants

If you declare a variable and you never change its value then you should declare it as a constant using the `let` keyword:

```swift
let myInt = 1;
let myString = "Hello"
```

They can be used exactly like a variable, just they cannot be changed - making your code safer and guarding against other parts of the program inadvertantly modifying data that should not be changed.