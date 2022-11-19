# Bash

## How to create lockfile in bash script

```bash
#!/bin/bash
# Prevent running more than one process with lockfile
 if { set -C; 2>/dev/null >~/mariadb-backup.lock; }; then
         trap "rm -f ~/mariadb-backup.lock" EXIT
 else
         echo "[ERROR] Another backup process is running...
               you can not run more than one process at the same time
               exciting..."
         exit
 fi
```

## How to check bash Error in script and exit from script

```bash
#!/bin/bash

# Handle error
function in_case_fail {
    local lineno=$1
    local msg=$2
    echo "[ERROR] Failed at line: $lineno: $msg"
    echo "[ERROR] Stopping Script..."
    exit 200
  }
trap 'in_case_fail ${LINENO} "$BASH_COMMAND"' ERR

# test it 
touch test1.txt # correct command
touccccch test2.txt # the incorrect command which trigger the trap and exited the script

```