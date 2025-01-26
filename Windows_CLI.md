# Windows CLI Commands

This document lists common Windows command-line commands along with their descriptions.

## Command & Descriptions

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

## Notes
- These commands are essential for navigating and managing files and directories in the Windows Command Prompt.
- Use `command /?` to learn more about any specific command.

