---
title: "Master the Linux command line with this beginner-friendly guide! From file ops to networking, become a Linux pro in no time."
seoTitle: "Mastering Essential Linux Commands: A Comprehensive Guide for Beginner"
seoDescription: "Master the Linux command line with this beginner-friendly guide! From file ops to networking, become a Linux pro in no time."
datePublished: Fri Apr 07 2023 13:46:47 GMT+0000 (Coordinated Universal Time)
cuid: clkfhto2m000709mb54gy8we3
slug: master-the-linux-command-line-with-this-beginner-friendly-guide-from-file-ops-to-networking-become-a-linux-pro-in-no-time
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690120241314/23916f93-1918-41e8-9c4b-5635c942a73e.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1690120958081/923b2e9b-7865-410e-8a0f-294f2f4a3932.jpeg
tags: linux, bash, devops, linux-for-beginners, linux-commands

---

## ls

**The** `ls` **command: List Files / Directories**

1. To show the files inside your current working directory:
    

```bash
ls
```

1. To show the files and directory inside a specific Directory:
    

```bash
ls {Directory_Path}
```

Syntax:

```bash
ls [-OPTION] [DIRECTORY_PATH]
```

Additional Flags and their Functionalities:

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-l` | \- | Show results in a long format |
| `-S` | \- | Sort results by file size |
| `-t` | \- | Sort results by modification time |
| `-r` | `--reverse` | Show files and directories in reverse order *(descending alphabetical order)* |
| `-a` | `--all` | Show all files, including hidden files *(file names which begin with a period* `.`) |
| `-la` | \- | Show long-format files and directories including hidden files |
| `-lh` | \- | list long format files and directories with readable size |
| `-A` | `--almost-all` | Shows all like `-a` but without showing `.`(current working directory) and `..` (parent directory) |
| `-d` | `--directory` | Instead of listing the files and directories inside the directory, it shows any information about the directory itself, it can be used with `-l` to show long formatted information |
| `-F` | `--classify` | Appends an indicator character to the end of each listed name, as an example: `/` character is appended after each directory name listed |
| `-h` | `--human-readable` | like `-l` but displays file size in the human-readable unit not in bytes |

## cd

The `cd` command: Used for Changing directory

Change the current working directory:

```bash
cd <specified_directory_path>
```

1. Change the current working directory to the home directory:
    

```bash
cd ~
```

OR

```bash
cd
```

1. Change to the previous directory:
    

```bash
cd -
```

This will also echo the absolute path of the previous directory.

1. Change the current working directory to the system's root directory:
    

```bash
cd /
```

Quick Tips

Adding a `..` as a directory will allow you to move "up" from a folder:

```bash
cd ..
```

This can also be done multiple times! For example, to move up three folders:

```bash
cd ../../../
```

Syntax:

```bash
cd [OPTIONS] directory
```

Additional Flags and Their Functionalities

| **Short flag** | **Long flag** | **Description** |
| --- | --- | --- |
| `-L` | \- | Follow symbolic links. By default,`cd` behaves as if the `-L` option is specified. |
| `-P` | \- | Don’t follow symbolic links. |

## cat

The `cat` command: concatenate files and redirect the output to the terminal or files

1. To display the content of a file in the terminal:
    

```bash
cat <specified_file_name>
```

1. To display the content of multiple files in the terminal:
    

```bash
cat file1 file2 ...
```

1. To create a file with the cat command:
    

```bash
cat > file_name
```

1. To display all files in the current directory with the same filetype:
    

```bash
cat *.<filetype>
```

1. To display the content of all the files in the current directory:
    

```bash
cat *
```

1. To put the output of a given file into another file:
    

```bash
cat old_file_name > new_file_name
```

1. Use the cat command with `more` and `less` options:
    

```bash
cat filename | more
cat filename | less
```

1. Append the contents of file1 to file2:
    

```bash
cat file1 >> file2
```

1. To concatenate two files together in a new file:
    

```bash
cat file1_name file2_name merge_file_name
```

1. In some implementations of cat, with option -n, it's possible to show line numbers:
    

```bash
cat -n file1_name file2_name > new_numbered_file_name
```

Syntax:

```bash
cat [OPTION] [FILE]...
```

Additional Flags and their Functionalities:

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-A` | `--show-all` | equivalent to -vET |
| `-b` | `--number-nonblank` | number nonempty output lines, overrides -n |
| `-e` | \- | equivalent to -vE |
| `-T` | \- | Display tab-separated lines in the file opened with `cat` command. |
| `-E` | \- | To show $ at the end of each file. |
| `-E` | \- | Display file with line numbers. |
| `-n` | `--number` | number all output lines |
| `-s` | `--squeeze-blank` | suppress repeated empty output lines |
| `-u` | \- | (ignored) |
| `-v` | `--show-nonprinting` | use ^ and M- notation, except for LFD and TAB |
| \- | `--help` | display this help and exit |
| \- | `--version` | output version information and exit |

---

## tac

The `tac` command: view files line-by-line, beginning from the last line.

