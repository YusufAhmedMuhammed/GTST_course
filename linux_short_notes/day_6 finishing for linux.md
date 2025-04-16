Here’s a **short note** based on the **"Finishing for Linux!"** PDF:

---

## **Linux – Final Concepts (Short Notes)**

### **1. Script Installation**
- Many tools are open-source and hosted on GitHub.
- To install:
  ```bash
  git clone <repo-link>
  ```

### **2. Script Dependencies**
- Scripts need modules/libraries:
  - **Python**: `pip install -r requirements.txt`
  - **Go**: `go install <modulename>`
  - **Ruby**: `gem install <modulename>`

---

### **3. Getting Help in Linux**
- `man <command>`: Opens manual
- `<command> -h`, `--help`: Shows help text

---

### **4. Linux Processes & Services**
- View processes: `ps`, `ps -A`, `ps -u username`
- Kill process:
  ```bash
  kill <PID>         # Stop
  kill -19 <PID>     # Pause
  kill -18 <PID>     # Resume
  kill -9 <PID>      # Force stop
  killall <name>     # Kill all instances
  ```

- Real-time monitoring: `top`, `htop`
  - In `htop`, use `F9` to kill

- Background/Foreground:
  - Run in background: `command &`
  - Stop temporarily: `Ctrl + Z`
  - Resume: `fg`

---

### **5. Managing Services**
Using `systemctl`:
```bash
sudo systemctl start/stop/status <service>
sudo systemctl enable/disable <service>
```

---

### **6. Output Redirection & Null Device**
- Redirect errors only: `command 2> error.txt`
- Redirect standard output: `command 1> out.txt`
- Discard output: `command > /dev/null 2>&1`

---

### **7. Symbolic Linking**
- Like Windows shortcuts:
```bash
ln -s target_file link_name
```

---

### **8. Alias**
- Custom shortcut for commands:
```bash
alias rex='ls -la'
```
- To make it permanent:
  - Bash: `~/.bashrc`
  - Zsh: `~/.zshrc`
  - Fish: `~/.config/fish/config.fish`

---

### **9. Tmux (Terminal Multiplexer)**
- Split terminal into multiple panes.
- Start: `tmux`
- Custom config: `~/.tmux.conf`
- Common shortcuts:
  - Horizontal: `Ctrl+A o`
  - Vertical: `Ctrl+A e`
  - New tab: `Ctrl+A c`
  - Switch tab: `Ctrl+A <number>`
  - Exit: `Ctrl+A x`

---

### **10. wget**
- Download files:
```bash
wget <link>
```

---

### **11. find**
- Search for files/directories:
```bash
find / -name "filename"
find /home -perm 777
find -type f         # Files only
find -type d         # Directories only
```

---

