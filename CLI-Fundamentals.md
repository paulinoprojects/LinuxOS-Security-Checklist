This cheat sheet provides a basic overview of essential Linux command-line interface (CLI) commands for new cybersecurity and Linux administrators.

## 1. Navigation & File Management

* **`cd`**: Change directory.
    * `cd /`: Go to root directory.
    * `cd ..`: Go to the parent directory.
    * `cd ~`: Go to home directory.
    * `cd Documents`: Go to the "Documents" directory.
* **`ls`**: List files and directories. 
    * `ls -l`: List with detailed information (permissions, owner, size, etc.).
    * `ls -a`: List all files, including hidden files (starting with ".").
* **`pwd`**: Print working directory (show current location).
* **`mkdir`**: Create a new directory. 
    * `mkdir new_folder`: Create a directory named "new_folder".
* **`touch`**: Create an empty file. 
    * `touch new_file.txt`: Create a file named "new_file.txt".
* **`rm`**: Remove a file. 
    * `rm file.txt`: Remove the file "file.txt".
    * **WARNING:** Use with caution! `rm -rf` (recursive force) can delete entire directories.
* **`cp`**: Copy files or directories. 
    * `cp file1.txt file2.txt`: Copy "file1.txt" to "file2.txt".
* **`mv`**: Move or rename files or directories.
    * `mv file.txt new_location/`: Move "file.txt" to "new_location".
    * `mv old_name.txt new_name.txt`: Rename "old_name.txt" to "new_name.txt".

## 2. User & Group Management

* **`whoami`**: Show the currently logged-in user.
* **`su`**: Switch user. 
    * `su root`: Switch to the root user (requires root password).
* **`sudo`**: Execute a command with root privileges. 
    * `sudo apt update`: Update package lists with root privileges.
* **`useradd`**: Create a new user account.
* **`userdel`**: Delete a user account.
* **`passwd`**: Change the password for the current user.

## 3. System Information

* **`df -h`**: Display disk space usage.
* **`free -h`**: Display system memory usage.
* **`top`**: Display real-time system processes (use `q` to quit).
* **`uptime`**: Show system uptime and load average.
* **`uname -a`**: Display system information (kernel version, architecture, etc.).

## 4. Package Management (using apt)

* **`apt update`**: Update package lists.
* **`apt upgrade`**: Upgrade installed packages.
* **`apt install <package_name>`**: Install a new package (e.g., `apt install vim`).
* **`apt remove <package_name>`**: Remove a package.

## 5. Text Editing

* **`nano`**: Simple text editor (easy to use for beginners).
* **`vim`**: Powerful text editor (steeper learning curve).

## 6. Security-Related Commands

* **`iptables`**: Configure firewall rules (advanced).
* **`fail2ban`**: Detect and block brute-force attacks.
* **`chkrootkit`**: Check for rootkit infections.

## Important Notes

* **Practice regularly:** The best way to learn is by practicing these commands in a safe environment (e.g., a virtual machine).
* **Read the manual:** For detailed information and advanced options, use the `man` command (e.g., `man ls`).
* **Use `tab` for autocompletion:** This can save you time and reduce typos.
* **Start with simple commands:** Gradually increase complexity as you gain experience.

This cheat sheet provides a basic foundation. As you delve deeper into cybersecurity and Linux administration, you'll encounter many more commands and tools. Remember to prioritize security best practices and always double-check your commands before executing them, especially those that involve deletion or modification of system files.

**Disclaimer:** This cheat sheet is for informational purposes only and should not be considered a substitute for professional guidance. Always refer to official documentation and exercise caution when using any command-line tools.
This code creates a well-formatted Markdown file with headings, lists, and code blocks for easy 
