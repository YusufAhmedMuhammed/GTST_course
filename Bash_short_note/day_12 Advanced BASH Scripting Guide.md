Advanced BASH Scripting Guide

## 1. **Regular Expressions (Regex)**

### Key Metacharacters

| Symbol  | Description                          | Example                            |
|---------|--------------------------------------|------------------------------------|
| `.`     | Any character except newline         | `h.llo` → "hello", "hxllo"         |
| `^`     | Start of line                        | `^Hello` → Lines starting w/ Hello |
| `$`     | End of line                          | `world$` → Ends with "world"       |
| `+`     | One or more                          | `lo+l` → "lol", "loool"            |
| `*`     | Zero or more                         | `lo*l` → "ll", "lool"              |
| `?`     | Zero or one                          | `colou?r` → "color", "colour"      |
| `{n,m}` | Between n and m times                | `a{2,4}` → "aa", "aaa", "aaaa"     |
| `\d`    | Digit character                      | `\d\d` → "42"                       |
| `\w`    | Word character                       | `\w+` → "User123"                  |

### Email Validator Regex:
```bash
^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4}$
```

---

## 2. **Conditionals & Loops**

### Extended `if-elif-else`:
```bash
read -p "Enter score: " score
if [[ $score -ge 90 ]]; then
  echo "Grade A"
elif [[ $score -ge 80 ]]; then
  echo "Grade B"
else
  echo "Grade C"
fi
```

### Loop Types

**For Loop:**
```bash
for i in {1..5}; do
  echo "Iteration $i"
done
```

**While Loop:**
```bash
count=0
while [[ $count -lt 5 ]]; do
  echo "Count: $count"
  ((count++))
done
```

**Until Loop:**
```bash
count=10
until [[ $count -eq 0 ]]; do
  echo "Countdown: $count"
  ((count--))
done
```

**Select (Menu) Loop:**
```bash
PS3="Choose OS: "
select os in Linux Windows Mac; do
  case $os in
    Linux) echo "Open source!" ;;
    Windows) echo "Commercial OS" ;;
    Mac) echo "Unix-based" ;;
    *) break ;;
  esac
done
```

---

## 3. **Functions & Return Values**

### Basic:
```bash
greet() {
  echo "Hello $1!"
}
greet "Nathan"
```

### With Return Value:
```bash
power() {
  echo $(($1 ** $2))
}
result=$(power 4 2)
echo "4^2 = $result"
```

---

## 4. **Linux Integration**

### System Info Script:
```bash
#!/bin/bash
echo "System Info:"
date
uname -a
```

### Bulk File Rename:
```bash
for file in *.txt; do
  mv "$file" "${file%.txt}.bak"
done
```

---

## 5. **Key Exercises**

### 1. Email Validator:
```bash
read -p "Enter email: " email
regex="^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4}$"
if [[ $email =~ $regex ]]; then
  echo "Valid email!"
else
  echo "Invalid email!"
fi
```

### 2. Login System with 5 Attempts:
```bash
attempts=0
while [[ $attempts -lt 5 ]]; do
  read -p "Username: " user
  read -sp "Password: " pass
  echo
  if [[ $user == "admin" && $pass == "secret" ]]; then
    echo "Welcome!"
    exit 0
  else
    ((attempts++))
    echo "Remaining attempts: $((5 - attempts))"
  fi
done
echo "Account locked!"
```

### 3. Number Sequence:
```bash
read -p "Start: " start
read -p "End: " end
for ((i=start; i<=end; i++)); do
  printf "%02d " "$i"
done
```

---

## 6. **Pro Tips for Scripting Like a Pro**

- Use `set -e` to stop on errors
- Quote every variable: `"${var}"`
- Debug:  
  ```bash
  bash -x script.sh
  ```

- Cleanup with `trap`:
  ```bash
  trap 'rm -f tempfile' EXIT
  ```

---

Let me know if you want this packaged into a downloadable `.md` or if you want a **PDF or printable cheat sheet** version. Also happy to add **cron jobs**, **signal handling**, or **bash unit tests** if you’re taking it even further.