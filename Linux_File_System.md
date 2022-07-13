# <b><ins><i>Linux File System</i></ins></b>
  
### <b><ins>Linux Filesystem Hierarchy Standard (FHS)</ins></b>

The layout of the Linux file system is defined in the Filesystem Hierarchy Standard (FHS), and this file system hierarchy is described in man 7 hier.  

| Directory | Use |   
|:-------|:----------|
| / | The root directory. This is where the file system tree starts. |
| /boot | Contains all files and directories that are needed to boot the Linux kernel. |
| /dev | Contains device files that are used for accessing physical devices. This directory is essential during boot. |
| /etc | Contains configuration files that are used by programs and services on your server. This directory is essential during boot. |
| /home  | Used for local user home directories. |
| /media, /mnt | Contain directories that are used for mounting devices in the file system tree. |
| /opt | Used for optional packages that may be installed on your server. |
| /proc | Used by the proc file system. This is a file system structure that gives access to kernel information. |
| /root | The home directory of the root user. |
| /run | Contains process and user-specific information that has been created since the last boot. |
| /srv | May be used for data by services like NFS, FTP, and HTTP. |
| /sys | Used as an interface to different hardware devices that is managed by the Linux kernel and associated processes. |
| /tmp | Contains temporary files that may be deleted without any warning during boot. |
| /usr | Contains subdirectories with program files, libraries for these program files, and documentation about them. |
| /var | Contains files that may change in size dynamically, such as log files, mail boxes, and spool files. |

### <b><ins>Commands</ins></b>
* mount : The mount command gives an overview of all mounted devices. To get this information, the /proc/mounts file is read, where the kernel keeps information about all current mounts. It shows kernel interfaces also, which may lead to a long list of mounted devices being displayed.
```bash
mount
```
  
* df -Th : The df -Th command was designed to show available disk space on mounted devices; it includes most of the system mounts. Because it will look on all mounted file systems, it is a convenient command to get an overview of current system mounts. The -h option summarizes the output of the command in a human-readable way, and the -T option shows which file system type is used on the different mounts.
```bash
df -Th
```
* findmnt: The findmnt command shows mounts and the relationship that exists between the different mounts. Because the output of the mount command is a bit overwhelming, you may like the output of findmnt.
```bash
findmnt
```


