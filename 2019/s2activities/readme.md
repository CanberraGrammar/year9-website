# JavaScript to Swift Cheat Sheet

Feel free to add or update this cheat sheet by filing a pull request! Note, this is written in [GitHub Flavoured Markdown](https://github.github.com/gfm/), not ASCIIDoctor like the rest of the site.

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

## Variables vs. constants

If you declare a variable and you never change its value then you should declare it as a constant using the `let` keyword:

```swift
let myInt = 1;
let myString = "Hello"
```

They can be used exactly like a variable, just they cannot be changed - making your code safer and guarding against other parts of the program inadvertantly modifying data that should not be changed.

## Selection (if) statements - binary selection

Binary (if-else) selection in JavaScript:

```javascript
var myInteger = 5;

if (myInteger < 5) {
  console.log("My integer is less than 5");
}

else {
  console.log("My integer is greater than, or equal to, 5");
}
```

The equivalent in Swift:

```swift
let myInteger = 5

if myInteger < 5 {
  print("My integer is less than 5")
}

else {
  print("My integer is greater than, or equal to, 5")
}
```

The above has introduced a few new concepts, in addition to the if statement construct:

* In Swift you do not end lines with a semicolon `;`. You actually can and it won't error, but it's unnecessary.

* Do not bracket conditions on `if` statements in Swift. You only bracket conditions if there are multiple conditions, for example: `if (myInteger < 5) && (doStuff == true)`.

* If you want to print something to the console in Swift you use `print`. This is only useful for your own debugging, as on an iOS device the user obviously won't have access to the console!

## Selection (if) statements - multiway selection

Multiway selection in JavaScript:

```javascript
var myInteger = 5;

if (myInteger < 5) {
  console.log("My integer is less than 5");
}

else if (myInteger < 10) {
	console.log("My integer is less than 10");
}

else {
  console.log("My integer is greater than, or equal to, 5");
}

```

The equivalent in Swift:

```swift
var myInteger = 5
        
if myInteger < 5 {
   print("My integer is less than 5")
}
        
else if myInteger < 10 {
   print("My integer is less than 10")
}
        
else {
   print("My integer is greater than 10")
}
```

## Repetition (loop) statements - for loop (less than condition)

`for` loop in JavaScript:

```javascript
var myInteger = 5;

for (var i = 0; i < myInteger; i++) }
	console.log(i);
}
```

The equivalent in Swift:

```swift
var myInteger = 5;

for i in 0..<myInteger {
	print(i)
}
```

## Repetition (loop) statements - for loop (less than, or equal to, condition)

`for` loop in JavaScript:

```javascript
var myInteger = 5;

for (var i = 0; i <= myInteger; i++) }
	console.log(i);
}
```

The equivalent in Swift:

```swift
var myInteger = 5;

for i in 0...myInteger {
	print(i)
}
```

## Repetition (loop) statements - while loop

`while` loop in JavaScript:

```javascript
var myInteger = 5;

while (i <= 5) {
	print(i)
	i++;
}
```

The equivalent in Swift:

```swift
var i = 0
        
while i <= 5 {
   print(i)
   i += 1
}
```

Things to note:

* Notice how we cannot use `i++` in Swift? See [SE-0004](https://github.com/apple/swift-evolution/blob/master/proposals/0004-remove-pre-post-inc-decrement.md) for more details.

## Repetition (loop) statements - do while loop

`do while` loop in JavaScript:

```javascript
var myInteger = 5;

do {
	print(i)
	i = i + 1
} while (i <= 5)
```

The equivalent in Swift:

```swift
var myInteger = 5;
        
repeat {
   print(i)
   i += 1
} while i <= 5

```