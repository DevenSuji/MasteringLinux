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

### <b><ins><i>Copying Files</i></ins></b>  
  
If you copy a file to a directory, but the target directory does not exist, a file will be created with the name of the alleged target directory. In many cases, that’s not the best solution and it would be better to just get an error message instead. You can
accomplish this by placing a / after the directory name, so use cp /etc/hosts /tmp/ and not cp /etc/hosts /tmp.  
  
| Command | Use |   
|:-------|:----------|
| cp /etc/hosts /tmp/file1 | Contents of the file hosts is copied over to the file by the name file1 |
| cp -R /tmp /tmp/sound/ | Recursive copy |
| cp -a ~ /tmp. | -a option keeps the permissions intact when copying |  
  
A special case when working with cp is hidden files. By default, hidden files are not copied over. There are three solutions to copy hidden files as well:  
```bash
cp /somedir/.* /tmp
``` 
This copies all files that have a name starting with a dot (the hidden files, that is) to /tmp. It gives an error message for directories whose name starts with a dot in /somedir, because the -R option was not used.  
  
```bash
cp -a /somedir/
```
This copies the entire directory /somedir, including its contents, to the current directory. So, as a result, a subdirectory somedir will
be created in the current directory.  
  
```bash
cp -a /somedir/. .
```
This copies all files, regular and hidden, to the current directory (notice the space between the two dots at the end of this command).

### <b><ins><i>Moving  Files</i></ins></b> 
To move files, you use the mv command. This command removes the file from its current location and puts it in the new location. You can also use it to rename a file (which, in fact, is nothing else than copying and deleting the original file anyway).  
Let’s take a look at some examples:  
* mv myfile /tmp: Moves the file myfile from the current directory to /tmp.  
* mkdir somefiles; mv somefiles /tmp: First creates a directory with the name somefiles and then moves this directory to /tmp. Notice that this also works if the directory contains files.  
* mv myfile mynewfile: Renames the file myfile to a new file with the name mynewfile.  
  
### <b><ins><i>Deleting Files</i></ins></b>
```bash
rm filename # Deletes the file by the name filename
rm -r /tmp/ # Deletes the files recursively.
```

### <b><ins><i>Links</i></ins></b>
Links on Linux are like aliases that are assigned to a file. There are symbolic links, and there are hard links. To understand a link, you need to know a bit about how the Linux file system uses inodes for file system administration.


##### <b><ins><i>Understanding Hard Links</i></ins></b>
Linux stores administrative data about files in inodes. The inode is used to store all administrative data about files. Every file on Linux has an inode, and in the inode, important information about the file is stored:
* The data block where the file contents are stored.
* The creation, access, and modification date.
* Permissions.
* File owners.  
  
Just one important piece of information is not stored in the inode: the name of the file. Names are stored in the directory, and each filename knows which inode it has to address to access further file information. It is interesting to know that an inode does not know which name it has; it just knows how many names are associated with the inode. These names are referred to as hard links. When you create a file, you give it a name. Basically, this name is a hard link. On a Linux file system, multiple hard links can be created to a file. This can be useful, because it enables you to access the file from multiple different locations. Some restrictions apply to hard links, though:  
* Hard links must exist all on the same device (partition, logical volume, etc).
* You cannot create hard links to directories.
* When the last name (hard link) to a file is removed, access to the file’s data is also removed.  
  
The nice thing about hard links is that no difference exists between the first hard link and the second hard link. They are both just hard links, and if the first hard link that ever existed for a file is removed, that does not impact the other hard links that
still exist. The Linux operating system uses links on many locations to make files more accessible.  
  
##### <b><ins><i>Understanding Symbolic Links</i></ins></b>  



