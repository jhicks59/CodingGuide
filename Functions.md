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
## A function named decision that handles a decision making process with multiple choices while supporting general outcomes and combat scenarios within a game

#### introPrompt: [String]: This is an array of strings that contains the introductory text or prompts that will be printed to the user.
#### choices: [String]: This is an array of strings that contains the possible choices the user can make after the introduction.
#### outcome: [String]: This is an array of strings that contains the outcome for each choice (used when combat == false).
#### combatChoices: [String] = [""]: This is an array of strings that contains the options available during a combat scenario (defaults to an array with an empty string if not provided). It is used when combat == true.
#### combat: Bool: This is a boolean flag that determines if the user is in a combat scenario. If combat == true, the choices relate to combat options; if combat == false, the choices are standard decisions.
```Swift
func decision( introPrompt: [String] , choices: [String], outcome: [String], combatChoices: [String] = [""], combat: Bool ){
```
#
## Display of intro prompt to set the scene for users
#### This loop goes through each string in the introPrompt array and prints it to the console. This is likely some introductory text to set the scene for the user.
```Swift
    for line in (introPrompt){
        print (line)
    }
```
#
## Displays choices
#### Similarly, this loop prints out each string in the choices array. These strings represent the available options for the user to choose from.
```Swift
    for line in (choices){
        print (line)
    
    }
```
#
## User Input Loop
#### The while !chosen loop ensures that the program keeps asking for input until the user selects a valid choice. readLine() is used to capture user input as a string.
#### The variable chosen is initially set to false and will be set to true once the user has made a valid selection.
### Handling Non-Combat Choices (combat == false):
#### If combat == false, the function will check the user’s input. Depending on whether the input is "1", "2", or "3", it will print the corresponding outcome from the outcome array.
#### After printing the outcome, chosen is set to true, meaning the user has made a valid selection.
#### The randomEvent() function is called after a valid choice, which could represent some other in-game event that occurs after making a decision (though we don't have the definition of randomEvent() here).
#### If the user enters an invalid input, the default case will print the fourth outcome (from outcome[3]), and the loop will continue.
### Handling Combat Choices (combat == true):
#### If combat == true, the function handles the input in a similar way, but the choices are taken from the combatChoices array.
#### The options are "1", "2", "3", or "4". Depending on the user's choice, the corresponding combat action is printed.
#### If the input is invalid, the default case prints the fifth option from combatChoices[4] (likely a message indicating an invalid input or some kind of error).
```Swift
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
#### The function continues to ask for input until the user provides a valid choice (either from the choices or combatChoices arrays). Once a valid choice is made, the appropriate message is printed, and the chosen flag is set to true, breaking the loop.
#
