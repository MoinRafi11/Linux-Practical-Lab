# Linux User Management Commands

This section covers basic Linux commands used to identify users, create and manage user accounts, assign group membership, and remove users.

---

## 1. `whoami`

Displays the username of the currently logged-in user.

### Command

```bash
whoami

Purpose:

1.Shows the current user account.
2.Useful for confirming which account is being used.


## 2. `id`

Displays the user ID (UID), group ID (GID), and group memberships of a user.

### Command

id

To check a specific user:

id username

Purpose:

1.Displays UID and GID information.
2.Shows the groups associated with a user.

## 3. `who`

Displays users currently logged into the system.

### Command

who

Purpose:

1.Shows active login sessions.
2.Displays information such as username, terminal, and login time.


## 4. `adduser`

Creates a new user account.

### Command
sudo adduser username

Purpose:

1.Creates a new user.
2.Creates the user's home directory.
3.Sets a password.
4.Allows additional user information to be configured.


## 5. `passwd`

Changes or sets a user's password.

### Command
sudo passwd username

Purpose:

1.Sets a password for a user.
2.Allows an existing user's password to be changed.


## 6. `usermod`

Modifies an existing user account.

### Add a user to the sudo group

sudo usermod -aG sudo username

Purpose:

1.Modifies user account properties.
2.-a appends the user to a group.
3.-G specifies the supplementary group.


## 7. `groups`

Displays the groups a user belongs to.

### Command
groups username

Purpose:

1.Shows the user's group memberships.
2.Useful for verifying group assignments.


## 8. `userdel`

Deletes a user account.

### Command
sudo userdel -r username

Purpose:

1.Removes the specified user account.
2.The -r option also removes the user's home directory and related files.


## 9. `Verify User Removal`

After deleting a user, its existence can be checked using:

id username

If the user no longer exists, Linux will report that the user cannot be found.

🧪 Practical Usage

These commands were practiced on an Ubuntu Linux virtual machine as part of this Linux Practical Lab.
