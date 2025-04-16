## **1. Linux File Hierarchy**
Linux has a **special directory structure** that organizes files in a **hierarchical tree** format.

### **Key Directories:**
1. `/` (Root) → Base of the Linux file system, contains all other directories.
2. `/bin` → Essential system commands like `ls`, `cp`, `pwd`.
3. `/boot` → Boot loader and kernel files (`grub`, `vmlinuz`).
4. `/dev` → Device files (`/dev/usb`, `/dev/tty1`).
5. `/etc` → System configuration files (`/etc/passwd`, `/etc/hosts`).
6. `/home` → Personal files for each user (`/home/user`).
7. `/lib` → Essential libraries required by binaries (`lib.so.*`).
8. `/media` → Mount points for external devices (`/media/cdrom`).
9. `/mnt` → Temporary mount directory for filesystems.
10. `/opt` → Additional software installed by the user.
11. `/sbin` → System administrator commands (`useradd`, `shutdown`).
12. `/tmp` → Temporary files that are deleted after reboot.
13. `/usr` → Stores user utilities, applications, and libraries.

---

## **2. Linux Text Editors**
Linux provides **command-line and graphical text editors** for file editing.

### **Command-Line Editors:**
- **VIM** → Advanced editor with multiple modes (command, insert, visual).
- **Nano** → Simple and user-friendly editor.
- **Emacs, Neovim** → Other advanced editors.

### **Graphical Editors:**
- **VS Code, Sublime, Gedit** → GUI-based editors for easier file management.

#### **Basic Commands for VIM:**
- Open file: `vim filename`
- Insert mode: Press `i`
- Save: `:w`
- Save & Quit: `:wq`
- Quit without saving: `:q!`
- Undo: `u`
- Copy & Paste in Visual Mode:
  - Select text: `v`
  - Copy: `y`
  - Paste: `p`
  - Delete: `d`

#### **Basic Commands for Nano:**
- Open file: `nano filename`
- Save: `Ctrl + S`
- Exit: `Ctrl + X`
- Undo: `Alt + U`
- Redo: `Alt + E`
- Copy: `Ctrl + Shift + C`
- Paste: `Ctrl + Shift + V`

---

## **3. Linux User Management**
Users in Linux have **different permissions and privileges**.

### **Types of Users:**
1. **Root User** (ID `0`) → Full administrative privileges.
2. **Normal User** (ID `1-999`) → Limited access.

### **Key Commands:**
- Check current user: `whoami`
- Create a user: `sudo useradd username`
- Add a user with details: `sudo adduser username`
- Switch to root: `sudo su`
- User details stored in:
  - `/etc/passwd` (User information)
  - `/etc/shadow` (Encrypted passwords)

---

