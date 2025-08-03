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
