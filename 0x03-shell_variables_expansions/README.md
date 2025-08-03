# Create a script that creates an alias. `Name: ls Value: rm *`

```bash
#!/bin/bash
alias ls='rm *'
```

# Create a script that prints hello user, where user is the current Linux user.
```bash
#!/bin/bash
echo "hello $USER"
```

### Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program. `2-path`
```bash
#!/bin/bash
export PATH="$PATH:/action"
```

This script appends `/action` to the end of the `PATH` environment variable.

#### What it does
- Modifies the `PATH` so that `/action` is searched **last** when looking for executables.
- Ensures that it does not override existing entries or break the search order.


### Create a script that counts the number of directories in the PATH. `3-paths`

```bash
#!/bin/bash
echo "$PATH" | tr ':' '\n' | wc -l

```

This script counts how many directory entries exist in the `$PATH` environment variable.

#### What it does
- Prints the number of colon-separated directories currently in `$PATH`.
- Each colon `:` is treated as a separator.
- Even empty entries (e.g. `::::`) are counted as valid path segments.

####  Example
```bash
$ echo $PATH
/usr/local/bin:/usr/bin:/bin
$ . ./3-paths
3
```

### Create a script that lists environment variables. `4-global_variables`
```bash
#!/bin/bash
printenv

```

#### What it does
- Uses the printenv command to display all environment variables.
- Filters out local shell variables and functions.
- Must be sourced or run in a shell session to reflect current environment.

#### Example 
```bash
$ source ./4-global_variables
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
HOME=/home/julien
USER=julien
LANG=en_US.UTF-8
...

```