# Windows CLI Commands

This document lists common Windows command-line commands along with their descriptions.

---

## Command Descriptions

### File and Directory Management

1. **`dir`**  
   Displays a list of files and directories in the current directory.

2. **`dir /a`**  
   Displays all files and directories, including hidden and system files.

3. **`cd ..`**  
   Changes the current directory to the parent directory.

4. **`cd \temp`**  
   Changes the current directory to the `\temp` directory on the current drive.

5. **`mkdir`**  
   Creates a new directory. The directory name must be specified after the command (e.g., `mkdir NewFolder`).

6. **`dir /?`**  
   Displays inline help and usage options for the `dir` command.

7. **`cls`**  
   Clears the screen of all previously displayed text.

8. **`echo`**  
   Displays messages or turns the command echoing feature on or off.

9. **`echo This is just a regular file > foo.txt`**  
   Creates a file named `foo.txt` in the current directory and writes the text "This is just a regular file" into it.

10. **`type`**  
    Displays the content of a text file in the command prompt. For example, `type foo.txt` shows the content of `foo.txt`.

11. **`more /?`**  
    Displays inline help and usage options for the `more` command, which is used to view text files one screen at a time.

12. **`tree`**  
    Displays a hierarchical view of the directory structure of the current drive or path.

13. **`tree | more`**  
    Displays the hierarchical directory structure one screen at a time, allowing the user to scroll through the output.

14. **`tree c:\ | more`**  
    Displays the hierarchical directory structure of the `C:\` drive one screen at a time.

---

## Other Commands

### Process and Task Management

1. **`taskmgr`**  
   Opens the Windows Task Manager, allowing you to monitor and manage running processes, performance, and system resources.

2. **`tasklist`**  
   Displays a list of currently running processes on the system.

3. **`tasklist | more`**  
   Displays the list of running processes one screen at a time, useful for large outputs.

4. **`tasklist /svc | find "lsass.exe"`**  
   Lists the services associated with running processes and filters the output to show only those related to `lsass.exe`.

---

### Network Configuration and Monitoring

1. **`ipconfig`**  
   Displays basic network configuration details such as IP address, subnet mask, and default gateway.

2. **`ipconfig /all`**  
   Shows detailed network configuration information, including MAC addresses, DNS servers, and DHCP status.

3. **`ipconfig | more`**  
   Displays the output of `ipconfig` one screen at a time for easier reading.

4. **`ipconfig | displaydns | more`**  
   Displays the contents of the DNS Resolver Cache one screen at a time.

5. **`ipconfig | displaydns | find "Record Name"`**  
   Filters the DNS Resolver Cache output to display only entries containing "Record Name."

6. **`netstat -rn | more`**  
   Displays the system's routing table and network routes one screen at a time.

7. **`netstat -an`**  
   Displays all active network connections and their listening ports, along with their states.

8. **`netsh`**  
   Opens the Network Shell (Netsh), a command-line utility for managing network configurations and settings.

9. **`netsh advfirewall show allprofiles`**  
   Displays the current settings for all Windows Firewall profiles (Domain, Private, Public).

10. **`netsh` (with "set" switch)**  
    You can use the "set" switch to modify firewall states (On or Off) directly, and this command can be added to a desktop shortcut for quick toggling.

11. **`arp -a | more`**  
    Displays the Address Resolution Protocol (ARP) table, showing IP-to-MAC address mappings, one screen at a time.

12. **`ping [ip address]`**  
    Sends ICMP Echo Requests to the specified IP address to test connectivity and measure round-trip time.

13. **`tracert [ip or url]`**  
    Traces the route packets take to reach the specified IP address or URL, showing each hop along the way.

---

### Alternate Data Streams (ADS)

Alternate Data Streams are a feature of the NTFS file system that allows multiple data streams to be associated with a single file. These can be used to hide data within a file.

1. **`echo This is a hidden file in an Alternate Data Stream > foo.txt:hiddenstuff.txt`**  
   Creates an Alternate Data Stream named `hiddenstuff.txt` attached to `foo.txt` and writes the text "This is a hidden file in an Alternate Data Stream" into it.

2. **`dir /r`**  
   Lists files in the directory and shows any Alternate Data Streams associated with them.

3. **`more < foo.txt:hiddenstuff.txt`**  
   Displays the content of the `hiddenstuff.txt` Alternate Data Stream attached to `foo.txt`.

4. **`notepad foo.txt:hiddenstuff.txt`**  
   Opens the `hiddenstuff.txt` Alternate Data Stream attached to `foo.txt` in Notepad for editing.

5. **`dir /s /r | more`**  
   Recursively lists files in the directory and subdirectories, including any Alternate Data Streams, one screen at a time.

6. **`dir /s /r | findstr /e ":$DATA" | more`**  
   Searches for and displays files with Alternate Data Streams containing the `:$DATA` stream, one screen at a time.

---

## Notes

- These commands are essential for navigating, managing, and troubleshooting in the Windows Command Prompt.
- Use `command /?` to learn more about any specific command.
