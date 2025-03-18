# Linux For DevOps
 
 ## Topics 
 ## 1: Introduction of Linux

 ### Definition of Linux or What is Linux ?
  Linux is an open-source operating system that is widely used for its stability, security, and flexibility. It was originally created by Linus Torvalds in 1991 and has since grown into a major force in the world of computing.
  Here are some key points about Linux:
  **Open-source:** The source code is freely available for anyone to view, modify, and distribute.
  **Versatile:** It can run on a wide range of devices, from servers and desktops to smartphones and embedded systems.
  **Secure:** Known for its strong security features, making it a popular choice for servers and other critical systems.
  **Community-driven:** Developed and maintained by a global community of developers and users.
  Linux distributions, such as Ubuntu, Fedora, and Debian, offer different features and user experiences, catering to various needs and preferences.

 ### What is the use of linux in DevOps ?
  Linux plays a crucial role in DevOps for several reasons:

1. **Server Management**: Many servers run on Linux due to its stability and performance. DevOps engineers use Linux to manage these servers, ensuring they are configured correctly and running smoothly.
2. **Automation**: Linux supports powerful scripting languages like Bash, which are used to automate repetitive tasks, such as deployments, backups, and monitoring.
3. **Containerization**: Tools like Docker and Kubernetes, which are essential for containerization and orchestration in DevOps, are built to run on Linux.
4. **Configuration Management**: Tools like Ansible, Puppet, and Chef are often used in DevOps for configuration management and are designed to work seamlessly with Linux.
5. **Security**: Linux's robust security features make it ideal for maintaining secure environments, which is critical in DevOps.
6. **Continuous Integration/Continuous Deployment (CI/CD)**: Linux environments are commonly used for setting up CI/CD pipelines, enabling automated testing and deployment of applications.

### What are popular DevOps tools for Linux?
There are many popular DevOps tools for Linux, each serving different aspects of the DevOps lifecycle. Here are some of the most widely used ones:

1. **Git**: A version control system that helps track changes in source code during software development.
2. **Jenkins**: An automation server used for continuous integration and continuous delivery (CI/CD).
3. **Docker**: A platform for developing, shipping, and running applications in containers.
4. **Kubernetes**: An orchestration tool for managing containerized applications across a cluster of nodes.
5. **Ansible**: A configuration management tool that automates software provisioning, configuration management, and application deployment.
6. **Terraform**: An infrastructure as code (IaC) tool that allows you to define and provision data center infrastructure using a high-level configuration language.
7. **Prometheus**: A monitoring and alerting toolkit designed for reliability and scalability.
8. **Grafana**: An open-source platform for monitoring and observability, often used in conjunction with Prometheus.
9. **Nagios**: A monitoring system that enables organizations to identify and resolve IT infrastructure problems.
10. **ELK Stack (Elasticsearch, Logstash, Kibana)**: A set of tools for searching, analyzing, and visualizing log data in real-time.

These tools help streamline various DevOps processes, from code management and integration to deployment, monitoring, and infrastructure management.

### Basics of Linux commands:
1. **Linux File System**
2. **Basic Linux Commands**
3. **Permissions and Ownership**
4. **Users, Groups, and Security**
5. **Package Management**
6. **Text Processing and Editing**
7. **Processes and Job Management**
8. **Networking basics**
9. **Disk and Storage Management**
10. **System Monitoring and Performance**
11. **Shell Scripting**
12. **Version Controlling with Git**
13. **Backup and Recovery**
14. **System Boot and Initialization**
15. **Services Management and Systemd**
16. **SELinux commands**
17. **Kernel Management**

## 1: Linux File System
Here's a brief overview of the Linux file system, some useful commands, and examples:

The Linux file system is hierarchical, starting from the root directory (`/`). Here are some key directories:

- **`/`**: Root directory, the top-level directory.
- **`/bin`**: Contains essential binary executables.
- **`/etc`**: Configuration files for the system.
- **`/home`**: User home directories.
- **`/var`**: Variable files, such as logs.
- **`/usr`**: User programs and utilities.
- **`/tmp`**: Temporary files.

### Useful Commands
Sure! Here are some examples of the Linux file system structure and its directories:

### Examples of Linux File System Directories

1. **Root Directory (`/`)**
   - The top-level directory in the Linux file system.
   - Example: `/`

2. **Binary Directory (`/bin`)**
   - Contains essential command binaries.
   - Example: `/bin/ls` (the `ls` command)

