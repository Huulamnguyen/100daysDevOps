## 100 Days of DevOps

<img src="assets/images/devops-loop.svg">

### Description:

The challenge involves committing to learning and implementing DevOps principles for 100 consecutive days and sharing my progress with the DevOps community on GitHub, Medium, and my personal blog on my portfolio

### Goals:

The goal of the challenge is to help me enhance their skills and knowledge in DevOps practices, gain hands-on experience with relevant tools, and build a strong network of peers in the DevOps community. 

Through daily commits and sharing progress with others, I can hold myself accountable and track my progress throughout the challenge.

The 100 Days of DevOps challenge is an excellent opportunity for developers and IT professionals to advance their careers and stay up-to-date with the latest industry trends. 

By participating in the challenge, individuals can improve their understanding of DevOps principles, enhance their problem-solving skills, and build a portfolio of DevOps projects that they can showcase to potential employers.

### Sources:

A big thanks to techworld with Nana that delivers a greate content to achive my Devops Journey.
Check it out at [Techworld with Nana][def]

[def]: https://techworld-with-nana.teachable.com/courses

### Table of Contents
2. [Operating Systems & Linux Basics](#operating-systems-&-linux-basics)
    1. [Introduction to Operating Systems](#introduction-to-operating-systems)
    2. [Introduction to Virtualization & Virtual Machines](#introduction-to-virtualization-&-virtual-machine)
    3. [Setup a Linux Virtual Machine](#setup-virtual-machine)
    4. [Linux File System](#linux-file-system)
    5. [Introduction to Command Line Interface (CLI - Part 1)](#introduction-to-command-line-interface-part-1)
    6. [Basic Linux Commands (CLI - Part 2)](#basic-linux-commands-cli-part-2)
    7. [Package Manager - Installing Software on Linux](#package-manager-install-software-on-linux)
    8. [Working with Vim Editor](#working-with-vim-editor)

## Contents

### 2. Operating Systems & Linux Basics <a name="operating-systems-&-linux-basics"></a>

#### 1. Introduction to Operating Systems <a name="introduction-to-operating-systems"></a>

**What is operating system?**
    
Operating System (OS) is a software managing: 
- computer hardware,
- software resources
- and provides common services for computer programs

OS as abstraction layer between applications and hardware. Which means that instead of applications (like browser) interacting with the computer hardware directly, they can use the OS as abstraction layer between the two

**Tasks of an Operating System**
1. Resource Allocation and Management
    - Process Management (CPU)
    - Memory Management (RAM): Allocating working memory (RAM = Rapid Access Memory) to applications
    - Storage Management (Hard Drive): Persisting data long-term, like files, browser configurations, games, pictures, videos etc

2. File Management
    - Files are stored in structured way A file system is organized into directories
    - On Unix system: tree file system
    - On Windows OS: multiple root folders

3. Device Management
    - Manages device communication via their respective drivers
    - Monitor, keyboards, mouse, printers, etc.

4. Other important tasks
    - Security:
        - Managing Users and Permissions
        - Each user has its own space and permissions
    - Networking:
        - Ports and IP addresses
        - Transmitting outgoing data from all application ports onto the network, and forwarding arriving network packets to processes

**Operating System Components**
1. Kernel
    - Heart of every OS
    - The core program that provides basic services for all other parts of the OS
    - Consists of device drivers, dispatcher, scheduler, file system etc.
    - Controls all hardware resources via device drivers
    - Kernel starts the process for app, Allocates resources to app, Cleans up the resources when app shuts down
2. Application Layer:

On the top is kernel is the application layer. For instance:

- For example different Linux distributions: Ubuntu, Mint, CentOS, Debian. Different application layers, but based on same Linux kernel
- Android is also based on **Linux kernel**
- MacOS and iOS is based on a different Kernel called **Darwin**

3. How to interact with Kernel
- Graphical User Interface (GUI)
- Command-Line Interface (CLI)

**3 Main Operating Systems**
- Linux, Windows, Mac OS

**Client OS vs Server OS**
CLient OS:
    - For personal computers with GUI and Input/Output (I/O) devices

Server OS:
    - Linux and Windows have server distributions
    - But Linux most widely used
    - More light-weight and performant
    - No GUI or other user applications

**Why Linux is a must for Devops Engineer**
- Linux is mostly used OS for servers!
- Known Linux is a must for DeVops Engineer

#### 2. Introduction to Virtualization & Virtual Machines <a name="introduction-to-virtualization-&-virtual-machine"></a>

**What is a Virtual Machine?**
- **Virtual Machine (VM)** is a virtual computer running on top of another host computer
- **How it works**: Virtualization:
    - Virtualization is the process of creating a software-based, or "virtual" version of a computer, with dedicated amounts of CPU, memory, and storage that are "borrowed" from a physical host computer.
    - Makes it possible that any OS can run on top of any other physical host machine
    - The VM is partitioned from the rest of the system, meaning it's completely isolated and can't interfere with the host computer's primary OS
- **Hypervisor**: 
    - The **essential component in the virtualization stack** is a piece of software called a **hypervisor**
    - One of the most popular hypervisor is open-source **Oracle VM VirtualBox**
- **Host OS vs Guest OS**
    - **Host OS**: runs directly on the hardware
    - **Guest OS**: runs on the virtual machine
- **Hypervisor Types**:
    - Type 1 - Native or Bare Metal:
        - That run directly on the host's hardware to control the hardware, and to monitor the guest OS. The guest OS runs on a separate level above the hypervisor.
        - Examples of this classic implementation of VM architecture are Oracle VM, Microsoft Hyper-V, VMware ESXi.
        - Use Cases:
            - Efficient usage of hardware resources (e.g. cloud provider):
                - Use all the resources of a performant big server 
                - Users can choose any resource combinations
    - Type 2 -  Hosted
        - Designed to run within a traditional OS
        - A hosted hypervisor adds a distinct software layer on top of the host OS, and the guest OS becomes a third software level above the hardware
        - Examples: Oracle VM VirtualBox, VMware Server, Microsoft Virtual PC, KVM, QEMU and Parallels.
        - Use Cases:
            - Learn and experiment
            - Test your app on different OS
            - Backing up your existing OS

- Review Type 1 and Type 2 of Hypervisor on the image below:

<img src="assets/images/type1-type2-hypervisor.webp" alt="Review Type 1 and Type 2 of Hypervisor on the image below">

**Benefits of a Virtual Machine, Why companies adopt Virtualization**
- Main benefit: Instead of OS being tightly coupled to the hardware, Virtualization gives an abstraction layer, with the following benefits:
    - Security: Secure very easily
    - Agility and speed: Spinning up a VM is easy and quick, compared to setting up an entire new server Cost savings: Efficient usage of hardware resources
    - Portable: OS as a portable file (VMI - Virtual Machine Image)
- VMI:
    - Includes OS and all applications on it 
    - You can have backups of your entire OS

#### 3. Setup a Linux Virtual Machine <a name="setup-virtual-machine"></a>
- You can just work in terminal on the Mac
- Or, create a Ubuntu VM on Digital Ocean

#### 4. Linux File System <a name="linux-file-system"></a>
- Plug in a USB => `/media`
- Change configs => `/etc`
- Install app => `/bin`, `/lib`, ...

#### 5. Introduction to Command Line Interface (CLI - Part 1) <a name="introduction-to-command-line-interface-part-1"></a>
GUI and CLI acre two ways to interact with operating system. 
**GUI vs CLI**
- GUI = A graphical user interface, where we have graphical elements that you can interact with, like buttons
- CLI = Command Line Interface, where users type in commands and see the results printed on the screen
    - Terminal = the GUI window that you see on the screen. It takes commands and shows output
    - **On servers you only have the CLI, no GUI**
**Why CLI over GUI?**
- Work more efficient 
- Easier for bulk operations 
- CLI is more powerful

#### 6. Basic Linux Commands (CLI - Part 2) <a name="basic-linux-commands-cli-part-2></a>
General Operations:
    
    - clear = Clears the terminal

Directory Operatings:
    
    - pwd = Show current directory. Example Output: /home/nana
    - ls = List folders and files. Example Output: Desktop  Downloads  Pictures  Documents
    - cd [dirname] = Change directory to [dir]
    - mkdir [dirname] = Make directory [dirname]
    - cd .. = Go up a directory

File Operations:
    
    - touch [filename] = Create [filename]
    - rm [filename] = Delete [filename]
    - rm -r [dirname] = Delete a non-empty directory and all the files in it
    - rm -d [dirname] or rmdir [dirname] = Delete an empty directory

Navigating in the File System:

    - cd usr/local/bin = Navigate multiple dirs (relative path - relative to current dir). Move to bin directory
    - cd ../.. = Move up 2 hierarchies, so go to 'usr' directory
    - cd /usr = Alternative to go to 'usr' directly (absolute path)
    - cd [absolute path] = Move to any location by providing the full path
    - cd /home/nana = Go to my home directory (absolute path)
    - cd ~ = Shortcut alternative to go to home directory
    - ls /etc/network = List folders and files of 'network' directory

More File and Directory Operations

    - mv [filename] [new_filename] = Rename the file to a new file name
    - cp -r [dirname] [new_dirname] = Copy dirname to new_dirname recursively meaning including the files
    - cp [filename] [new_filename] = Copy filename to new_filename

Some more useful commands

    - ls -R [dirname] = Show dirs and files but also sub dirs and files
    - history = Gives a list of all past commands typed in the current terminal session
    - history 20 = Show list of last 20 commands
    - CTRL + r = Search history
    - CTRL + c = Stop current command
    - CTRL + SHIFT + v = Paste copied text into terminal
    - ls -a = See hidden files too
    - cat [filename] = Display the file content
    - cat .bash_history = Example 1: Display the file content
    - cat Documents/java-app/Readme.md = Example 2: Display the file content

Display OS Information

    - uname -a = Show system and kernel
    - cat /etc/os-release =  Show OS information
    - lscpu = Display hardware information, e.g. how many CPU you have etc.
    - lsmem = Display memory information

Execute commands as superuser

    - sudo [some command] = Allows regular users to run programs with the security privileges of the superuser or root
    - su - admin = Switch from nana user to admin

#### 7. Package Manager - Installing Software on Linux <a name="package-manager-install-software-on-linux"></a>
**How to install software**
- On Windows
    - On Windows you have download installer
    - Wizards that guide you through the installation

- On Linux:
    - On Linux you will install **applications mostly with package manager tools** on CLI

**Introduction to Package Manager**
- Tasks of a Package Manager:
    - Downloads, installs or updates existing software from a repository
    - Ensures the integrity and authenticity of the package
    - Manages and resolves all required dependencies
    - Knows where to put all the files in the Linux file system
    - Easy upgrading of the software.

**Package Manager - pre-installed**
- Package Manager is already included in every Linux distribution
- On Ubuntu, you have APT package manager available. **APT = Advanced Package Tool**
- Package Manager like apt has commands you can use to install, uninstall or upgrade software

**Package Repository**
- A repository is a storage location, where all the software packages are hosted
- Contains thousands of programs
- Package Manager fetches the packages from these repositories
- `sudo apt update`:
    - Pulls the latest changes from the APT repositories
    - The APT package index is basically a database
    - Holding records of available packages from the repositories

**Alternative Package Manager**
- A very similar package manager is APT-GET, which you will often come across
- APT:
    - user friendly
    - Fewer
    - Recommended by Linux distributions
- APT-GET:
    - On Ubuntu, APT-GET also out of the box available
    - Different set of commands
    - You can achieve the same user friendly output, if you use additional command options
    - E.g. "apt search" not available

**Alternative ways to install software**
- Ubuntu Software Center
    - Like an app store
    - A utility for installing, purchasing, removing software in Ubuntu
    - Has a graphical UI, so no need for using the CLI
- Snap Package Manager
    - Snap is a software packaging and deployment system
    - Snap = A snap is a bundle of an app and its dependencies 
    - Snap Store = Provides a place to upload snaps, and for users to browse and install the software
    - Snapcraft = Is the command and framework used to build and publish snaps

**Linux Distribution**
- Debian Based: APT OR APT-GET (package manager)
    - Ubuntu
    - Debian
    - Mint

- Read Hat Based: YUM (package manager)
    - RHEL
    - CentOS
    - Fedora

#### 8. Working with Vim Editor <a name="working-with-vim-editor"></a>

**Introduction to Vi and Vim**
- Vi and Vim are built-in text editors in Linux

**Use cases for using text editor in CLI**
- Small modifications can be faster, especially when you are currently working in the CLI
- Faster to create and edit at the same time
- Supports multiple formats
- When working on a server

**Working with Vim**
- Vim has two modes:
    - Insert mode
    - Command mode:
        - This is the default mode
        - You can't edit the text
        - Whatever you type is interpreted as a command 
       - Navigate, Search, Delete, Undo etc.

- `vim {filename}` => open the file name, if it doesn't exist, create a new one.
- **Editing**:
    - `i`: switch to insert mode
    - `dd`: delete a line
    - `d10`: delete 10 lines
    - `u`: undo
    - `0`: jump to the start of line
    - `$`: jump to the end of line
    - `A`: jump to the end of line and switch to insert mode
    - `12G`: go to line 12

- **Saving and quitting**:
    - `:wq`: write file to disk and quit vim
    - `:q!`: quit vim without saving changes

- **Searching and Replacing**
    - `/pattern`: will search the pattern
    - `n`: jump to the match
    - `N`: jump to the previous match
    - `:%s/mystring/my-new-string`: will replace all occurrences of "my-stirng" with "my-new-string"

- Pressing `Escape`, switches you back to **command mode**