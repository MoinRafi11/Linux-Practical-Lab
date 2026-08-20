# Linux File Management Commands

This section covers basic Linux commands used to create, view, copy, move, rename, and delete files.

---

## 1. `touch`

Creates a new empty file.

### Command

```bash
touch filename.txt

Purpose:

1.Creates an empty file.
2.Updates the timestamp if the file already exists.

## 2. `ls`

Lists files and directories.

### Command
ls

Useful options:

ls -l
ls -a
ls -lah

Purpose:

1.-l displays detailed information.
2.-a includes hidden files.
3.-h displays file sizes in a human-readable format.


## 3. `cat`

Displays the contents of a file.

### Command
cat filename.txt

Purpose:

1.Reads and displays file contents directly in the terminal.


## 4. `cp`

Copies files or directories.

# Copy a file
cp source.txt destination.txt

#Copy a directory
cp -r source-directory destination-directory

Purpose:

1.Creates a duplicate of the specified file or directory.


## 5. `mv`

Moves or renames files and directories.

#Rename a file
mv old-name.txt new-name.txt

#Move a file
mv filename.txt directory/

Purpose:

1.Moves files between directories.
2.Can also be used to rename files and directories.


## 6. `rm`

Removes files.

### Command
rm filename.txt

#Remove a directory and its contents
rm -r directory

#Force removal
rm -f filename.txt

Purpose:

1.Deletes files and directories.


## 7. `mkdir`

Creates a directory.

### Command
mkdir directory-name

#Create nested directories
mkdir -p project/linux/commands

Purpose:

1.Creates a new directory.
2.The -p option creates parent directories when necessary.


## 8. `rmdir`

Removes an empty directory.

### Command
rmdir directory-name

Purpose:

1.Removes a directory only when it is empty.


## 9. `file`

Identifies the type of a file.

### Command
file filename

Purpose:

1.Displays information about the type and format of a file.

## 10. find

Searches for files and directories.

### Command
find . -name "filename.txt"

Purpose:

1.Searches recursively from the specified location.

🧪 Practical Usage

These commands were practiced on an Ubuntu Linux virtual machine as part of this Linux Practical Lab.