3. **Configuration Directory (`/etc`)**
   - Stores system configuration files.
   - Example: `/etc/passwd` (user account information)

4. **Home Directory (`/home`)**
   - Contains personal directories for users.
   - Example: `/home/username` (user's home directory)

5. **Variable Directory (`/var`)**
   - Holds variable data files, such as logs.
   - Example: `/var/log/syslog` (system log file)

6. **User Programs Directory (`/usr`)**
   - Contains user programs and utilities.
   - Example: `/usr/bin/python` (Python interpreter)

7. **Temporary Directory (`/tmp`)**
   - Used for temporary files.
   - Example: `/tmp/tempfile.txt` (temporary file)

8. **Device Directory (`/dev`)**
   - Contains device files.
   - Example: `/dev/sda` (first hard disk)

9. **Library Directory (`/lib`)**
   - Stores essential shared libraries.
   - Example: `/lib/libc.so.6` (C standard library)

10. **Boot Directory (`/boot`)**
    - Contains boot loader files.
    - Example: `/boot/vmlinuz` (Linux kernel image)

### Example File Paths

- **System Configuration File**: `/etc/hostname`
- **User's Document**: `/home/username/Documents/report.txt`
- **Log File**: `/var/log/auth.log`
- **Executable File**: `/usr/bin/grep`
- **Temporary File**: `/tmp/session_data`

These examples illustrate the hierarchical structure and organization of the Linux file system, making it easier to manage and locate files.


## Basic Useful Commands:

Sure! Here are some commonly used Linux commands along with brief explanations and examples:

### 1. `ls`
**Lists files and directories.**
```bash
ls -l
```
*Example*: Lists files in long format, showing details like permissions, owner, size, and modification date.

### 2. `cd`
**Changes the current directory.**
```bash
cd /home/user
```
*Example*: Changes to the user's home directory.

### 3. `cp`
**Copies files and directories.**
```bash
cp file1.txt file2.txt
```
*Example*: Copies `file1.txt` to `file2.txt`.

### 4. `mv`
**Moves or renames files and directories.**
```bash
mv oldname.txt newname.txt
```
*Example*: Renames `oldname.txt` to `newname.txt`.

### 5. `rm`
**Removes files or directories.**
```bash
rm file.txt
```
*Example*: Deletes `file.txt`.

### 6. `mkdir`
**Creates a new directory.**
```bash
mkdir newdir
```
*Example*: Creates a directory named `newdir`.

### 7. `chmod`
**Changes file permissions.**
```bash
chmod 755 script.sh
```
*Example*: Sets read, write, and execute permissions for the owner, and read and execute permissions for others.

### 8. `ps`
**Displays current processes.**
```bash
ps aux
```
*Example*: Shows all running processes.

### 9. `grep`
**Searches for patterns in files.**
```bash
grep "search_term" file.txt
```
*Example*: Searches for "search_term" in `file.txt`.

### 10. `top`
**Displays system processes in real-time.**
```bash
top
```
*Example*: Shows real-time system processes and resource usage.

### 11. `find`
**Searches for files and directories.**
```bash
find /home/user -name "*.txt"
```
*Example*: Finds all `.txt` files in the user's home directory.

### 12. `tar`
**Archives files.**
```bash
tar -cvf archive.tar /path/to/directory
```
*Example*: Creates an archive named `archive.tar` from the specified directory.

### 13. `df`
**Displays disk space usage.**
```bash
df -h
```
*Example*: Shows disk space usage in a human-readable format.

### 14. `du`
**Displays directory space usage.**
```bash
du -sh /path/to/directory
```
*Example*: Shows the size of the specified directory in a human-readable format.

### 15. `nano` or `vim`
**Text editors for editing files.**
```bash
nano file.txt
```
*Example*: Opens `file.txt` in the Nano text editor.

These commands are fundamental for navigating and managing the Linux file system. They help perform a wide range of tasks, from file manipulation to system monitoring.

### Assignments / Practicals:
1. **Navigate to the FileSystem and list out the contents and files using above learnt commands.**
2. **Create a new directory called assignment-dir, navigate into it, and create an empty file named file-practice.txt, then add the content / information in that file.**
3. **Create a new directories called assignment1, assignment2. Create a file1.txt and Add content into it "This is text file", then copy this file to assignment2 directory. Then move the assignment2 directory to the assignment1 directory.**
4. **Check the usage of Disk Space and the individual directories under root(/).**


## Permissions and Ownership :
