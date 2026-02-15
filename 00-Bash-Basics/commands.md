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
-----------------------------------------
- Command: ./script.sh
- Explanation: Runs a script from the current directory.
--------------------------------------------------------
- Command: bash script.sh
- Explanation: Runs a script explicitly using Bash.

---------------------------------------------------

## 3. Variables:
- Command: VAR=value
- Explanation: Creates a variable.
- Syntax: 
-	 	NAME="Thando"
----------------------------------
- Command: echo "$VAR"
- Explanation: Prints a variable value.
- Syntax: 
-	 	echo "$NAME"
---------------------------------------
- Command: export VAR=value
- Explanation: Makes variable available to child processes.
- Syntax: 
-	 	export ENVIRONMENT="production"

-----------------------------------------------------------

## 4. Command Substitution:
- Command: $ (command)
- Explanation: Captures output of a command into a variable.
- Syntax: 
-	 	current_date=$(date)

------------------------------------------------------------

## 5. Input/Output Redirection:
- Command: >
- Explanation: Redirect output (overwrite).
- Syntax: 
-	 	command > file.txt
-------------------------------------------
- Command: >>
- Explanation: Redirect output (append).
- Syntax: 
-	 	command >> file.txt
----------------------------------------
- Command: 2>
- Explanation: Redirect error output.
- Syntax: 
-	 	command 2> errors.txt
-------------------------------------
- Command: |
- Explanation: Pipe output of one command into another.
- Syntax: 
-	 	ps aux | head

--------------------------------------------------------

## 6. Conditionals:
- Command: if [ condition ]
- Explanation: Tests a condition.
- syntax:
<pre>
	if [ -f file.txt ]; then
		echo "File exists"
	fi
</pre>

- Common Tests:
	- '-f' -> file exists.
	- '-d' -> directory exists.
	- '-x' -> executable file.
	- '-z' -> string is empty.
	- '-n' -> string is not empty.

------------------------------

## 7. Loops:
- Command: for
- Explanation: Iterates over a list.
- Syntax:
<pre>
	for user in user1 user2 user3; do
		echo "$user"
	done
</pre>
------------------------------------
- Command: while
- Explanation: Executes while condition is true.
- Syntax: 
<pre>
	while read line; do
		echo "$line"
	done < file.txt
</pre>

------------------------------------------------

## 8. Functions:
- Command: function_name()
- Syntax:
<pre>
	log_info() 
	{
		echo "[INFO] $1"
	}
</pre>

--------------------------------

## 9. Arguments:
- Command: $1, $2 $@
- Explanation: Access script arguments.
- Syntax: 
<pre>
	username="$1"
</pre>
---------------------------------------
- Command: $#
- Explanation: Number of arguments passed.
- Syntax: 
<pre>
	if [ "$#" -ne 1 ]; then
		echo "Usage: ./script.sh <username>"
		exit 1
	fi
</pre>

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

- Report filename pattern:
<pre>
	report_file="system_report_$(date +%F_%H-%M-%S).txt"
</pre>

------------------------------------------------------------

## 11. User Provisioning Building Blocks (Ubuntu/Debian):
### Common commands:
- Check if user exists: id <username>
- Add a sudo user: sudo adduser <username>
- Add a user to a group: sudo usermod -aG <group> <username>
- Change a user's password: sudo passwd <username>
- Show group info: getent group <group>

### Existence Check Pattern:
<pre>
	if id "$username" &>/dev/null; then
		echo "User exists."
	else
		sudo adduser "$username"
	fi
</pre>
