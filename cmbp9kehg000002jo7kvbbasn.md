---
title: "Linux Basics Explained: From OS Concepts to Essential Commands"
seoTitle: "Linux Basics Explained: OS Concepts, Commands & Distributions"
seoDescription: "Master Linux fundamentals for beginners: OS architecture, essential commands, and popular distributions like Ubuntu & Kali. Start your sysadmin journey toda"
datePublished: Sun Jun 08 2025 18:30:00 GMT+0000 (Coordinated Universal Time)
cuid: cmbp9kehg000002jo7kvbbasn
slug: linux-basics-explained-from-os-concepts-to-essential-commands
canonical: https://devopslinuxcraft.hashnode.dev/
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/oqStl2L5oxI/upload/945b0f54ee90b849a001a67c04137049.jpeg
tags: linux, opensource, cli, devops, shell, beginners, terminal-commands, devops-tools, linux-for-beginners, linux-commands, operatingsystems, fundamentals-of-linux, sysadmin-basics, kernel-and-shell

---

Whether you're a DevOps enthusiast, a developer, or a curious beginner, understanding Linux is crucial in today’s tech world. In this post, we’ll walk through the foundational concepts of Linux, its history, distributions, and key commands every user should know.

---

## 🐧 What is Linux?

Linux is a **free and open-source operating system** (OS) known for its high security and multitasking capabilities. It's widely used in:

* Servers
    
* Embedded systems
    
* Supercomputers
    
* Smartphones
    
* IoT devices
    

---

## 💡 What is an Operating System?

An **Operating System** acts as an interface between hardware and the user. Every application — like web browsers, notepads, or games — needs an OS to run.

---

## 🧰 Types of OS (Operating Systems)

* Single-user OS
    
* Multi-user OS
    
* Distributed OS
    
* Real-time OS
    
* Mobile OS
    

---

## 🔀 Linux Distributions

Different communities and companies have customized Linux and released them as **distributions** (distros):

* Ubuntu
    
* RedHat
    
* Debian
    
* CentOS
    
* Fedora
    
* OpenSUSE
    
* Kali Linux
    
* Rocky Linux
    
* Amazon Linux
    

Each has its own package manager and default settings but shares the same Linux kernel.

---

## 🧠 History of Linux

In **1991**, a Finnish student named **Linus Torvalds** created the Linux Kernel as a personal project. Initially named **"Freax"**, it was later renamed to **Linux**.

Today, Linux powers everything from smartphones and web servers to washing machines and cars.

---

## 🧩 Kernel & Shell

### 🔸 Kernel

The **kernel** is the heart of the OS. It manages hardware, memory, and process control.

### 🔸 Shell

The **shell** is the interface that interprets user commands. There are two types:

* **CLI (Command Line Interface)** — terminal-based
    
* **GUI (Graphical User Interface)** — mouse and window-based
    

---

## 🖥️ Terminal and User Privileges

By default, users operate as a standard user like `ec2-user`. To perform admin actions, switch to **root** user using:

```bash
sudo -i  # Switch to root user
exit     # Exit back to regular user
```

---

## **🔧 Essential Linux Commands**

🔹 **System Commands**

```bash
uname       # Show OS type
uname -r    # Show kernel version
uname -a    # Show all OS info
clear       # Clear terminal
uptime      # Show system uptime
hostname    # Display system DNS name
hostnamectl # Change system hostname
```

**🔹 IP and Network**

```bash
ip addr         # Show IP addresses
ip route        # Show routing table
ifconfig        # Alternative for ip addr
```

**🔹 Time and Date**

```bash
date                       # Show current date and time
timedatectl                # View timezone info
timedatectl set-timezone Asia/Kolkata  # Set timezone
```

**🗓️ Formatted** `date` **Command Options in Linux**

```bash
| Command             | Description                                            |
|---------------------|--------------------------------------------------------|
| `date`              | Shows system date and timestamp                        |
| `date +"%d"`        | Prints day of the month (01–31)                        |
| `date +"%m"`        | Prints the month of the year (01–12)                   |
| `date +"%y"`        | Prints the last two digits of the year                 |
| `date +"%H"`        | Prints the hour (00–23)                                |
| `date +"%M"`        | Prints the minute of the hour (00–59)                  |
| `date +"%S"`        | Prints the seconds count in the minute (00–60)         |
| `date +"%D"`        | Prints the date in MM/DD/YY format                     |
| `date +"%F"`        | Prints the full date as YYYY-MM-DD                     |
| `date +"%A"`        | Prints the day of the week (e.g., Monday)              |
| `date +"%B"`        | Prints the full month name (e.g., January–December)    |
| `who`               | Prints info about the default user in the system       |
```

