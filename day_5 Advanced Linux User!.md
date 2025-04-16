

## **1. Advanced User Management**
- **Change user password:** `sudo passwd username`
- **Change user ID:** `sudo usermod -u new_id username`
- **Delete user:** `sudo userdel -r username`
- **Switch user:** `su - username`
- **Create a home directory for a user:** `sudo mkhomedir_helper username`
- **Change user’s default shell:** `sudo usermod username -s /bin/bash`

### **Group Management**
- **Create a group:** `sudo groupadd groupname`
- **Add user to a group:** `sudo usermod -aG groupname username`
- **Check user’s group:** `groups username`
- **Remove user from a group:** `sudo gpasswd -d username groupname`

### **Sudoers File**
- Users must be added to the **sudoers file** to execute `sudo` commands.
- **Edit sudoers file:** `sudo visudo`
- Add: `username ALL=(ALL) ALL`

---

## **2. File Ownership & Permissions**
### **Ownership**
- Every file has an **owner** (user) and a **group**.
- **Change ownership:**  
  ```bash
  sudo chown user:group filename
  ```

### **File Permissions**
- **Three permission types:**  
  - **Read (r = 4)**  
  - **Write (w = 2)**  
  - **Execute (x = 1)**
- **Three permission groups:**  
  - **User (u)**
  - **Group (g)**
  - **Others (o)**

### **Changing Permissions**
#### **Symbolic method:**
- Add execute for all: `chmod a+x filename`
- Remove write for group: `chmod g-w filename`
- Give full permissions to user only: `chmod u+rwx filename`

#### **Numeric method:**
- **Each digit represents (user-group-other)**
- `chmod 777 file` → **Full permissions (rwx-rwx-rwx)**
- `chmod 640 file` → **User: rw-, Group: r--, Others: no access**
- `chmod 755 file` → **User: rwx, Group: r-x, Others: r-x**

### **Special Permissions**
- **SUID (4000)** → Runs as file owner.
- **SGID (2000)** → Runs as group.
- **Sticky Bit (1000)** → Prevents others from deleting a file.

---

## **3. Software & Package Installation**
### **APT (Advanced Package Tool)**
- **Update system repository:** `sudo apt update`
- **Search for a package:** `sudo apt search packagename`
- **Install a package:** `sudo apt install packagename`
- **Remove a package:** `sudo apt remove packagename`
- **Upgrade all packages:** `sudo apt upgrade`

### **Common Errors & Fixes**
- **"Could not get lock /var/lib/apt/lists/lock"** → Close other apt processes.
- **"Could not open lock /var/lib/dpkg/lock-frontend"** → Use `sudo`.
- **"Unable to locate package"** → Check for spelling errors.
- **"Repository error"** → Fix by updating sources: `sudo apt edit-sources`.

### **DPKG (Debian Package Manager)**
- **Used for offline installation (`.deb` files)**
- **Install a `.deb` package:** `sudo dpkg -i package.deb`
- **Remove a package:** `sudo dpkg -r packagename`
- **Purge a package (remove config too):** `sudo dpkg -P packagename`

---

## **4. Practical Tasks**
1. Create a user `gtst` and set password to `pass123`.
2. Change `Perm.txt` file owner to `gtst` and group to `root`.
3. Set `chmod 631` to `Perm.txt` (User: rw-, Group: --x, Others: --x).
4. Install and remove the package `cmatrix` using APT.

---

