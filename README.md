# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

var problem = "split this string into words and print them on separate lines"
for a in problem.components(separatedBy: " ") {
print("\(a)")
}

```

Example

Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```


## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "

var condensedString = testString.replacingOccurrences(of: "  ", with: " ")

//condensedString = " How about thesespaces ? "
```


## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`

```swift
var reversed = sample.components(separatedBy: " ")
var answerQ3 = ""
for a in reversed {
answerQ3 = "\(a) " + answerQ3
}
print(answerQ3)
```


## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`

```swift
var sample = "danaerys dad cat civic bottle"
var palindromeCount = 0
for a in sample.components(separatedBy: " ") {
if a == String(a.reversed()) {
palindromeCount += 1
}
}
print(palindromeCount)
```


## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`

```swift
var L = "LLL"
var A = 0
for a in sampleQ5 {
if a == "P" {
continue
}else if a == "A" {
A += 1
}
}
if sampleQ5.contains(L) == true || A > 1{
print("false")
} else {
print("true")
}

```

## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`

```swift
var sampleQ6 = ("aa", "aaba")
var Ransom = sampleQ6.0
var Mag = sampleQ6.1
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
var vowelCountM = 0
var consonantCountM = 0
var vowelCountR = 0
var consonantCountR = 0
for a in Mag {
for b in vowels {
if a == b {
vowelCountM += 1
}
}
for c in consonants {
if c == a {
consonantCountM += 1
}
}
}

for a in Ransom {
for b in vowels {
if a == b {
vowelCountR += 1
}
}
for c in consonants {
if c == a {
consonantCountR += 1
}
}
}
if vowelCountR <= vowelCountM && consonantCountR <= consonantCountM {
print("true")
} else {
print("false")
}
```
