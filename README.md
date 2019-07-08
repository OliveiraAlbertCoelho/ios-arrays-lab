# Arrays lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

Create an array of strings called `colors` that contain "orange", "red", "yellow", "turquoise", and "lavender".

Then, using array subscripting and string interpolation, print out the String `"orange, yellow, and lavender are some of my favorite colors"`.
```swift
var color: [String] = ["orange", "red", "yellow", "turquoise","lavender"]
print("\(color[0]), \(color[2]) and \(color[3]) are some of my favorite colors")

```

## Question 2

Remove "Illinois" and "Kansas" from the array below.
```swift
var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]
westernStates.remove(at: 5)
westernStates.remove(at: 4)
print(westernStates)

```
## Question 3

Iterate through the array below. For each state, print out the name of the state, a colon, and whether it is or is not **in the continental United States.**

```swift
let moreStates: [String] = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]

for i in moreStates {
if i != moreStates[0] && i != moreStates[2]{
print("\(i): continental United States")
} else {
print("\(i): not continental United States")
}
}
```

## Question 4

Print out how many non-whitespace characters are in `myString`:

`let myString = "This is good practice with Strings!"`
```swift
let myString = "This is good practice with Strings!"
var whiteSpace = 0
for i in myString {
if i != " "{
whiteSpace += 1
}
}
print(whiteSpace)
```

Iterate through the array below. For each sentence, print out how many non-whitespace characters are in it.

`let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]`
```swift
var whiteSpace = 0
var counter = 0
let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]
for i in myFavoriteQuotes {
for a in myFavoriteQuotes[counter]{
if a != " "{
whiteSpace += 1
}

}
counter += 1
print("the line \(i) has a total of \(whiteSpace) non-whitespace characters  " )
whiteSpace = 0
}
print(whiteSpace)

```

## Question 5

Iterate through `garden` and place any 🌷 that you find into the `basket`. Replace any 🌷 that you pick up with `"dirt"`. Then print how many 🌷 are in your `basket`.

```swift
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()
var counter = 0
for i in garden {
if i == String("\u{0001f337}"){
garden[counter] = "dirt"
basket.append("\u{0001f337}")
}
counter+=1
}
print("Garden array: \(garden)")
print("Basket array: \(basket) has a total of \(basket.count) flowers")



```

## Question 6

The below array represents an unfinished batting lineup for a baseball team. **You, the coach,** need to make some last minute changes:

- Add "Suzuki" to the end of your lineup.
- Change "Jeter" to "Tejada".
- Change "Thomas" for "Guerrero"
- Put "Reyes" to bat 8th instead.

`var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]`
```swift
var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]
var counter = 0
for i in battingLineup {
if i == "Jeter"{
print(i)
battingLineup[counter] = "Tejada"
}
if i == "Thomas" {
battingLineup[counter] = "Guerrero"

}
counter += 1

}
battingLineup.append("Suzuki")
battingLineup.swapAt(0, 7)
print(battingLineup)
```

## Question 7

Given an array of Ints, find out if it contains a target number.  

(The built-in `contains(_:)` function will do this, but you aren't allowed to use it for this exercise.)


```swift
var numbers: [Int]

let target: Int = 32
```

Ex.1

```swift
numbers = [4,2,6,73,32,4,2,1]

target = 32

//true
```

Ex. 2

```swift
numbers = [32459,2,4,5,1,4,2,1]

target = 3

//false
```
```
var numbers = [4,2,6,73,32,4,2,1]
var some = false
let target: Int = 32
for i in numbers {
if i == target {
some = true
}
}
print(some)


```

## Question 8

Find the largest value in an array of Int.  Do not use the built-in `max()` method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.

let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var greatest = -1000
for i in arrayOfNumbers {
if i > greatest {
greatest = i
}
}
print(arrayOfNumbers)
print(greatest)




```


## Question 9

Find the smallest value in an array of Int.  Do not use the built in min() method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.


let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var smallest = 1000
for i in arrayOfNumbers {
if i < smallest {
smallest = i
}
}
print(arrayOfNumbers)
print(smallest)

```


## Question 10

Iterate through `secondListOfNumbers`, and print out all the odd numbers.

`var secondListOfNumbers = [19,13,14,19,101,10000,141,404]`
```swift
var secondListOfNumbers = [19,13,14,19,101,10000,141,404]
for i in secondListOfNumbers {
if i%2  != 0{
print(i)
}
}

```

## Question 11

Iterate through `thirdListOfNumbers`, and print out the sum.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`
```swift
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sum = 0
for i in thirdListOfNumbers {
sum += i
}
print(sum)

```

## Question 12

Iterate through `thirdListOfNumbers`, and print out the sum of all the even numbers.

`var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]`
```swift
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sum = 0
for i in thirdListOfNumbers {
if i % 2 == 0{
sum += i
}}
print(sum)

```

## Question 13

Append every Int that appears in both `listOne` and `listTwo` to the `sharedElements` array. Then print **how many Ints** are shared.

```swift
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()
for i in listOne {
for b in listTwo {
if i == b {
sharedElements.append(b)
}
}
}
print(sharedElements)

