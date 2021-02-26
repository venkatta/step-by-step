how to reset root password in CentOS 7.

#

* In the boot grub menu select option to edit.
* Select Option to edit (e).
* Go to the line of Linux 16 and change ro with rw init=/sysroot/bin/sh.
* Now press Control+x to start on single user mode.
* Now access the system with this command.
```
chroot /sysroot
```
* Reset the password.
```
passwd root
```
* Update selinux information
```
touch /.autorelabel
```
* Exit chroot
```
exit
```
* Reboot your system
```
reboot
```
