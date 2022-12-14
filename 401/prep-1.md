## Practice in Terminal 

1. **The Command Line**:
- Command line or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text. 
- Within a terminal, you have a shell. This is part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is **bash** which stands for Bourne again shell. 
- To view which shell you are using, you may use a command called **echo**: **echo $SHELL**. 

2. **Basic Navigation**:
- **pwd** stands for Print Working Directory. The command does just that. 
- Next we have to know what is there. The command for this task is **ls**, short for list. 
- **ls[options][location]**. The square brackets mean that those items are optional. 
- First character will indicate if it's a normal file (-) or a directory (d).
- There are two types of paths, **absolute** and **relative**. Whenever we refer to a file or directory, we are using one of those paths. 
- At the very top of the structure is what's called the **root** directory. It is denoted by a single slash (/).
- Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash (/).
- Relative paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash (/).
- In order to move around the system, we use a command called **cd** which stands for change directory. **cd [location]**.

3. **More About Files**:
- Everything is a file under the hood with Linux. 
- Linux is an extensionless system. It does not have characters at the end of a file which denotes what type of file it is. ex. file.exe, file.txt.
- There is command called **file** we can use that helps us find this out. **file [path]**.
- Linux is case sensitive. 
- Spaces in file and directory names are perfectly valid but we need to be a little careful with them. 
- Single or double quotes can be used and anything inside the quotes is considered a single item. 
- Escape characters can be used to escape (or nulify) the special meaning of a character by using a backslash `(\)`.
- If a file name starts with an a, then it is a hidden file. **ls -a** shows all hidden files and directories. 

4. **Manual Pages**:
- Set of pages that explain every command available on your system including what they do, the specifics of how to run them, and what command line arguments they accept. 
- **`man <command to look up>`**.
- It is possible to search a keyword on the Manual pages. **`man -k <search item>`**.
- Within the Manual page, you can perform a search for 'term'. **`/<term>`**.
- After performing a search within a Manual page, select the next found item by entering **n**.

5. **File Manipulation**:
- To make a directory, you enter **`mkdir [options] <Directory>`** on the command line.
- To remove a directoy, you enter **`rmdir [options] <Directory>`** on the command line. 
- To create a blank file, you enter **`touch [options] <filename>`**.
- To copy a file or directory, you enter **`cp [options] <source> <destination>`**. 
- To move a file or directory, you enter **`mv [options] <source> <destination>`**.
- To remove or delete a file, you enter **`rm [options] <file>`**.
- The Linux command line does not have an undo feature. 

[Back to main page](./README.md)
