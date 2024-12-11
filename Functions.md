# Functions - A group of statements that perform a task within specified parameters
### A function named openWelcome with no parameters and a return type of String
```Swift
func openWelcome() -> String {
    return "Hello, welcome to my app!"
}

print(openWelcome())
```
#
### A function named greeting with a parameter of type String named person and returns a String. Inside the function is a constant named greet that uses string concatenation to create a new string combined with the person parameter.
```Swift
func greeting(person: String) -> String {
    let greet = "Hello " + person + "! How are you today?"
    return greet
}

print(greeting(person: "Jeremiah"))
```
#### When called with defined parameters and printed the string "Hello Jeremiah! How are you today?" will display
