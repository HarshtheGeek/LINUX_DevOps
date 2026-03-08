# LINUX_DevOps

## 1) How Does the Internet Work?

At a high level, the internet is a global network of interconnected computers that communicate using standardized protocols.

### Core Components

**1. Client**

* Your device (browser, mobile app).
* Initiates requests.

**2. Server**

* A machine that responds to client requests.

**3. IP Address**

* Unique address of a device on a network.
* Example: `142.250.183.14`

**4. DNS (Domain Name System)**

* Converts domain names (e.g., google.com) → IP addresses.
* Like a phonebook for the internet.

**5. Protocols**

* HTTP/HTTPS → Web communication
* TCP → Reliable data transfer
* UDP → Faster, less reliable transfer
* SSL/TLS → Encryption

---

### Step-by-Step Flow (When You Open a Website)

1. You type `example.com` in the browser.
2. DNS resolves it to an IP address.
3. Browser sends an HTTP request to that IP.
4. Server processes the request.
5. Server sends back a response (HTML/CSS/JS).
6. Browser renders the page.

This is called the **request-response cycle**.

---

## 2) What is a Server?

A server is a machine (physical or virtual) that provides services to other machines.

### Types of Servers

* Web Server
* Application Server
* Database Server
* File Server
* Mail Server

### Important:

A server is not defined by hardware — it is defined by **role**.

Example:

* Your laptop can act as a server if it hosts an API.

---

## 3) Difference Between Web Server and Application Server

| Feature        | Web Server           | Application Server     |
| -------------- | -------------------- | ---------------------- |
| Main Role      | Serve static content | Execute business logic |
| Content        | HTML, CSS, images    | Dynamic responses      |
| Examples       | Nginx, Apache        | Node.js, Spring Boot   |
| Speed          | Very fast            | Slightly heavier       |
| Logic Handling | Minimal              | Full business logic    |

### Flow in Real Architecture

Client → Web Server → Application Server → Database

Example:

* Nginx (web server) handles static files.
* Node.js (application server) handles API logic.

---

## 4) Types of Applications

### 1. Standalone Applications

* Run on a single machine.
* No internet required.
* Example: MS Word.

### 2. Web Applications

* Accessed via browser.
* Hosted on remote server.
* Example: Gmail.

### 3. Mobile Applications

* Installed on mobile devices.
* Can be native or hybrid.
* Example: WhatsApp.

### 4. Distributed Applications

* Components spread across multiple servers.
* Example: Microservices architecture.

---

## 5) What are Standalone Apps?

Applications that:

* Run locally.
* Do not require server interaction.
* Store data locally.

Examples:

* VLC
* Calculator
* Offline IDE

### Architecture

User → App → Local OS → Local Storage

No network dependency.

---

## 6) What are Web Applications?

Applications hosted on a server and accessed through browsers.

### Characteristics

* Client-Server architecture
* Centralized data
* Scalable
* Requires internet

### Architecture

Browser (Frontend)
↓
Web Server
↓
Application Server
↓
Database

Examples:

* Amazon
* LinkedIn
* GitHub

---

## 7) What is Application Support?

Application support refers to maintaining and monitoring live applications to ensure smooth operation.

### Responsibilities

* Monitoring logs
* Fixing bugs
* Restarting services
* Handling production issues
* Performance optimization

### Tools Used

* Linux commands (top, ps, netstat)
* Monitoring tools (Prometheus)
* Log tools (ELK Stack)

This is operational maintenance of a running system.

---

## 8) What is Application Maintenance?

Maintenance focuses on long-term improvement and sustainability.

### Types

1. Corrective Maintenance
   Fixing defects.

2. Adaptive Maintenance
   Updating due to OS/library changes.

3. Perfective Maintenance
   Adding enhancements.

4. Preventive Maintenance
   Refactoring for future stability.

---

## DevOps Perspective

* Internet → Communication layer
* Server → Hosting layer
* Web/App Server → Execution layer
* Support → Operational layer
* Maintenance → Lifecycle layer


## What is UNIX?

**UNIX** is a multiuser, multitasking operating system originally developed in 1969 at **Bell Labs** by **Ken Thompson**, **Dennis Ritchie**, and others.

It was designed to be:

* Simple
* Portable
* Powerful for developers
* Based on small, modular tools

