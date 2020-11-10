### HW 5: ls -l


Implement a simplified analog of the ls -l command.

The name of the directory is passed to the program as an argument.

It is necessary to display the contents of the directory as:

ATTRIBUTES QTY_REFERENCE OWNER GROUP SIZE NAME \
If a file name is specified as an argument, then display information only about this single file.

For symbolic links, print the other filenames they link to.

In case of an error, output the error text to the standard error stream and exit with code 1.


#### Examples

##### Input
/boot

##### Output

-rw-r--r-- 1 root root      512 backup_mbr \
lrwxrwxrwx 1 root root        1 boot -> . \
-rw-r--r-- 1 root root     1725 boot.readme \
-rw-r--r-- 1 root root   196482 config-4.12.14-lp150.12.22-default \
drwxr-xr-x 6 root root     4096 grub2 \
lrwxrwxrwx 1 root root       34 initrd -> initrd-4.12.14-lp150.12.22-default \
-rw------- 1 root root 11847632 initrd-4.12.14-lp150.12.22-default \
-rw-r--r-- 1 root root   182704 memtest.bin \
-rw-r--r-- 1 root root   422912 message \
-rw-r--r-- 1 root root  1124964 symtypes-4.12.14-lp150.12.22-default.gz \
-rw-r--r-- 1 root root   388747 symvers-4.12.14-lp150.12.22-default.gz \
-rw-r--r-- 1 root root      484 sysctl.conf-4.12.14-lp150.12.22-default \
-rw-r--r-- 1 root root  3474420 System.map-4.12.14-lp150.12.22-default \
-rw-r--r-- 1 root root  8028448 vmlinux-4.12.14-lp150.12.22-default.gz \
lrwxrwxrwx 1 root root       35 vmlinuz -> vmlinuz-4.12.14-lp150.12.22-default \
-rw-r--r-- 1 root root  7057520 vmlinuz-4.12.14-lp150.12.22-default

#### Codereview
In order to pass the task you will need to attend the review. It will be conducted via zoom meeting for every student personally. It should last around 15mins for every student. The codereview will be conducted at the seminar time. It will be start Dec 1-st 13:55.

### Checking solutions and soft deadline
You need to send at least partially working solution by Nov 24-th 23:59:59.

#### Deadline:
Nov 30, 23:59:59

#### Points:
This task costs 18pts
