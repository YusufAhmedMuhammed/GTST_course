## 1. 🧾 Introduction
BASH = Bourne Again Shell (command-line interface interacting with the Linux kernel).

Script: A .sh file containing shell commands used for:

Automation

System administration

DevOps workflows

Ethical hacking tools

## 2. ⚙️ Getting Started
File Extension: .sh (optional but recommended)

Shebang Line:

`#!/bin/bash`
Make Executable:

`chmod +x script.sh`

Run the Script:

`./script.sh      # Requires execute permission`
`bash script.sh   # No execute permission needed`
## 3. 🖨️ Output & Comments
Display Text:

`echo "Hello World"`

Single-line Comment:

`# This is a comment
`

Multi-line Comment (Not officially supported; use workaround):

`: <<'COMMENT'`
`This is a`
`multi-line comment.`
`COMMENT`
## 4. 💾 Variables
Assigning Variables:

`NAME="Nathan"  # No spaces around '='`
Accessing Variables:

`echo $NAME`

System Variables:

`echo $USER   # Current user`
`echo $PWD    # Current directory`
`echo $HOME   # Home directory`
## 5. 🧍 Input Handling
User Input:

`read -p "Enter name: " NAME`
`read -sp "Password: " PASS  # Silent input`

Script Arguments:

`# Run: ./script.sh Nathan Hailu`
`echo "Name: $1, Father: $2"`
## 6. 🍇 Arrays
Declare & Access:

`fruits=("apple" "banana" "mango")`
`echo "I love ${fruits[@]}"     # All elements`
`echo "First fruit: ${fruits[0]}"`
## 7. ➕ Arithmetic Operations
Using (( )):

`num1=10`
`num2=5`
`sum=$((num1 + num2))`

Using let:

`let "num1 += 3"`
## 8. 🔁 Conditionals
Numeric Comparison:

`if [ $num -gt 10 ]; then`
  `echo "Greater than 10"`
`fi`

String Comparison:

`if [ "$name" = "Nathan" ]; then`
  `echo "Welcome Nathan!"`
`fi`

Logical Operators:

`if [[ $age -gt 18 && "$role" = "admin" ]]; then`
  `echo "Access granted"`
`fi`
## 9. 🧪 Exercises
✅ Array Display

`fruits=("apple" "banana" "pineapple" "mango")`
`echo "I love ${fruits[@]}"`

🔐 Login Script

`read -p "Username: " user`
`read -sp "Password: " pass`
`echo`
`if [ "$user" = "gtst" ] && [ "$pass" = "1234" ]; then`
  `echo "Welcome to GTST!"`
`else`
  `echo "Access denied!"`
`fi`

➗ Math Validation

`read -p "Enter two numbers: " a b`
`sum=$((a + b))`
`if [ $sum -eq 10 ]; then`
  `echo "You are master!"`
`else`
  `echo "Poor at math..."`
`fi`
## 10. 💡 Key Tips
Use sleep 2 for timed delays.

Exit status:

`exit 0  # Success`
`exit 1  # Error`

Always quote variables:

`echo "$var"  # Prevent word splitting and globbing issues`