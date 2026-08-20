# Linux Environment Variables

Environment variables are dynamic values stored by the operating system and shell that provide configuration information to processes and applications.

---

## 1. View Environment Variables with `env`

The `env` command displays the environment variables available to the current shell.

### Command

```bash
env

Purpose:

1.Displays environment variables and their values.
2.Useful for checking the current shell environment.



## 2. View Environment Variables with printenv

printenv displays environment variables.

### Command
printenv


#To display a specific variable:

printenv HOME

Purpose:

1.Displays the value of an environment variable.
2.Can be used to inspect individual variables.


## 3. `echo`

The echo command can be used to display the value of an environment variable.

### Command
echo $HOME

Example:

/home/moin011

The $ tells the shell to substitute the value of the variable.


## 4. Common Environment Variables
$HOME

#Stores the path to the current user's home directory.

echo $HOME
$USER

#Stores the current username.

echo $USER
$SHELL

#Displays the shell being used.

echo $SHELL
$PATH

Contains the directories searched by the shell when executing commands.

echo $PATH
$PWD

Contains the current working directory.

echo $PWD


## 5. Create a Shell Variable

A variable can be created without spaces around the = sign.

MY_VARIABLE="Linux Practical Lab"

Display its value:

echo $MY_VARIABLE

This variable is available in the current shell.



## 6. Export a Variable

The export command makes a shell variable available to child processes.

### Command
export MY_VARIABLE="Linux Practical Lab"

Check the value:

echo $MY_VARIABLE

Check whether it is exported:

printenv MY_VARIABLE


## 7. Remove a Variable

The unset command removes a shell variable.

### Command
unset MY_VARIABLE

Verify:

echo $MY_VARIABLE

The variable will no longer have a value.



## 8. Temporary vs Persistent Variables

A variable created in the current shell is normally temporary.

For example:

export MY_VARIABLE="Linux Practical Lab"

The variable generally exists only for the current shell session and its child processes.

For persistent environment variables, configuration files such as:

~/.bashrc

or system-wide configuration files can be used.



🧪 Basic Workflow

Create variable
      ↓
MY_VARIABLE="Linux Practical Lab"
      ↓
Export variable
      ↓
export MY_VARIABLE
      ↓
Check variable
      ↓
echo $MY_VARIABLE
      ↓
Remove variable
      ↓
unset MY_VARIABLE