UNIX became the foundation for many modern operating systems.

---

## Core Characteristics

### 1. Multiuser

Multiple users can access the system simultaneously via terminals.

### 2. Multitasking

Multiple processes can run concurrently.

### 3. File-Centric Design

Everything is treated as a file:

* Regular files
* Directories
* Devices
* Processes

### 4. Hierarchical File System

Single root directory `/`
All files branch from this root.

### 5. Shell + Kernel Architecture

* **Kernel** → Core of the OS (manages memory, CPU, processes, devices)
* **Shell** → Command-line interface (bash, sh, ksh, etc.)

---

## UNIX Architecture (Conceptual View)

**Layers:**

1. Hardware
2. Kernel
3. Shell
4. User Applications

---

## Key UNIX Commands

| Command | Purpose                 |
| ------- | ----------------------- |
| `ls`    | List files              |
| `cd`    | Change directory        |
| `pwd`   | Print working directory |
| `cp`    | Copy files              |
| `mv`    | Move/rename files       |
| `rm`    | Remove files            |
| `grep`  | Search text             |
| `chmod` | Change file permissions |

---

## Why UNIX Was Revolutionary

* Written in C → portable across hardware
* Introduced pipes (`|`) for chaining commands
* Encouraged modular tool design
* Influenced modern OS design principles

---

## UNIX vs Linux

**Linux** is **not UNIX**, but it is *Unix-like*.

Linux was created by **Linus Torvalds** in 1991 and follows UNIX principles.

Other Unix-based systems:

* **macOS**
* **FreeBSD**
* **Solaris**

---

## Where UNIX Is Used

* Servers
* Supercomputers
* Networking infrastructure
* Enterprise systems
* Development environments

---

## In One Line

UNIX is a powerful, multiuser operating system that shaped nearly every modern OS used today.

If you want, I can also explain:

* UNIX internals (process scheduling, memory management)
* Difference between Kernel and Shell in depth
* How UNIX handles processes (fork, exec)
* Or compare UNIX with Windows from an OS design perspective

# Linux Kernel?

The Linux kernel is the core component of the Linux operating system.

It sits between:

**Hardware**
**User applications**

- It controls how software talks to hardware.
- Without the kernel, the operating system cannot function.
- It is software basically

## Bootloader

A **bootloader** is a small program that runs **immediately after a computer is powered on**. Its job is to **load the operating system kernel into memory and start it**.

Without a bootloader, the system cannot start an operating system.

---

## Boot Process (Simplified)

1. **Power On**
2. **BIOS or UEFI firmware** checks hardware.
3. **Bootloader is executed from the boot device** (SSD/HDD/USB).
4. Bootloader **loads the operating system kernel**.
5. Kernel starts the operating system.

---

## Example in Linux

A common Linux bootloader is **GRUB (Grand Unified Bootloader)**.

GRUB can:

* Choose between multiple operating systems
* Pass parameters to the kernel
* Start Linux

Example menu:

```
Ubuntu
Advanced options for Ubuntu
Windows Boot Manager
```

This is why dual-boot systems can select between **Linux and Windows**.

---

## Example in Windows

Windows uses **Windows Boot Manager**, which loads the Windows kernel during startup.

---




## Windows vs Linux

| Feature                   | Windows                                               | Linux                                                               |
| ------------------------- | ----------------------------------------------------- | ------------------------------------------------------------------- |
| **Developer**             | Developed by Microsoft                                | Developed by Linus Torvalds and the open-source community           |
| **Source Code**           | Closed source (proprietary)                           | Open source - General Public license                                                        |
| **Cost**                  | Requires a paid license (usually preinstalled on PCs) | Mostly free                                                         |
| **User Interface**        | Strong GUI focus; very beginner friendly              | GUI available, but strong command-line usage                        |
| **Customization**         | Limited customization                                 | Highly customizable                                                 |
| **Security**              | More targeted by malware and viruses                  | Generally more secure due to permission model                       |
| **Performance**           | Heavier; consumes more system resources               | Lightweight; runs well on older hardware                            |
| **Software Installation** | Install using `.exe` or `.msi` files                  | Usually installed through package managers (`apt`, `yum`, `pacman`) |
| **File System**           | NTFS, FAT32                                           | ext4, Btrfs, XFS                                                    |
| **Use Cases**             | Gaming, office work, general consumer use             | Servers, development, cybersecurity, cloud systems                  |

