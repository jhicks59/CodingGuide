# Loops - runs a block of code repeatedly until a set condition becomes false
### for-in Loop - used to iterate over a sequence (like a range, array, dictionary, or string).
##### Syntax
```Swift
for item in sequence {
    // Code to execute for each item
}
  ```
### Example
```Swift
let albums = ["4", "Beyoncè", "Lemonade", "Renaissance"]

for album in albums {
    print("\(album) is now on Apple Music")
}
```
#
### while Loop - repeats as long as a condition is true. Used when the number of iterations is not predetermined.
##### Syntax
```Swift
while condition {
    // Code to execute while the condition is true
}
```
### Example
```Swift
var number = 1

while number <= 20 {
    print(number)
    number += 1
}

print("Ready or not, here I come!")
```
#
### repeat loop - similar to while loops, but the conditon is writtin at the end so that the code runs atleast once before checking the condition.
##### Syntax
```Swift
repeat {
    // some code to execute atleast once
} while // condition
```
```Swift
var number = 1

repeat {
    print(number)
    number += 1
} while number <= 20

print("Ready or not, Here I come!)
```