`tac` is a Linux command that allows you to view files line-by-line, beginning from the last line. (tac doesn't reverse the contents of each line, only the order in which the lines are presented.) It is named by analogy with a `cat`.

**Examples:**

1. To display the content of a file in the terminal:
    

```bash
tac <specified_file_name>
```

1. This option attaches the separator before instead of after.
    

```bash
tac -b concat_file_name tac_example_file_name
```

1. This option will interpret the separator as a regular expression.
    

```bash
tac -r concat_file_name tac_example_file_name
```

1. This option uses STRING as the separator instead of a new line.
    

```bash
tac -s concat_file_name tac_example_file_name
```

1. This option will display the help text and exit.
    

```bash
tac --help
```

1. This option will give the version information and exit.
    

```bash
tac --version
```

Syntax:

```bash
tac [OPTION]... [FILE]...
```

Additional Flags and their Functionalities:

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-b` | `--before` | attach the separator before instead of after |
| `-r` | `--regex` | interpret the separator as a regular expression |
| `-s` | `--separator=STRING` | use STRING as the separator instead of Newline |
| \- | `--help` | display this help and exit |
| \- | `--version` | output version information and exit |

## mkdir

The `mkdir` command: Create a directory.

Syntax

```bash
$ mkdir [-m=mode] [-p] [-v] [-Z=context] directory [directory ...]
```

Examples

1. Make a directory named **myfiles**.
    

```bash
$ mkdir myfiles
```

1. Create a directory named **myfiles** in the home directory:
    

```bash
$ mkdir ~/myfiles
```

1. Create the **mydir** directory, and set its file mode (`-m`) so that all users (`a`) may read (`r`), write (`w`), and execute (`x`) it.
    

```bash
$ mkdir -m a=rwx mydir
```

You can also create sub-directories of a directory. It will create the parent directory first if it doesn't exist. If it already exists, then it moves further to create the sub-directories without any error message.

For directories, this means that any user on the system may view ("read"), and create/modify/delete ("write") files in the directory. Any user may also change to ("execute") the directory, for example with the `cd` command.

1. Create the directory **/home/test/src/python**. If any of the parent directories **/home**, **/home/test**, or **/home/test/src** do not already exist, they are automatically created.
    

```bash
$ mkdir -p /home/test/src/python
```

Options

| **Short Flags** | **Long Flags** | **Descriptions** |
| --- | --- | --- |
| `-m` | `--mode=MODE` | Set file mode (as in chmod), not `a=rwx - unmask`. |
| `-p` | `--parents` | No error if existing, make parent directories as needed. |
| `-v` | `--verbose` | Print a message for each created directory. |
| `-Z` | `--context=CTX` | Set the SELinux security context of each created directory to CTX. |
| \- | `--help` | Display a help message and exit. |
| \- | `--version` | Output version information and exit. |

## rmdir

The rmdir command is used to remove empty directories from the filesystem in Linux. The rmdir command removes every directory specified in the command line only if these directories are empty.

Syntax:

```bash
rmdir [OPTION]... DIRECTORY...
```

1. remove directory and its ancestors
    

```bash
rmdir -p a/b/c			// is similar to 'rmdir a/b/c a/b a'
```

1. remove multiple directories
    

```bash
rmdir a b c
```

Additional Flags and their Functionalities:

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-` | `--ignore-fail-on-non-empty` | ignore each failure that is solely because a directory is non-empty |
| `-p` | `--parents` | remove DIRECTORY and its ancestors |
| `-d` | `--delimiter=DELIM` | use DELIM instead of TAB for field delimiter |
| `-v` | `--verbose` | output a diagnostic for every directory processed |

## touch

The `touch` Command: modifies a file's timestamps. If the file specified doesn't exist, an empty file with that name is created.

Syntax

```bash
touch [OPTION]... FILE...
```

Options

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-a` | \- | Change only the access time. |
| `-c` | `--no-create` | Do not create any files. |
| `-d` STRING | `--date=STRING` | Parse *STRING* and use it instead of the current time. |
| `-f` | \- | (Ignored) This option does nothing but is accepted to provide compatibility with BSD versions of the `touch` command. |
| `-h` | `--no-dereference` | Affect each symbolic link instead of any referenced file (useful only on systems that can change the timestamps of a symlink). This option implies `-c`, nothing is created if the file does not exist. |
| `-m` | \- | Change only the modification time. |
| `-r=FILE` | `--reference=FILE` | Use this file's times instead of the current time. |
| `-t STAMP` | \- | Use the numeric time *STAMP* instead of the current time. The format of *STAMP* is \[\[**CC**\]**YY**\]**MMDDhhmm**\[**.ss**\]. |
| \- | `--time=WORD` | An alternate way to specify which type of time is set (e.g. *access*, *modification*, or *change*). This is equivalent to specifying `-a` or `-m`. |

## vim

The vim is a text editor for Unix that comes with Linux, BSD, and macOS. It is known to be fast and powerful.

Note: Do not confuse vim with vi. vi, which stands for "Visual", is a text editor. vim stands for "Vi Improved", and is an improved clone of the vi editor.

Syntax:

```bash
vim [FILE_PATH/FILE_NAME]
```

1. To open the file named "demo.txt" from your current directory:
    

```bash
vim demo.txt
```

1. To open the file in a specific directory:
    

```bash
vim {File_Path/filename}
```

1. To open the file starting on a specific line in the file:
    

```bash
vim {File_Path/filename} +LINE_NUMBER
```

Interactive training: In this interactive tutorial, you will learn the different ways to use the Vim command:

[https://www.openvim.com/](https://www.openvim.com/)

Additional Flags and their Functionalities:

| **Flags/Options** | **Description** |
| --- | --- |
| `-e` | Start in Ex mode (see [Ex-mode](http://vimdoc.sourceforge.net/htmldoc/intro.html#Ex-mode)) |
| `-R` | Start in read-only mode |
| `-R` | Start in read-only mode |
| `-g` | Start the [GUI](http://vimdoc.sourceforge.net/htmldoc/gui.html#GUI) |
| `-eg` | Start the GUI in Ex mode |
| `-Z` | Like "vim", but in restricted mode |
| `-d` | Start in diff mode [diff-mode](http://vimdoc.sourceforge.net/htmldoc/diff.html#diff-mode) |
| `-h` | Give usage (help) message and exit |
| `+NUMBER` | Open a file and place the cursor on the line number specified by NUMBER |

## nano

The `nano` command: lets you create/edit text files.

1. Open an existing file, type `nano` followed by the path to the file:
    

```bash
nano /path/to/filename
```

1. Create a new file, type `nano` followed by the filename:
    

```bash
nano filename
```

1. Open a file with the cursor on a specific line and character use the following syntax:
    

```bash
nano +line_number,character_number filename
```

Overview of some Shortcuts and their Functionalities:

| **Shortcut** | **Description** |
| --- | --- |
| `Ctrl + S` | Save current file |
| `Ctrl + O` | Offer to write file ("Save as") |
| `Ctrl + X` | Close buffer, exit from nano |
| `Ctrl + K` | Cut current line into cutbuffer |
| `Ctrl + U` | Paste contents of cutbuffer |
| `Alt + 6` | Copy current line into cutbuffer |
| `Alt + U` | Undo last action |
| `Alt + E` | Redo last undone action |

## who

The `who` command: lets you print out a list of logged-in users, the current run level of the system and the time of the last system boot.

1. Print out all details of currently logged-in users
    

```bash
who -a
```

1. Print out the list of all dead processes
    

```bash
who -d -H
```

Syntax:

```bash
who [options] [filename]
```

Additional Flags and their Functionalities

| **Short Flag** | **Description** |
| --- | --- |
| `-r` | prints all the current run level |
| `-d` | print all the dead processes |
| `-q` | print all the login names and the total number of logged-on users |
| `-h` | print the heading of the columns displayed |
| `-b` | print the time of the last system boot |

## whoami

The `whoami` command: displays the username of the current effective user.

Syntax:

```bash
whoami [-OPTION]
```

There are only two options which can be passed to it :

`--help`: Used to display the help and exit

`--version`: Output version information and exit

## echo

The `echo` command: display the line of text/string that is passed as an argument

1. To Show the line of text or string passed as an argument:
    

```bash
echo Hello There
```

1. To show all files/folders similar to the `ls` command:
    

```bash
echo *
```

1. To save text to a file named [foo. bar](http://foo.bar):
    

```bash
echo "Hello There" > foo.bar
```

1. To append text to a file named [foo. bar](http://foo.bar):
    

```bash
echo "Hello There" >> foo.bar
```

Syntax:

```bash
echo [option] [string]
```

It is usually used in shell scripts and batch files to output status text to the screen or a file. The `-e` used with it enables the interpretation of backslash escapes

Additional Options and their Functionalities:

| **Option** | **Description** |
| --- | --- |
| `\b` | removes all the spaces in between the text |
| `\c` | suppress trailing new line with backspace interpreter ‘-e‘ to continue without emitting new line. |
| `\n` | creates a new line from where it is used |
| `\t` | creates horizontal tab spaces |
| `\r` | carriage returns with backspace interpreter ‘-e‘ to have specified carriage return in output |
| `\v` | creates vertical tab spaces |
| `\a` | alert returns with a backspace interpreter ‘-e‘ to have a sound alert |
| `-n` | omits echoing trailing newline. |

## su

The `su` command: allows you to run commands with a substitute user and group ID.

Syntax:

```bash
$ su [options] [-] [<user>[<argument>...]]
```

Options :

```bash
-m, -p         --> do not reset environment variables
-w             --> do not reset specified variables
-g             --> specify the primary group
-G             --> specify a supplemental group
-l             --> make the shell a login shell
-f             --> pass -f to the shell (for csh or tcsh)
-s             --> run <shell> if /etc/shell allows it 
-p             --> create a new pseudo terminal
-h             --> display this help
-v             --> display version
```

## useradd

The `useradd` command: used to add or update user accounts to the system.

To add a new user with the `useradd` command the syntax would be the following:

```bash
useradd NewUser
```

To add a new user with the `useradd` command and give a home directory path for this new user the syntax would be the following:

```bash
useradd -d /home/NewUser NewUser
```

To add a new user with the `useradd` command and give it a specific id the syntax would be the following:

```bash
useradd -u 1234 NewUser
```

Syntax:

```bash
useradd [OPTIONS] NameOfUser
```

Possible options:

| **Flag** | **Description** | **Params** |
| --- | --- | --- |
| `-d` | The new user will be created using /path/to/directory as the value for the user's login directory | /path/to/directory |
| `-u` | The numerical value of the user's ID | ID |
| `-g` | Create a user with a specific group id | GroupID |
| `-M` | Create a user without a home directory | \- |
| `-e` | Create a user with an expiry date | DATE (format: YYYY-MM-DD) |
| `-c` | Create a user with a comment | COMMENT |
| `-s` | Create a user with a changed login shell | /path/to/shell |
| `-p` | Set an unencrypted password for the user | PASSWORD |

## userdel

The `userdel` command: used to delete a user account and related files

To delete a user with the `userdel` command the syntax would be the following:

```bash
userdel userName
```

To force the removal of a user account even if the user is still logged in, using the `userdel` command the syntax would be the following:

```bash
userdel -f userName
```

To delete a user along with the files in the user’s home directory using the `userdel` command the syntax would be the following:

```bash
userdel -r userName
```

Syntax:

```bash
userdel [OPTIONS] userName
```

Possible options:

| **Flag** | **Description** |
| --- | --- |
| `-f` | Force the removal of the specified user account even if the user is logged in |
| `-r` | Remove the files in the user’s home directory along with the home directory itself and the user’s mail spool |
| `-Z` | Remove any SELinux(Security-Enhanced Linux) user mapping for the user’s login. |

## usermod

The `usermod` command: lets you change the properties of a user in Linux through the command line. After creating a user we sometimes have to change their attributes, like their password or login directory etc. So to do that we use the `usermod` command.

Syntax:

```bash
usermod [options] USER
```

Note : Only the superuser (root) is allowed to execute `usermod` command

Options and their Functionalities:

| **Option** | **Description** |
| --- | --- |
| `-a` | to add anyone in the group to a secondary group |
| `-c` | to add a comment field for the user account |
| `-d` | to modify the directory for any existing user account |
| `-g` | change the primary group for a User |
| `-G` | to add supplementary groups |
| `-l` | to change the existing user login name |
| `-L` | to lock a system user account |
| `-m` | to move the contents of the home directory from the existing home dir to the new dir |
| `-p` | to create an un-encrypted password |
| `-s` | to create a specified shell for new accounts |
| `-u` | to assign UID for the user account |
| `-U` | to unlock any locked user |

Examples:

1. To add a comment/description for a user:
    

```bash
sudo usermod -c "This is test user" test_user
```

1. To change the home directory of a user:
    

```bash
sudo usermod -d /home/sam test_user
```

1. To change the expiry date of a user:
    

```bash
sudo usermod -e 2021-10-05 test_user
```

1. To change the group of a user:
    

```bash
sudo usermod -g sam test_user
```

1. To change the user login name:
    

```bash
sudo usermod -l test_account test_user
```

1. To lock a user:
    

```bash
sudo usermod -L test_user
```

1. To unlock a user:
    

```bash
sudo usermod -U test_user
```

1. To set an unencrypted password for the user:
    

```bash
sudo usermod -p test_password test_user
```

1. To create a shell for the user:
    

```bash
sudo usermod -s /bin/sh test_user
```

1. To change the user id of a user:
    

```bash
sudo usermod -u 1234 test_user
```

## passwd

The `passwd` command: changes the password of user accounts. A normal user may only change the password for their account, but a superuser may change the password for any account. `passwd` also changes the account or associated password validity period.

The syntax of the `passwd` command is :

```bash
$ passwd [options] [LOGIN]
```

options

```bash
-a, --all
        This option can be used only with -S and causes show status for all users.

-d, --delete
        Delete a user's password.

-e, --expire
        Immediately expire an account's password.

-h, --help
        Display help message and exit.

-i, --inactive
        This option is used to disable an account after the password has been expired for a number of days.

-k, --keep-tokens
        Indicate password change should be performed only for expired authentication tokens (passwords).

-l, --lock
        Lock the password of the named account.

-q, --quiet
        Quiet mode.

-r, --repository
        change password in repository.

-S, --status
        Display account status information.
```

## login

The `login` Command: Initiates a user session.

Syntax

```bash
$ login [-p] [-h host] [-H] [-f username|username]
```

Flags and their functionalities

| **Short Flag** | **Description** |
| --- | --- |
| `-f` | Used to skip a login authentication. This option is usually used by the getty(8) autologin feature. |
| `-h` | Used by other servers (such as telnetd(8) to pass the name of the remote host to login so that it can be placed in utmp and wtmp. Only the superuser is allowed use this option. |
| `-p` | Used by getty(8) to tell login to preserve the environment. |
| `-H` | Used by other servers (for example, telnetd(8)) to tell login that printing the hostname should be suppressed in the login: prompt. |
| `--help` | Display help text and exit. |
| `-v` | Display version information and exit. |

Examples

To log in to the system as user sniper, enter the following at the login prompt:

```bash
$ login: sniper
```

If a password is defined, the password prompt appears. Enter your password at this prompt.

## cp

The `cp` command: used to copy files or groups of files or directories. It creates an exact image of a file on a disk with different file name. The cp command requires at least two filenames in its arguments.

1. To copy the contents of the source file to the destination file.
    

```bash
cp sourceFile destFile
```

If the destination file doesn't exist then the file is created and the content is copied to it. If it exists then the file is overwritten.

1. To copy a file to another directory specify the absolute or the relative path to the destination directory.
    

```bash
cp sourceFile /folderName/destFile
```

1. To copy a directory, including all its files and subdirectories
    

```bash
cp -R folderName1 folderName2
```

The command above creates the destination directory and recursively copies all files and subdirectories from the source to the destination directory.

If the destination directory already exists, the source directory itself and its content are copied inside the destination directory.

1. To copy only the files and subdirectories but not the source directory
    

```bash
cp -RT folderName1 folderName2
```

Syntax:

The general syntax for the cp command is as follows:

```bash
cp [OPTION] SOURCE DESTINATION
cp [OPTION] SOURCE DIRECTORY
cp [OPTION] SOURCE-1 SOURCE-2 SOURCE-3 SOURCE-n DIRECTORY
```

The first and second syntax is used to copy the Source file to the Destination file or Directory. The third syntax is used to copy multiple Sources(files) to the Directory.

Some useful options

1. `-i` (interactive) `i` stands for Interactive copying. With this option system first warns the user before overwriting the destination file. cp prompts for a response, if you press y then it overwrites the file and with any other option leaves it uncopied.
    

```bash
$ cp -i file1.txt fileName2.txt
cp: overwrite 'file2.txt'? y
```

1. `-b`(backup) -b(backup): With this option cp command creates the backup of the destination file in the same folder with a different name and in a different format.
    

```bash
$ ls
a.txt b.txt

$ cp -b a.txt b.txt

$ ls
a.txt b.txt b.txt~
```

1. `-f`(force) If the system is unable to open the destination file for writing operation because the user doesn't have writing permission for this file then by using the -f option with the cp command, the destination file is deleted first and then copied of content is done from source to destination file.
    

```bash
$ ls -l b.txt
-r-xr-xr-x+ 1 User User 3 Nov 24 08:45 b.txt
```

User, group and others don't have writing permission.

Without `-f` option, command not executed

```bash
$ cp a.txt b.txt
cp: cannot create regular file 'b.txt': Permission denied
```

With the -f option, the command executed successfully

```bash
$ cp -f a.txt b.txt
```

Additional Flags and their Functionalities:

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-i` | \--interactive | prompt before overwrite |
| `-f` | \--force | If an existing destination file cannot be opened, remove it and try again |
| `-b` | \- | Creates the backup of the destination file in the same folder with a different name and in a different format. |
| `-r or -R` | `--recursive` | **cp** command shows its recursive behaviour by copying the entire directory structure recursively. |
| `-n` | `--no-clobber` | do not overwrite an existing file (overrides a previous -i option) |
| `-p` | \- | preserve the specified attributes (default: mode, ownership, timestamps), if possible additional attributes: context, links, xattr, all |

## mv

The `mv` command: lets you move one or more files or directories from one place to another in a file system like UNIX.

It can be used for two distinct functions:

* To rename a file or folder.
    
* To move a group of files to a different directory.
    

Syntax:

```bash
mv [options] source (file or directory)  destination
```

1. To rename a file called old\_name.txt:
    

```bash
mv old_name.txt new_name.txt
```

1. To move a file called *essay.txt* from the current directory to a directory called *assignments* and rename it *essay1.txt*:
    

```bash
mv essay.txt assignments/essay1.txt
```

1. To move a file called *essay.txt* from the current directory to a directory called *assignments* without renaming it
    

```bash
mv essay.txt assignments
```

Additional Flags and their Functionalities:

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-f` | `--force` | Force move by overwriting destination file without prompt |
| `-i` | `--interactive` | Interactive prompt before overwrite |
| `-u` | `--update` | Move only when the source file is newer than the destination file or when the destination file is missing |
| `-n` | `--no-clobber` | Do not overwrite an existing file |
| `-v` | `--verbose` | Print source and destination files |
| `-b` | `--backup` | Create a Backup of the Existing Destination File |

## ifconfig

ifconfig is used to configure the kernel-resident network interfaces. It is used at boot time to set up interfaces as necessary. After that, it is usually only needed when debugging or when system tuning is needed.

Syntax:

```bash
ifconfig [-v] [-a] [-s] [interface]
ifconfig [-v] interface [aftype] options
```

1. To display the currently active interfaces:
    

```bash
ifconfig
```

1. To show all interfaces which are currently active, even if down:
    

```bash
ifconfig -a
```

1. To show all the error conditions:
    

```bash
ifconfig -v
```

1. To show a short list:
    

```bash
ifconfig -s
```

1. To display details of the specific network interface (say `eth0`):
    

```bash
ifconfig eth0
```

1. To activate the driver for an interface (say `eth0`):
    

```bash
ifconfig eth0 up
```

1. To deactivate the driver for an interface (say `eth0`):
    

```bash
ifconfig eth0 down
```

1. To assign a specific IP address to a network interface (say `eth0`):
    

```bash
ifconfig eth0 10.10.1.23
```

1. To change the MAC(Media Access Control) address of a network interface (say `eth0`):
    

```bash
ifconfig eth0 hw ether AA:BB:CC:DD:EE:FF
```

1. To define a netmask for a network interface (say `eth0`):
    

```bash
ifconfig eth0 netmask 255.255.255.224
```

1. To enable promiscuous mode on a network interface (say `eth0`):
    

```bash
ifconfig eth0 promisc
```

In normal mode, when a packet is received by a network card, it verifies that it belongs to itself. If not, it drops the packet normally. However, in the promiscuous mode, it accepts all the packets that flow through the network card.

1. To disable promiscuous mode on a network interface (say `eth0`):
    

```bash
ifconfig eth0 -promisc
```

1. To set the maximum transmission unit to a network interface (say `eth0`):
    

```bash
ifconfig eth0 mtu 1000
```

The MTU allows you to set the limit size of packets that are transmitted on an interface. The MTU can handle a maximum number of octets to an interface in one single transaction.

1. To add additional IP addresses to a network interface, you can configure a network alias to the network interface:
    

```bash
ifconfig eth0:0 10.10.1.24
```

Please note that the alias network address is in the same subnet mask of the network interface. For example, if your eth0 network ip address is `10.10.1.23`, then the alias IP address can be `10.10.1.24`. An example of an invalid IP address is `10.10.2.24` Since the interface subnet mask is `255.255.255.224`

1. To remove a network alias:
    

```bash
ifconfig eth0:0 down
```

Remember that for every scope (i.e. same net with address/netmask combination) all aliases are deleted, if you delete the first alias.

Help Command

Run the below command to view the complete guide to `ifconfig` command.

```bash
man ifconfig
```

## ip

The ip command is present in the net-tools which is used for performing several network administration tasks and used to show or manipulate routing, devices, and tunnels

Syntax:

```bash
ip [ OPTIONS ] OBJECT { COMMAND | help }
```

1. To assign an IP Address to a specific interface (eth1) :
    

```bash
 ip addr add 192.168.50.5 dev eth1
```

1. To show detailed information about network interfaces like IP Address, MAC Address information etc. :
    

```bash
ip addr show
```

Additional Flags and their Functionalities:

| **Flag** | **Description** |
| --- | --- |
| `-a` | Display and modify IP Addresses |
| `-l` | Display and modify network interfaces |
| `-r` | Display and alter the routing table |
| `-n` | Display and manipulate neighbour objects (ARP table) |
| `-ru` | The rule in the routing policy database. |
| `-s` | Output more information. If the option appears twice or more, the amount of information increases |
| `-f` | Specifies the protocol family to use |
| `-r` | Use the system's name resolver to print DNS names instead of host addresses |
| `-c` | To configure colour output |

## df

The df command in Linux/Unix is used to show the disk usage & information. df is an abbreviation for "disk free".

df displays the amount of disk space available on the file system containing each file name argument. If no file name is given, the space available on all currently mounted file systems is shown.

Syntax:

```bash
df [OPTION]... [FILE]...
```

1. Show available disk space Action\*\*:\*\* --- Output the available disk space and where the directory is mounted
    

Details: --- Outputted values are not human-readable (are in bytes)

Command\*\*:\*\*

```bash
df
```

1. Show available disk space in human-readable form **Action:** --- Output the available disk space and where the directory is mounted
    

Details: --- Outputted values ARE human-readable (are in GBs/MBs)

Command\*\*:\*\*

```bash
df -h
```

1. Show available disk space for the specific file system **Action:** --- Output the available disk space and where the directory is mounted
    

Details: --- Outputted values are only for the selected file system

Command:

```bash
df -hT file_system_name
```

1. Show available inodes Action: --- Output the available inodes for all file systems
    

Details: --- Outputted values are for inodes and not available space

Command:

```bash
df -i
```

1. Show file system type Action: --- Output the file system types
    

Details: --- Outputted values are for all file systems

Command:

```bash
df -T
```

1. Exclude file system type from the output Action\*\*:\*\* --- Output the information while excluding the chosen file system type
    

Details: --- Outputted values are for all file systems EXCEPT the chosen file system type

Command:

```bash
df -x file_system_type
```

Options

| **Short Flag** | **Long Flag** | **Description** |
| --- | --- | --- |
| `-a` | `--all` | Include pseudo, duplicate, and inaccessible file systems. |
| `-B` | `--block-size=SIZE` | Scale sizes by SIZE before printing them; e.g., `-BM` prints sizes in units of 1,048,576 bytes; see SIZE format below. |
| `-h` | `--human-readable` | Print sizes in powers of 1024 (e.g., 1023M). |
| `-H` | `--si` | Print sizes in powers of 1000 (e.g., 1.1G). |
| `-i` | `--inodes` | List inode information instead of block usage. |
| `-k` | \- | Like `--block-size=1K`. |
| `-l` | `--local` | Limit listing to local file systems. |
| \- | `--no-sync` | Do not invoke `sync` before getting usage info (default). |
| \- | `--output[=FIELD_LIST]` | Use the output format defined by `FIELD_LIST`, or print all fields if FIELD\_LIST is omitted. |
| `-P` | `--portability` | Use the `POSIX` output format |
| \- | `--sync` | Invoke sync before getting usage info. |
| \- | `--total` | Elide all entries insignificant to available space, and produce a grand total. |
| `-t` | `--type=TYPE` | Limit listing to file systems of type `TYPE`. |
| `-T` | `--print-type` | Print file system type. |
| `-x` | `--exclude-type=TYPE` | Limit listing to file systems not of type `TYPE`. |
| `-v` | \- | Ignored; included for compatibility reasons. |
| \- | `--help` | Display help message and exit. |
| \- | `--version` | Output version information and exit. |

## clear

In Linux, the clear command is used to clear the terminal screen.

```bash
$ clear
```

## wget

The wget command is used for downloading files from the Internet. It supports downloading files using HTTP, HTTPS and FTP protocols. It allows you to download several files at once, download in the background, resume downloads, limit bandwidth, mirror a website, and much more.

Syntax:

The `wget` syntax requires you to define the downloading options and the URL the to-be-downloaded file is coming from.

```bash
$ wget [options] [URL]
```

1. Starting a regular download
    

```bash
wget https://releases.ubuntu.com/20.04/ubuntu-20.04.3-desktop-amd64.iso
```

1. You can resume a download using the `-c` option
    

```bash
wget -c https://mirrors.piconets.webwerks.in/ubuntu-mirror/ubuntu-releases/20.04.3/ubuntu-20.04.3-desktop-amd64.iso
```

1. To download in the background, use the `-b` option
    

```bash
wget -b https://mirrors.piconets.webwerks.in/ubuntu-mirror/ubuntu-releases/20.04.3/ubuntu-20.04.3-desktop-amd64.iso
```

Additional Flags and Their Functionalities

| **short Flag** | **Description** |
| --- | --- |
| `-v` | prints version of the wget available on your system |
| `-h` | print help message displaying all the possible options |
| `-b` | This option is used to send a process to the background as soon as it starts. |
| `-t` | This option is used to set the number of retries to a specified number of times |
| `-c` | This option is used to resume a partially downloaded file |

## ssh

The ssh command in Linux stands for "Secure Shell". It is a protocol used to securely connect to a remote server/system. ssh is more secure in the sense that it transfers the data in encrypted form between the host and the client. ssh runs at TCP/IP port 22.

1. Use a Different Port Number for SSH Connection:
    

```bash
ssh test.server.com -p 3322
```

1. \-i ssh to a remote server using a private key?
    

```bash
ssh -i private.key user_name@host
```

1. \-l ssh specifying a different username
    

```bash
ssh -l alternative-username sample.ssh.com
```

Syntax:

```bash
ssh user_name@host(IP/Domain_Name)
```

```bash
ssh -i private.key user_name@host
```

```bash
ssh sample.ssh.com  ls /tmp/doc
```

Additional Flags and their Functionalities:

| **Flag** | **Description** |
| --- | --- |
| `-1` | Forces ssh to use protocol SSH-1 only. |
| `-2` | Forces ssh to use protocol SSH-2 only. |
| `-4` | Allows IPv4 addresses only. |
| `-A` | Authentication agent connection forwarding is enabled. |
| `-a` | Authentication agent connection forwarding is disabled. |
| `-B bind_interface` | Bind to the address of bind\_interface before attempting to connect to the destination host. This is only useful on systems with more than one address. |
| `-b bind_address` | Use bind\_address on the local machine as the source address of the connection. Only useful on systems with more than one address. |
| `-C` | Compresses all data (including stdin, stdout, stderr, and data for forwarded X11 and TCP connections) for a faster transfer of data. |
| `-c cipher_spec` | Selects the cipher specification for encrypting the session. |
| `-D [bind_address:]port` | Dynamic application-level port forwarding. This allocates a socket to listen to the port on the local side. When a connection is made to this port, the connection is forwarded over the secure channel, and the application protocol is then used to determine where to connect from the remote machine. |
| `-E log_file` | Append debug logs instead of standard errors. |
| `-e escape_char` | Sets the escape character for sessions with a pty (default: ‘~’). The escape character is only recognized at the beginning of a line. The escape character followed by a dot (‘.’) closes the connection; followed by control-Z suspends the connection; and followed by itself sends the escape character once. Setting the character to “none” disables any escapes and makes the session fully transparent. |
| `-F configfile` | Specifies a per-user configuration file. The default for the per-user configuration file is ~/.ssh/config. |
| `-f` | Requests ssh to go to the background just before command execution. |
| `-G` | Causes ssh to print its configuration after evaluating Host and Match blocks and exit. |
| `-g` | Allows remote hosts to connect to local forwarded ports. |
| `-I pkcs11` | Specify the PKCS#11 shared library ssh should use to communicate with a PKCS#11 token providing keys. |
| `-i identity_file` | A file from which the identity key (private key) for public key authentication is read. |
| `-J [user@]host[:port]` | Connect to the target host by first making an ssh connection to the jump host\[(/iam/jump-host) and then establishing a TCP forwarding to the ultimate destination from there. |
| `-K` | Enables GSSAPI-based authentication and forwarding (delegation) of GSSAPI credentials to the server. |
| `-k` | Disables forwarding (delegation) of GSSAPI credentials to the server. |
| `-L [bind_address:]port:host:hostport`, `-L [bind_address:]port:remote_socket`, `-L local_socket:host:hostport`, `-L local_socket:remote_socket` | Specifies that connections to the given TCP port or Unix socket on the local (client) host are to be forwarded to the given host and port, or Unix socket, on the remote side. This works by allocating a socket to listen to either a TCP port on the local side, optionally bound to the specified bind\_address, or to a Unix socket. Whenever a connection is made to the local port or socket, the connection is forwarded over the secure channel, and a connection is made to either the host port hostport, or the Unix socket remote\_socket, from the remote machine. |
| `-l login_name` | Specifies the user to log in as on the remote machine. |
| `-M` | Places the ssh client into “master” mode for connection sharing. Multiple -M options place ssh into “master” mode but with confirmation required using ssh-askpass before each operation that changes the multiplexing state (e.g. opening a new session). |
| `-m mac_spec` | A comma-separated list of MAC (message authentication code) algorithms, specified in order of preference. |
| `-N` | Do not execute a remote command. This is useful for just forwarding ports. |
| `-n` | Prevents reading from stdin. |
| `-O ctl_cmd` | Control an active connection multiplexing master process. When the -O option is specified, the ctl\_cmd argument is interpreted and passed to the master process. Valid commands are: “check” (check that the master process is running), “forward” (request forwardings without command execution), “cancel” (cancel forwardings), “exit” (request the master to exit), and “stop” (request the master to stop accepting further multiplexing requests). |
| `-o` | Can be used to give options in the format used in the configuration file. This is useful for specifying options for which there is no separate command-line flag. |
| `-p`, `--port PORT` | Port to connect to the remote host. |
| `-Q query_option` | Queries ssh for the algorithms supported for the specified version 2. The available features are: cipher (supported symmetric ciphers), cipher-auth (supported symmetric ciphers that support authenticated encryption), help (supported query terms for use with the -Q flag), mac (supported message integrity codes), kex (key exchange algorithms), kex-gss (GSSAPI key exchange algorithms), key (keytypes), key-cert (certificate key types), key-plain (non-certificate key types), key-sig (all keytypes and signature algorithms), protocol-version (supported SSH protocol versions), and sig (supported signature algorithms). Alternatively, any keyword from ssh\_config(5) or sshd\_config(5) that takes an algorithm list may be used as an alias for the corresponding query\_option. |
| `-q` | Quiet mode. This causes most warning and diagnostic messages to be suppressed. |
| `-R [bind_address:]port:host:hostport, -R [bind_address:]port:local_socket, -R remote_socket:host:hostport, -R remote_socket:local_socket, -R [bind_address:]port` | Specifies that connections to the given TCP port or Unix socket on the remote (server) host are to be forwarded to the local side. |
| `-S ctl_path` | Specifies the location of a control socket for connection sharing, or the string “none” to disable connection sharing. |
| `-s` | May be used to request the invocation of a subsystem on the remote system. Subsystems facilitate the use of SSH as a secure transport for other applications (e.g. sftp(1)). The subsystem is specified as the remote command. |
| `-T` | Disable pseudo-terminal allocation. |
| `-t` | Force pseudo-terminal allocation. This can be used to execute arbitrary screen-based programs on a remote machine, which can be very useful, e.g. when implementing menu services. Multiple -t options force tty allocation, even if ssh has no local tty. |
| `-V` | Display the version number. |
| `-v` | Verbose mode. It echoes everything it is doing while establishing a connection. It is very useful in the debugging of connection failures. |
| `-W host:port` | Requests that standard input and output on the client be forwarded to the host on port over the secure channel. Implies -N, -T, ExitOnForwardFailure and ClearAllForwardings, though these can be overridden in the configuration file or using -o command line options. |
| `-w local_tun[remote_tun]` | Requests tunnel device forwarding with the specified tun devices between the client (local\_tun) and the server (remote\_tun). The devices may be specified by numerical ID or the keyword “any”, which uses the next available tunnel device. If remote\_tun is not specified, it defaults to “any”. If the Tunnel directive is unset, it will be set to the default tunnel mode, which is “point-to-point”. If a different Tunnel forwarding mode it desired, then it should be specified before -w. |
| `-X` | Enables X11 forwarding (GUI Forwarding). |
| `-x` | Disables X11 forwarding (GUI Forwarding). |
| `-Y` | Enables trusted X11 Forwarding. |
| `-y` | Send log information using the syslog system module. By default, this information is sent to stderr. |