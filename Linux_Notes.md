# <b><ins><i>Linux Notes</i></ins></b>
  
### <b><ins>Basic Specs for installing RHEL 8</ins></b>
* 1 GiB RAM
* 10 GiB Hard Disk
* Network Card

### <b><ins>KDUMP</ins></b> 
Allows you to use a KDUMP kernel. This is a kernel that creates a core dump if anything goes wrong.  
  
### <b><ins>Deafult File System In RHEL 8</ins></b>
RHEL 8 by default uses the XFS file system. This file system cannot be shrunk; it can only be expanded. Therefore, it is sometimes a better choice to use Ext4.  
  
### <b><ins>Benefits of RHEL 8</ins></b>
The most important things that you get in the official RHEL 8 Server release is access to the Red Hat Customer Portal. Through this portal, you have access to a wide variety of information regarding RHEL, in addition to updates provided through Red Hat Network (RHN). In particular, the Red Hat knowledge base is invaluable; you can use it to find answers to many common problems that have been posted there by Red Hat consultants.

### <b><ins>Alias</ins></b>
An alias is a command that a user can define as needed. Some aliases are provided by default; type alias on the command line to get an overview. To define an alias, use alias newcommand='oldcommand', as in the default alias ll='ls -l --color=auto' that has already been created on your system. Aliases are executed before anything else. So, if you have an alias with the name ll but also a command with the name ll, the alias will always take precedence, unless a complete pathname is used.
```bash
cls='clear --color=auto'
```

### <b><ins>VIM Commands</ins></b>

| VIM Command | Explanation |   
|:-------|:----------|
| Esc | Switches from input mode to command mode. Press this key before typing any command. |
| i, a | Switches from command mode to input mode at (i) or after (a) the current cursor position. |
| o | Opens a new line below the current cursor position and goes to input mode. | 
