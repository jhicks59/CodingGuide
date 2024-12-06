# Conditionals - Statements in code that runs based on set conditions

### If Statements
#### Runs a block of code within braces based on set condtions after 'if'
```swift
let myFavoriteMovieLengthInSeconds = 8820

if myFavoriteMovieLengthInSeconds == 8820 {
print("This might be my favorite movie. What's the title?")
}
```

### Else-if statements
#### Runs certain blocks of code based on the condition(s) matching the code after 'if' or the alternitive code set after 'else if'. If none of the conditions are met then the code after the final 'else' runs.
```swift
let myFavoriteMovieLengthInSeconds = 8820

if myFavoriteMovieLengthInSeconds < 8820 {
        print("That's not my favorite movie.")
        } else if myFavoriteMovieLengthInSeconds > 8820 {
        print("Not my favorite, but I might like it.")
        } else if myFavoriteMovieLengthInSeconds == 8820 {
        print("That is my favorite movie.")
        } else {
        print("What's this movie called?"
        }
```

### Nested If statements
#### The use of an if statement inside of an if statement
```swift
let myFavoriteMovieLengthInSeconds = 8820

if myFavoriteMovieLengthInSeconds >= 8500  {
        if myFavoriteMovieLengthInSeconds == 8820 {
                print("This may be my favoite movie")}
} else {
print("I hated that movie")
}
```

### Switch Statements
#### Executes a block of code based on multiple alternatives
```swift
let myFavoriteMovieLengthInSeconds = 8820

switch myFavoriteMovieLengthInSeconds {
case 0...5000:
print("Wayy too short to be a good movie")
case 5001...7500:
print("Ok, we're getting somewhere but not quite there yet")
case 7501...9000:
print("This might be a great movie, let's watch it!")
default: 
print("What in the world is going on?")
}
```
