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
#### introPrompt: [String]: This is an array of strings that contains the introductory text or prompts that will be printed to the user.
#### choices: [String]: This is an array of strings that contains the possible choices the user can make after the introduction.
#### outcome: [String]: This is an array of strings that contains the outcome for each choice (used when combat == false).
#### combatChoices: [String] = [""]: This is an array of strings that contains the options available during a combat scenario (defaults to an array with an empty string if not provided). It is used when combat == true.
#### combat: Bool: This is a boolean flag that determines if the user is in a combat scenario. If combat == true, the choices relate to combat options; if combat == false, the choices are standard decisions.
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
