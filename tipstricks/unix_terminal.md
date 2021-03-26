# Files
### Search files 
``` javascript By name
find /path-to-search-from -name Filename
```
``` javascript By name, hide errors (-iname for case insensitive search)
find /path-to-search-from -name Filename 2>/dev/null
```

-type d (directories)
-type f (files)
-perm 777 (permissions)
-perm 4000 (SUID bit)
-perm /u=s (SUID bit)
-perm 2644 (SGID bit)
-perm 1551 (Sticky bit)
-perm /a=x (executable files)
! -perm 777 (without permissions)
-exec chmod 644 {} \;  (find files and execute chmod command)
-user root (files belonging to root)
-group developer
-cmin -60 (changed in last hour)
-amin -60 (accessed in last hour)
-size +50M -size -100M


# MISC
### Terminal shortcuts
CTRL+D - exit, sends an EOF marker to bash
CTRL+U - delete everything from cursor to beginning of line
CTRL+Z - put terminal application to background, get back to it with fg command
CTRL+A - move cursor to beginning of the line
CTRL+E - move cursor to end of the line

### Environment variables
printenv – The command prints all or the specified environment variables.
set – The command sets or unsets shell variables. When used without an argument it will print a list of all variables including environment and shell variables, and shell functions.
unset – The command deletes shell and environment variables.


# Processes
pwdx - show working directory of a process
