# Bash Basics: Commands.
This file contains Bash commands and syntax required to build:
1. System health reporting scripts.
2. User provisioning automation scripts.

All commands are written in general form and can be adapted inside scripts.

---------------------------------------------------------------------------

## 1. Script Structure:
- Command: #!/bin/bash
- Explanation: Shebang line that tells the system to execute the script using Bash.

- Command: set -euo pipefail
- Explanation: Enables strict mode. Stops script on error, undefined variables, and pipeline failures.

------------------------------------------------------------------------------------------------------

## 2. Running and Managing Scripts:
- Command: chmod +x script.sh
- Explanation: Makes a script executable.

- Command: ./script.sh
- Explanation: Runs a script from the current directory.

- Command: bash script.sh
- Explanation: Runs a script explicitly using Bash.

---------------------------------------------------

## 3. Variables:
- Command: VAR=value
- Syntax: 
-	 NAME="Thando"
- Explanation: Creates a variable.

- Command: echo "$VAR"
- Syntax: 
-	 echo "$NAME"
- Explanation: Prints a variable value.

- Command: export VAR=value
- Syntax: 
-	 export ENVIRONMENT="production"
- Explanation: Makes variable available to child processes.

-----------------------------------------------------------

## 4. Command Substitution:
- Command: $ (command)
- Syntax: 
-	 current_date=$(date)
- Explanation: Captures output of a command into a variable.

------------------------------------------------------------

## 5. Input/Output Redirection:
- Command: >
- Syntax: 
-	 command > file.txt
- Explanation: Redirect output (overwrite).

- Command: >>
- Syntax: 
-	 command >> file.txt
- Explanation: Redirect output (append).

- Command: 2>
- Syntax: 
-	 command 2> errors.txt
- Explanation: Redirect error output.

- Command: |
- Syntax: 
-	 ps aux | head
- Explanation: Pipe output of one command into another.

--------------------------------------------------------

## 6. Conditionals:
- Command: if [ condition ]
- syntax: 
-	 if [ -f file.txt ]; then
-	     echo "File exists"
-        fi
- Explanation: Tests a condition.
- Common Tests:
	- '-f' -> file exists.
	- '-d' -> directory exists.
	- '-x' -> executable file.
	- '-z' -> string is empty.
	- '-n' -> string is not empty.

------------------------------

## 7. Loops:
- Command: for
- Syntax: 
-	  for user in user1 user2 user3; do
-		echo "$user"
-	  done
- Explanation: Iterates over a list.


- Command: while
- Syntax: 
-	  while read line; do
- 		echo "$line"
-	  done < file.txt
- Explanation: Executes while condition is true.

------------------------------------------------

## 8. Functions:
- Command: function_name()
- Syntax: 
-	  log_info() {
-		echo "[INFO] $1"
-	  }

--------------------------------

## 9. Arguments:
- Command: $1, $2 $@
- Syntax: 
-	 username="$1"
- Explanation: Access script arguments.


- Command: $#
- Syntax: 
-	  if [ "$#" -ne 1 ]; then
-		echo "Usage: ./script.sh <username>"
-		exit 1
-	  fi
- Explanation: Number of arguments passed.

------------------------------------------

## 10. System Health Reporting Commands:
Used inside reporting scripts:
- hostname
- whoami
- date
- uptime
- df -h
- free -h
- ps aux --sort=-%cpu | head
- systemctl --failed
- journalctl -p err -n 20