**🔹 User Info**

```bash
who      # See logged-in users
whoami   # See current user
```

### 🔹 Processes

```bash
ps         # View running processes
kill -9 PID  # Kill a process by ID
```

---

### **🔍 Hardware Commands**

```bash
lscpu       # CPU info
lsblk -a    # Block devices info
free -m     # Memory in MB
df -h       # Disk usage
```

| **Command** | **Description** | **Example Usage** |
| --- | --- | --- |
| `lscpu` | Displays detailed CPU architecture information (cores, threads, model). | \`lscpu |
| `lsblk -a` | Lists all block devices (disks, partitions) with tree-like hierarchy. | \`lsblk -a |
| `free` | Shows RAM usage in **kilobytes (KB)** (total, used, free, cache). | \`free |
| `free -m` | Displays RAM usage in **megabytes (MB)** (easier to read). | `free -m` |
| `df -h` | Reports disk space usage in **human-readable** format (GB/MB). | \`df -h |

**You can also use** `date +` **with various options to format output:**

```bash
date +"%d-%m-%Y"  # Custom date format
date +"%A"        # Day of the week
```

---

### **🐧 Linux File and Folder Commands**

**📄 1. Creating Files**

Use the `touch` command to create one or multiple files:

```bash
touch filename
touch aws azure gcp
touch linux{1..5}  # Creates linux1, linux2, ..., linux5
```

**❌ 2. Deleting Files**

Remove files using `rm`. Be cautious — deleted files don't go to a recycle bin!

```bash
rm filename               # Prompts before deleting
rm -f filename            # Force delete (no prompt)
rm -f aws azure gcp       # Delete multiple files
rm -f linux{1..5}         # Delete linux1 to linux5
rm -f *.txt               # Delete all .txt files
rm -f a*                  # Delete files starting with 'a'
rm -f *                   # Delete all files in current directory
```

**📁 3. Creating Folders**

To create directories (folders), use `mkdir`:

```bash
mkdir foldername
mkdir git maven jenkins
mkdir docker{1..5}        # docker1 to docker5
```

Create nested directories with the `-p` option:

```bash
mkdir -p aws/azure/gcp/ccit
```

**🗑️ 4. Deleting Folders**

Use `rmdir` to remove empty folders:

```bash
rmdir foldername
rmdir git maven jenkins
rmdir docker{1..5}
rmdir *                   # Remove all empty folders
```

To remove folders and their contents, use:

```bash
rm -rf foldername
rm -rf *                  # ⚠️ DANGEROUS: Deletes all files & folders
```

**📂 5. Changing Directories**

Navigate through your file system:

```bash
cd foldername             # Enter a folder
cd                        # Go to home directory
cd -                      # Go to previous directory
cd ../                    # Go one directory up
cd ../../                 # Go two directories up
```

**🗂️ 6. Listing Files and Folders**

To see what’s inside your directory:

```bash
ls                        # Lists names only
ll                        # Lists detailed info (permissions, size, etc.)
```

Check contents of a specific folder:

```bash
ll foldername
```

**📋 7. Copying Files**

The `cp` command is used to copy files:

```bash
cp file1 file2            # Overwrites file2 with contents of file1
```

To **append** content instead of overwriting, use:

```bash
cat file1 >> file2        # Appends content of file1 to file2
```

**🔁 8. Moving or Renaming Files**

The `mv` command can move or rename:

```bash
mv file1 file2            # Renames file1 to file2 or moves it
```

**🧠 Pro Tip: Use Brace Expansion to Save Time**

Linux supports brace expansion for patterns:

```bash
mkdir project{1..3}       # Creates project1, project2, project3
touch test{A..C}.txt      # Creates testA.txt, testB.txt, testC.txt
```

**🔚 Final Thought for** **Linux File and Folder Commands**

The Linux command line can be intimidating at first, but once you get comfortable with file and folder operations, everything else becomes easier. Try these commands in your terminal, and you'll quickly gain confidence in managing your system efficiently.

> 💬 Do you use any Linux shortcuts that save you time? Share them in the comments below!

---

## 🏁 Conclusion

Linux is more than just an OS — it's a **powerful ecosystem** that empowers developers, system admins, and organizations worldwide. Whether you're managing a server or developing an app, mastering the **Linux basics and commands** is your first step to unlocking its full potential.

**⭐ *Follow me for more Linux & DevOps content!*  
🔁 *Leave a comment if you found this helpful or want more command deep-dives!***

```yaml

---

Would you like me to:
- Suggest a **cover image** for the blog?
- Create a **second part** on advanced Linux topics?
- Generate a **logo** to match your blog theme?

Let me know!
```