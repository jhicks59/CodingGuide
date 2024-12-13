# Complex Types
## Arrays - collections of data stored in a single named group
##### best used when data stored has duplicates, or the order of the data matters
```Swift
let john = "John Lennon"
let paul = "Paul McCartney"
let george = "George Harrison"
let ringo = "Ringo Starr"

let beatles = [john, paul, george, ringo]

print(beatles[1])
```
#
## Set - collections of unique data stored in a random order
##### best used to store unique values
```Swift
let colors = Set(["red", "blue", "green"])
let colors2 = Set(["red", "blue", "green", "red", "blue"])
```
#
## Tuples - stores several value together within a single value but are fixed in size and the types cannot be changed once created
##### best used for precise date such as a location or name
```Swift
var name = (first: "Taylor", last: "Swift")
print(name.0)
print(name.last)
```
