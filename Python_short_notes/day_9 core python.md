

## 1. Indexing and Slicing
Indexing: Access items using their position (starting at 0).


`languages = ["Python", "Swift", "C++"]==`
`==print(languages[0])  # Output: Python==`

Negative Indexing: Access items from the end.

`print(languages[-1])  # Output: C++`

Slicing: Extract sub-parts using [start:stop:step]

`name = 'No 1 is Nathan'`
`print(name[8:14])  # Output: Nathan`
## 2. Input Handling
Using input(): Takes string input from the user.

`name = input("Enter your name: ")`
`print(f"Hello {name}!")`

Command-Line Arguments (sys.argv):

`import sys`
`print(f"Hello {sys.argv[1]}!")`

Note: sys.argv[0] is the filename itself.

## 3. Operators

Arithmetic: +, -, *, /, %, **

Assignment: =, +=, -=, etc.

Comparison: , !=, >, <, >=, <=

Logical: and, or, not

Bitwise: &, |, ^, ~, <<, >>

Example:

`x = 10`
`y = 5`
`print(x > y and x != y)  # Output: True`
## 4. Control Flow
Conditional Execution:

`if number > 0:`
    `print("Positive")`
`elif number == 0:`
    `print("Zero")`
`else:`
    `print("Negative")`
    
Nested if: Place one if inside another.

## 5. Error Handling
Handle errors using try-except blocks.


`try:`
    `result = 10 / 0`
`except ZeroDivisionError:`
    `print("Cannot divide by zero!")`
    
Optional: Use finally for cleanup actions, or else if no exception occurs.

## 6. Loops

for Loop:

`for i in range(5):`
    `print(i)  # 0 to 4`

while Loop:

`count = 0`
`while count < 5:`
    `print(count)`
    `count += 1`
    
break: Exit the loop early.

continue: Skip to next iteration.

## 7. Exercises & Assignments
Try implementing:

🔐 Username/password sorter

🎲 Number guessing game

✅ Login system with dictionary & loops