---

## Practical Example

**Installing software**

**Windows**

```
Download Chrome.exe → Double click → Install
```

**Linux (Ubuntu)**

```
sudo apt install chromium-browser
```

Linux emphasizes **terminal-based package management**, while Windows relies mostly on **graphical installers**.

---

## Where Each Is Commonly Used

**Windows**

* Personal computers
* Gaming
* Office environments

**Linux**

* Servers and cloud infrastructure
* Programming and development
* Cybersecurity and DevOps

Large platforms like Google, Amazon, and Meta Platforms heavily rely on Linux servers.

---

# Linux File System

The **Linux file system** is the hierarchical structure used by Linux to **organize, store, and manage files and directories** on a storage device. Instead of multiple drive letters (like `C:` or `D:` in Windows), Linux organizes everything under a **single root directory `/`**.

All files, devices, programs, and directories exist within this unified directory tree.

---

## Key Characteristics

1. **Hierarchical structure**
   Files are arranged in a tree-like structure starting from the root `/`.

2. **Everything is treated as a file**
   Hardware devices, processes, and system information are accessed as files.

3. **Case sensitive**
   `file.txt` and `File.txt` are different.

4. **Permission-based security**
   Each file has permissions for **owner, group, and others**.

---

## Basic Structure

![Image](https://www.devopsschool.com/blog/linux-tutorials-linux-file-systems/)

## Important Linux Directories

### `/` (Root Directory)

* The **top-level directory** of the Linux filesystem.
* All other directories originate from here.

### `/home`

* Contains **personal directories for users**.

Example:

```
/home/harsh
/home/user1
```

---

### `/bin`

* Contains **essential command binaries** used by all users.

Examples:

```
ls
cp
mv
cat
```

---

### `/etc`

* Stores **system configuration files**.

Examples:

```
/etc/passwd
/etc/hosts
```

---

### `/usr`

* Contains **user programs and applications** installed on the system.

Examples:

```
/usr/bin
/usr/lib
```

---

### `/var`

* Stores **variable data** such as logs and caches.

Examples:

```
/var/log
/var/tmp
```

---

### `/tmp`

* Temporary files created by applications.
* Usually cleared when the system restarts.

---

### `/dev`

* Contains **device files** representing hardware.

Examples:

```
/dev/sda
/dev/usb
```

---

### `/boot`

* Contains **bootloader files and kernel required to start Linux**.

---

## Example Path

```
/home/harsh/projects/app.js
```

Meaning:

* `/` → root
* `home` → users directory
* `harsh` → user folder
* `projects` → project directory
* `app.js` → file

---

## Summary

The Linux file system:

* Uses a **single root directory `/`**
* Organizes files in a **tree hierarchy**
* Treats **everything as a file**
* Uses **permissions for security**
* Contains standard directories defined by the **Filesystem Hierarchy Standard (FHS)**.

---

# Linux Commands

## 1. `ls`

**Definition:**
Lists files and directories inside the current directory.

**Syntax**

```bash
ls
```

**Example**

```bash
ls
```

**Output Example**

```
file1.txt  notes.txt  folder1
```

**Useful Variants**

* `ls -a` → shows hidden files
* `ls -lh` → shows size in human-readable format

---

# 2. `cd`

**Definition:**
Changes the current directory.

**Syntax**

```bash
cd directory_name
```

**Examples**

```bash
cd Documents
```

Move to parent directory:

```bash
cd ..
```

Move to home directory:

```bash
cd ~
```

---

# 3. `mkdir`

**Definition:**
Creates a new directory.

**Syntax**

```bash
mkdir directory_name
```

**Example**

```bash
mkdir projects
```

Create multiple directories:

```bash
mkdir dir1 dir2 dir3
```

Create nested directories:

```bash
mkdir -p project/src/code
```

---

# 4. `ls -l`

**Definition:**
Lists files in **long format**, showing detailed information.

**Syntax**

```bash
ls -l
```

**Example Output**

```
-rw-r--r-- 1 user user  124 Mar 8  file1.txt
drwxr-xr-x 2 user user 4096 Mar 8  folder1
```

**Fields Meaning**

```
permissions  links owner group size date filename
```

---

# 5. `pwd`

**Definition:**
Prints the **current working directory**.

**Syntax**

```bash
pwd
```

**Example**

```bash
pwd
```

**Output**

```
/home/harsh/Documents
```

---

# 6. `touch`

**Definition:**
Creates an empty file or updates file timestamp.

**Syntax**

```bash
touch filename
```

**Example**

```bash
touch notes.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt
```

---

# 7. `clear`

**Definition:**
Clears the terminal screen.

**Syntax**

```bash
clear
```

**Example**

```bash
clear
```

Shortcut:

```
Ctrl + L
```

---

# 8. `rm`

**Definition:**
Deletes files.

**Syntax**

```bash
rm filename
```

**Example**

```bash
rm notes.txt
```

Delete multiple files:

```bash
rm file1.txt file2.txt
```

---

# 9. `rm -r`

**Definition:**
Deletes directories **recursively** (including files inside).

**Syntax**

```bash
rm -r directory
```

**Example**

```bash
rm -r projects
```

Force delete:

```bash
rm -rf projects
```

---

# 10. `rmdir`

**Definition:**
Removes **empty directories only**.

**Syntax**

```bash
rmdir directory
```

**Example**

```bash
rmdir testFolder
```

---

# 11. `cat`

**Definition:**
Displays file contents.

**Syntax**

```bash
cat filename
```

**Example**

```bash
cat notes.txt
```

Combine files:

```bash
cat file1.txt file2.txt
```

Create file with cat:

```bash
cat > file.txt
```

---

# 12. `echo`

**Definition:**
Displays text or writes text into files.

**Syntax**

```bash
echo "text"
```

**Example**

```bash
echo "Hello Linux"
```

Write text to file:

```bash
echo "Hello" > file.txt
```

Append text:

```bash
echo "World" >> file.txt
```

---

# 13. `head`

**Definition:**
Shows the **first 10 lines** of a file.

**Syntax**

```bash
head filename
```

**Example**

```bash
head data.txt
```

Show first 5 lines:

```bash
head -n 5 data.txt
```

---

# 14. `tail`

**Definition:**
Shows the **last 10 lines** of a file.

**Syntax**

```bash
tail filename
```

**Example**

```bash
tail log.txt
```

Show last 5 lines:

```bash
tail -n 5 log.txt
```

Live log monitoring:

```bash
tail -f log.txt
```

---

# 15. `zcat`

**Definition:**
Displays contents of **compressed (.gz) files** without extracting them.

**Syntax**

```bash
zcat filename.gz
```

**Example**

```bash
zcat logs.gz
```

---

# 16. `less`

**Definition:**
Views large files **page by page** with scrolling.

**Syntax**

```bash
less filename
```

**Example**

```bash
less data.txt
```

Navigation

```
Space → next page
b → previous page
q → quit
```

---

# 17. `more`

**Definition:**
Displays file content **page by page** (older alternative to `less`).

**Syntax**

```bash
more filename
```

**Example**

```bash
more notes.txt
```

Difference:

* `less` allows backward scrolling
* `more` does not easily allow it

---

# 18. `cp`

**Definition:**
Copies files or directories.

**Syntax**

```bash
cp source destination
```

**Example**

```bash
cp file1.txt file2.txt
```

Copy file to folder:

```bash
cp file.txt Documents/
```

Copy directory:

```bash
cp -r folder1 folder2
```

---

# 19. `mv`

**Definition:**
Moves or renames files.

**Syntax**

```bash
mv source destination
```

**Examples**

Rename file:

```bash
mv old.txt new.txt
```

Move file to directory:

```bash
mv file.txt Documents/
```

---

# 20. `inode`

**Definition:**
An **inode (Index Node)** is a data structure used by Linux filesystems to store metadata about a file.

It stores:

* file size
* file owner
* permissions
* timestamps
* disk block location

It **does NOT store the file name**.

**Example**

Check inode number:

```bash
ls -i
```

Output:

```
123456 file1.txt
123457 notes.txt
```

Each file has a unique inode number.

---

# Important Concept (Related to Inodes)

### Hard Link

Two filenames pointing to the **same inode**.

```bash
ln file1.txt hardlink.txt
```

### Soft Link (Symbolic Link)

Pointer to another file path.

```bash
ln -s file1.txt softlink.txt
```

---


