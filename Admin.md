# Administrative Access

There are many Linux commands which deal with sensitive information like passwords, system hardware, or otherwise operate under other exceptional circumstances. Preventing regular users from executing these commands helps to protect the system. Logging in as the root user provides administrative access, allowing for the execution of some of the privileged commands.

### Allows you to temporarily act as a different user

```
su OPTIONS USERNAME
```
### Allows a user to execute a command as another user without creating a new shell

```
sudo [OPTIONS] COMMAND
```
The sudo command only provides administrative access for the execution of the specified command. This is an advantage as it reduces the risk that a user accidentally executes a command as root. The intention to execute a command is clear; the command is executed as root if prefixed with the sudo command. Otherwise, the command is executed as a regular user.

# Permissions

Permissions determine the ways different users can interact with a file or directory.

The output includes permission information
```
ls -l
```

The first character of this output indicates the type of a file. After the file type character, the permissions are displayed.

```
- rw-r--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh
```
* The first set is for the user who owns the file.
* The second set is for the group that owns the file.
* The last set is for everyone else, any one who that first two sets of permissions do not apply to.


## Permission Types

* read (r): Allows for file contents to be read or copied.
* write (w): Allows for contents to be modified or overwritten. Allows for files to be added or removed from a directory.
* execute (x): Allows for a file to be run as a process, although script files require read permission, as well.

## Changing File Permissions

Used to change the permissions of a file or directory. Only the root user or the user who owns the file is able to change the permissions of a file.

```
chmod [<SET><ACTION><PERMISSIONS>]... FILE
```
* SET: which set of permissions is being changed

Symbol|	Meaning
--- | ---
u	   | User: The user who owns the file.
g	   | Group: The group who owns the file.
o	   | Others: Anyone other than the user owner or member of the group owner.
a	   | All: Refers to the user, group and others.

* ACTION: 

Number  | Symbol|	Meaning
--- | --- | ---
1   | +	    | Add the permission, if necessary
2   | =	    | Specify the exact permission
3   | -	    | Remove the permission, if necessary
