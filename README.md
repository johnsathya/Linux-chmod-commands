Linux-chmod-commands
====================
chmod

The chmod command is used to change the permissions of a file or directory. To use it, you specify the desired permission settings and the file or files that you wish to modify.

It is easy to think of the permission settings as a series of bits (which is how the computer thinks about them). Here's how it works:

rwx rwx rwx = 111 111 111
rw- rw- rw- = 110 110 110
rwx --- --- = 111 000 000

and so on...

rwx = 111 in binary = 7
rw- = 110 in binary = 6
r-x = 101 in binary = 5
r-- = 100 in binary = 4

In terminal we can see,
  drwxrwxr-x 10 www-data root ... ..( Here 'd' stands for directory)
  -rwxr-xr-x  1 www-data root ... ..( Here '-' stands for file)  
  
Value	Meaning
777   (rwxrwxrwx) No restrictions on permissions. Anybody may do anything. Generally not a desirable setting.

755   (rwxr-xr-x) The file's owner may read, write, and execute the file. All others may read and execute the file. This setting is common for programs that are used by all users.

700   (rwx------) The file's owner may read, write, and execute the file. Nobody else has any rights. This setting is useful for programs that only the owner may use and must be kept private from others.

666   (rw-rw-rw-) All users may read and write the file.

644   (rw-r--r--) The owner may read and write a file, while all others may only read the file. A common setting for data files that everybody may read, but only the owner may change.

600   (rw-------) The owner may read and write a file. All others have no rights. A common setting for data files that the owner wants to keep private.

Example :How to used in terminal:
  user :
  user@user:~$ sudo chmod -R 777 
  super user :
  user@user:~$ chmod -R 777
    


  
  
