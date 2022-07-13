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

### <b><ins><i>Absolute and Relative Pathnames</i></ins></b>

* Absolute filename/pathname: An absolute filename, or absolute pathname, is a complete path reference to the file or
directory you want to work with. This pathname starts with the root directory, followed by all subdirectories up to the actual filename. No matter what your current directory is, absolute filenames will always work. An example of an absolute filename is /home/lisa/file1.
  
* Relative filename/pathname: A relative filename is relative to the current directory as shown with the pwd command. It contains only the elements that are required to get from the current directory up to the item you need. Suppose that your current directory is /home
(as shown by the pwd command). When you refer to the relative filename lisa/file1, you are referring to the absolute filename /home/lisa/file1.


### <b><ins><i>Listing Files and Directories</i></ins></b>

| Command | Use |   
|:-------|:----------|
| ls -l | Shows a long listing, which includes information about file properties, such as creation date and permissions. |
| ls -a | Shows all files, including hidden files. |
| ls -lrt | This is a very useful command. It shows commands sorted on modification date. You’ll see the most recently modified files last in the list. |
| ls -d | Shows the names of directories, not the contents of all directories that match the wildcards that have been used with the ls command. |
| ls -R | Shows the contents of the current directory, in addition to all of its subdirectories; that is, it Recursively descends all subdirectories. |