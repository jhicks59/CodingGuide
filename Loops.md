# Loops - runs a block of code repeatedly until a set condition becomes false
### for-in Loop - used to iterate over a sequence (like a range, array, dictionary, or string).
##### Syntax
```Swift
for item in sequence {
    // Code to execute for each item
}
  ```
##### Example
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
##### Example
```Swift
var number = 1

while number <= 10 {
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
##### Example
```Swift
var number = 1

repeat {
    print(number)
    number += 1
} while number <= 10

print("Ready or not, Here I come!")
```
#
### exiting loops - exit a loop using the `break` keyword
```Swift
// normal countdown
var countDown = 10

while countDown >= 0 {
    print(countDown)
    countDown -= 1
}

print("Blast Off!")
```
```Swift
// accelerated countdown using loop break
var countDown2

while countDown2 >= 0 {
    print(countDown2)

    if countDown2 == 4 {
        print("I'm bored. Let's go now!")
        break
    }
    countDown2 -= 1
}
```
#
### exiting multiple loops - the process of breaking a nested loops inner and outer loop simultaneously.
```Swift
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print("\(i) * \(j) is \(product)")

        if product == 50 {
            print("It's a bullseye!")
            break outerLoop
        }
    }
}
```
#
### skipping items in a loop using the `continue` keyword