```


## Question 14

Write code such that `noDupeList` has all the same Ints as `dupeFriendlyList`, but has no more than one of each Int.

```swift
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []
for i in dupeFriendlyList {
if !noDupeList.contains(i){
noDupeList.append(i)
}
}
print(noDupeList)
```

## Question 15

Find the second smallest number in an Array of Ints

`let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}`
```swift

let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var small = Int.max
var secSmall = Int.max

for i in arrayOfNumbers {
if i < small {
small = i //
}
}

for i in arrayOfNumbers {
if i < secSmall && i != small {
secSmall = i
}
}
print(secSmall)

```

## Question 16

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.
```swift
var sum = 0
for i in 1..<100 {
if i % 3 == 0 || i % 5 == 0 {
sum += i
}
}
print(sum)
```
## Question 17

Make an array that contains all elements that appear **more than twice** in `someRepeatsAgain`.

```swift
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]
```


## Question 18

Identify if there are 3 integers that sum to 10 in the following array. If so, print them as a triplet. If there are multiple triplets, print all possible triplets.

```swift
var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]
for a in tripleSumArr {
for b in tripleSumArr {
for c in tripleSumArr{
if a+b+c == 10{
print("\(a),\(b),\(c) , triplets")
}
}
}
}
```


## Question 19

Given an array of Strings, find the the String with the most "a"s in it.

input: `["apes", "abba", "apple"]`

output: `"abba"`
```swift
var input = ["apes", "abba", "apple", "aaaaa"]
var more = 0
var secondMost = 0
var counter = 0
var winner = ""
for i in input {
for a in input[counter]{
if a == "a" {
more += 1
}

}
if more > secondMost {
secondMost = more
winner = ""
winner += i
}
more = 0

counter += 1
}
print(winner)


```


## Question 20

Given an Array of Arrays of Ints, find the Array of Ints with the largest sum:

Input: `[[2,4,1],[3,0],[9,3]]`

Output: `[9,3]`
```swift
var input = [[2,4,1],[3,0],[9,3]]
var sum = 0
var biGsum = 0
for a in 0..<input.count {
for b in input[a] {
sum += b
}
if sum > biGsum {
biGsum = sum
}
sum = 0
}
print(biGsum)

```


## Question 21

Given an Arr ay of Tuples of type `(Int, Int)`, create an array containing all the tuples where the first Int is equal to the second Int.

Input: `[(4,2), (-3,-3), (1,1), (3,9)]`

Output: `[(-3,-3), (1,1)]`
```swift

let tuppleArray = [(4,2), (-3,-3), (1,1), (3,9)]
var holderTupple: [(Int, Int)] = []
for i in tuppleArray {
if i.0 == i.1 {
holderTupple.append((i))
}
}
print(holderTupple)

```




## Question 22

Given an Array of Bools, make a variable called `allAreTrue` that is true if all of the Bools are true and false if any of them are false.

Input: `[true, false, true, true]`

Output: `false`
```swift
var input = [true, true, true, true]
var allAreTrue = true
for i in input {
if i != true {
allAreTrue = false
}
}
print(allAreTrue)
```


## Question 23

Given an Array of Ranges of Ints, create an array that has all the values from all the ranges in order from smallest to greatest with no duplicates.

Input: `[0..<3 , 2..<10, -4..<6, 13..<14]`

Output: `[-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10,13]`
```swift
var arrayOfRanges = [0..<3 , 2..<10, -4..<6, 13..<14]
var sortedRanges = [Int]()
for i in arrayOfRanges {
for b in i {
if !sortedRanges.contains(b){
sortedRanges.append(b)
}}
}
sortedRanges.sort()
print(sortedRanges)
```


## Question 24

Given an array of Characters, create a String ignoring and uppercase Characters and spaces.  Then uppercase every other character of the String.

Input: `let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C,"e"]`

Output: `"ApLeAuE"`
```swift

let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C","e"]
var word = ""
var counter = 0
for i in arr where i != " " {
if i != Character(i.uppercased()) {
if counter % 2 == 0{
word += i.uppercased()
}else {
word += String(i)
}
counter += 1
}}
print(word)
```

## Question 25

Print out each element in `myMatrix`

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`
```swift
var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]
for i in myMatrix {
for b in i {
print(b)
}
}

```

## Question 26

Print out the sum of the diagonals of `myMatrix`.

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`
```swift

var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]
var counter = 0
var diagonalsSum = 0
for i in myMatrix {
for b in i {
if counter % 2 == 0 {
diagonalsSum += b
}
counter += 1
}
}
print(diagonalsSum)

```

## Question 27

Using for loops, rotate `matrixToRotate` 90 degrees.

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

![Matrix Rotation](images/rotated_matrix.jpeg)
```swift
var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
var secMatrix = Array(repeating: Array(repeating: 0, count: matrixToRotate.count),count: matrixToRotate.count)
for i in 0..<matrixToRotate.count {
for  b in 0..<matrixToRotate[i].count {
secMatrix[i][b] = matrixToRotate[matrixToRotate[i].count-1-b][i]
}
}
print(secMatrix)


```
