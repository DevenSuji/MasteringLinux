# <b><ins><i>Managing Files</i></ins></b>

As an administrator, you need to be able to perform common file management tasks. These tasks include the following:  
* Working with wildcards.
* Managing and working with directories.
* Working with absolute and relative pathnames.
* Listing files and directories.
* Copying files and directories.
* Moving files and directories.
* Deleting files and directories.

### <b><ins><i>Working with Wildcards</i></ins></b>

When working with files, using wildcards can make your work a lot easier. A wildcard is a shell feature that helps you refer to multiple files in an easy way.
| Wildcard | Use |   
|:-------|:----------|
| * | Refers to an unlimited number of any characters. ls *, for instance, shows all files in the current directory (except those that have a name starting with a dot). |
| ? | Used to refer to one specific character that can be any character. ls c?t would match cat as well as cut. |
| [auo] | Refers to one character that may be selected from the range that is specified between square brackets. ls c[auo]t would match cat, cut, and cot. |

### <b><ins><i>Commands</i></ins></b>

| Wildcard | Use |   
|:-------|:----------|
| cd | Brings one back to his/her home directory |
| cd .. | Goes one step back in the folder hierarchy. |
| cd / | Brings us to the root directory |
| cd /home | Takes us to /home directory |
| touch file1 | Creates and empty file by the name file1. |
| mkdir folder1 | Creates a directory by the name folder1 |
| rmdir folder1 | Deletes the folder by the name folder1 |