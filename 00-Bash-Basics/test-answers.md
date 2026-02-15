# Bash Basics: Test Questions.

## Section  1: Shell Basics.
1. Difference between 'bash script.sh' and './script.sh':
- 'bash script.sh' runs the script by explicitly calling Bash.
- './script.sh' runs the script as an executable file, which requires execute permissions and relies on the shebang (e.g., '#!/usr/bin/env bash') to choose the interpreter.

2. What 'chmod +x script.sh' does:
- Adds execute permission so the script can be run like a program using './script.sh'.

3. Command to print current directory:
- pwd (Print Working Directory).

4. Command to list all files including hidden ones:
- ls -a or ls -la.
------------------

## Section 2: Variables and Output.
1. Create variable that stores name and one that prints it:
- NAME="Thando".
- echo "$NAME"

2. Normal vs Exported Variables:
- A normal variable exists only in the current shell.
- An exported variable becomes an environment variable and is available to child processes (programs/scripts launched from the shell).

3. What '$?' represents:
- The exit status code of the last command (0 = success, non-zero = failure).
-----------------------------------------------------------------------------

## Section 3: Redirextion and Pipelines.
1. Save output of ls into files.txt (overwrite):
- ls > files.txt

2. Append output of date to logs.txt:
- date >> logs.txt

3. What 2> does:
- Redirects error output (stderr) to a file.

4. What a pipeline (|) does using an example:
- A pipeline sends the output (stdout) of one command as input to another.
- Example:
<pre> 
	ps aux | head
</pre>
- 'ps aux' outputs processes, and 'head' shows only the first few lines.
------------------------------------------------------------------------

## Section 4: Conditions.
1. Test if 'report.txt' exists:
- [ -f report.txt ]

2. Test if 'scripts' folder exists:
- [ -d scripts ]

3. Meaning of '-f' in '[ -f file ]:
- Explicitly used to check if files are regular and if the exist in their paths.

4. Meaning of '-d' in '[ -d folder ]:
- True if path exists and is a directory.
-----------------------------------------

## Section 5: Loops and Functions.
1. For loop printing from 1 to 5:
<pre>
	for i in 1 2 3 4 5; do
		echo "$i"
	done
</pre>

2. Function 'log_info()' printing '[INFO]:
<pre>
	log_info ()
	{
		echo "[INFO] $1"
	}
</pre>

3. One reason functions improve scripts:
- They reduce repetition and make scripts easier to read, reuse, and mantain.
-----------------------------------------------------------------------------

## Section 6: Scenario-based Questions.
### Scenario 1: System health report.
1. Filename pattern + first line into file command:
- Filename pattern:
<pre> report_file="system_report_$(date +%F_%H-%M-%S).txt" </pre>
- Write first line into the file:
<pre> echo "System Report - $(date)" > report_file" </pre>

2. Five commands to include in a system health report + their contribution:
- 'hostname': identifies which machine the report came from.
- 'date': timestamp of when the report was generated.
- 'uptime': shows how long the system has been running and load averages.
- 'df -h': shows disk usage to spot low disk space problems.
- 'free -h': shows memory usage to spot memory pressure or low RAM.
-------------------------------------------------------------------

### Scenario 2: User Provisioning.
1. Check whether a user exists + safe conditional pattern:
- Command: id username
- Safe consitional pattern:
<pre>
	if id "$username" &>/dev/null; then
		echo "User exists: $username"
	else
		sudo adduser "$username"
	fi
</pre>

2. Add user to the sudo group:
- Command: sudo usermod -aG sudo "$username"

3. Strict mode line near top of script:
- Command: set -euo pipefail
----------------------------

### Scenario 3: Professional Workflow.
1. Usage block text:
- Usage: ./user_provision.sh
- Description: Creates a new user if it does not exist and optionally adds the user to a group.
- Example: ./user_provision.sh thando

2. Why cleaner usage output is operational efficiency:
- Clear usage output reduces mistakes and saves time by showing the correct inputs immediately without needing troubleshooting.
-------------------------------------------------------------------------------------------------------------------------------

## Section 7: Practical Mini-Builds.
1. Tiny script (10-20 line max):
<pre>
	#!usr/bin/env bash
	set -euo pipefail

	report_file="system_report_$(date) +%F_%H-%M-%S).txt"
	
	echo "System Report - $(date)" > "$report_file"
	echo "Hostname: $(hostname)" >> "$report_file"
	echo "Uptime: $(uptime)" >> "$report_file"

	echo "Created Report: $report_file"
</pre>

2. Tiny provisioning script outline (argument check, user existence, create if not, success message):
<pre>
	#!usr/bin/env bash
	set -euo pipefail

	if [ "$#" -ne 1 ]; then
		echo "Usage: ./user_provision.sh <username>"
		exit 1
	fi

	username="$1"

	if id "$username" &>/dev/null; then
		echo "User already exists: $username"
	else
		sudo adduser "$username"
		echo "User created successfully: $username"
	fi
</pre>
