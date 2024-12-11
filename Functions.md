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
#### When called with defined parameters and printed the string "Hello Jeremiah! How are you today?" will display.
#
### A decision making function that handles a decision making process with multiple choices while supporting general outcomes and combat scenarios within a game
```Swift
func decision( introPrompt: [String] , choices: [String], outcome: [String], combatChoices: [String] = [""], combat: Bool ){
```
#### test
```Swift
    for line in (introPrompt){
        print (line)
    }

    for line in (choices){
        print (line)
    
    }
    var chosen = false
    
    
    while !chosen {
        if let input = readLine(){
            if !combat {
                switch input {
                case "1":
                    print (outcome[0])
                    chosen = true
                    randomEvent()
                case "2":
                    print (outcome[1])
                    chosen  = true
                    randomEvent()
                case "3":
                    print (outcome[2])
                    chosen  = true
                    randomEvent()
                default:
                    print (outcome[3])
                }
            }
            if combat {
                switch input {
                case "1":
                    print (combatChoices[0])
                    chosen = true
                case "2":
                    print (combatChoices[1])
                    chosen  = true
                case "3":
                    print (combatChoices[2])
                    chosen  = true
                case "4":
                    print (combatChoices[3])
                    chosen = true
                default:
                    print (combatChoices[4])
                }
                
            }
        }
    }
}
```
####
#
