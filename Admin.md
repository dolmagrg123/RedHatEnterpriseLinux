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
- **rw-r--r-- 1** sysadmin sysadmin 647 Dec 20  2017 hello.sh
```



