# Conditionals - Statements in code that run based on set conditions

### Else if statements

```swift
let myFavoriteMovieLengthInSeconds = 8820
/// this is a tests
if myFavoriteMovieLengthInSeconds < 8820 {
        print("That's not my favorite movie.")
        } else if myFavoriteMovieLengthInSeconds > 8820 {
        print("Not my favorite, but I might like it.")
        } else {
        print("That is my favorite move.")
```

### Switch Statements

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
