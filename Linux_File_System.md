# <b><ins><i>Linux File System</i></ins></b>
  
### <b><ins>Basic Specs for installing RHEL 8</ins></b>

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