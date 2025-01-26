# Linux CLI Command Reference

This document provides a list of essential Linux CLI commands, categorized for easy navigation. Each command includes a brief description.

---

## **User and System Management**

- **`sudo su`**  
  Switch to superuser (root).

- **`sudo apt list --upgradeable`**  
  List all packages with available updates.

- **`sudo apt update`**  
  Update the list of available packages.

- **`sudo apt upgrade`**  
  Upgrade installed packages.  
  - **Auto-confirm prompts**:  
    ```bash
    sudo apt -y upgrade
    ```

- **`ssh [username]@[ip address]`**  
  Connect to a remote server using SSH.

- **`ssh-keygen -if /etc/ssh/ssh_host_ecdsa_key.pub`**  
  Generate an SSH key from a public key file.

---

## **File and Directory Management**

- **`pwd`**  
  Print the current working directory.

- **`sudo apt install tree`**  
  Install the `tree` command.  
  **`tree`**  
  Display directory structure in a tree format.

- **`ls`**  
  List files and directories in the current directory.  
  - **Detailed with human-readable sizes**:  
    ```bash
    ls -alh
    ```

- **`cd [directory]`**  
  Change to a specific directory.  
  - **Parent directory**:  
    ```bash
    cd ..
    ```  
  - **Home directory**:  
    ```bash
    cd ~
    ```  
  *(Tip: Use the `Tab` key to auto-complete directory names.)*
  *(Tip: Press the Tab key twice quickly to see all possible directories or files you can navigate to from your current location.)*
  
---

## **Network Management**

- **`ip a`**  
  Display all network interfaces and their IP addresses.

- **`ip a | grep inet`**  
  Filter output to show only IPv4 and IPv6 addresses.

- **`ip neighbor`**  
  Show ARP cache (connected devices).

- **`ip -s link show [interface]`**  
  Display statistics for a specific network interface.

- **`watch -n 1 "ip -s link show [interface]"`**  
  Monitor interface statistics in real time.

- **`netstat -an | less`**  
  View active network connections.

- **`arp`**  
  Display ARP cache.  
  - **Detailed ARP table**:  
    ```bash
    arp -an
    ```

---

## **Process Management**

- **`ps`**  
  Display currently running processes.

- **`top`**  
  Interactive process viewer.  
  - **Add memory graph**: Press `m`.  
  - **Limit displayed processes**: Press `n`.

---

## **Disk and Storage Management**

- **`df`**  
  Display disk space usage for mounted filesystems.  
  - **Human-readable format**:  
    ```bash
    df -h
    ```

- **`find`**  
  Search for files and directories.  
  - **Search by name in the current directory**:  
    ```bash
    find . -name [search word]
    ```  
  - **Search system-wide**:  
    ```bash
    find / -name [search word]
    ```  
  - **Search by size**:  
    ```bash
    find / -type f -size +1G  # Files > 1GB
    find / -type f -size -1G  # Files < 1GB
    find / -type f -size 0    # Empty files
    ```

- **`less`**  
  View file content with pagination.  
  - **Keep output on one line per entry**:  
    ```bash
    less -S [filename]
    ```  
  - **Exit `less`**:  
    ```bash
    q
    ```

---

## **Logs and History**

- **`cat .bash_history`**  
  View the history of commands entered in the terminal.

- **`history`**  
  Display the command history.

- **`[command] --help`**  
  Display usage information for a command.

- **`man [command]`**  
  View detailed manual pages for a command.  
  - **Search within manual pages**:  
    ```bash
    /[search term]
    ```

---

## **System Monitoring and Security**

- **`iptables -L -nxv`**  
  Display all active firewall rules.

- **`w`**  
  Show users currently logged into the system.

- **`last -a`**  
  View login history.

- **`lastb | cut -f 1 -d ' ' | head`**  
  Show a summary of failed login attempts.

- **`lastb | cut -f 1 -d ' ' | sort | uniq -c | sort -rn | head`**  
  Display a sorted list of failed login attempts.

- **`clear`**  
  Clear the terminal screen.

---

## **Notes**

- Linux commands are case-sensitive. Ensure proper capitalization when entering commands.
- Use `man [command]` or `[command] --help` for detailed usage instructions.
