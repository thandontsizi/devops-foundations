# Practical Tests: Linux Navigation and Inspection.
These questions are meant to simulate what I think might be real workplace scenarios.
Answers explain reasoning, not just commands.

## Test 1:
### Scenario:
You are about to delete files on a remote server.
What command should you run first to confirm your location and why?

### Answer:
I would run pwd to confirm my current working directory.
Deleting files from the wrong directory on remote or production systems can cause data loss or service outages.
Verifying the current path ensures that any destructive command is executed in the intended location only.


## Test 2:
### Scenario:
You need to inspect the contents of a directory without entering it.
Which command do you use, and what risk does it reduce?

### Answer:
I would use ls /path/to/directory.
This allows me to inspect files and directories without changing my working directory.
It reduces the risk of running commands in the wrong location and helps avoid accidental changes to unrelated files.


## Test 3:
### Scenario:
You join a new project with an unfamiliar directory structure.
How can you quickly understand its layout?

### Answer:
I would use tree -L 2 to view the directory structure up to a limited depth.
This provides a high-level overview of how the project is organised without overwhelming output, allowing me to understand where key files and directories are located.


## Test 4:
### Scenario:
You are on a production server with no internet access and you encounter an unfamiliar command.
How do you learn how to use the command safely?

### Answer:
I would use man "command" to read the manual page.
The manual provides accurate information about what the command does, its options, and examples.
This allows me to understand the commanf before using it and avoid unsafe flags or incorrect usage.


## Test 5:
### Scenario:
Why is it dangerous to assume your current directory in operational environments?

### Answer:
Assuming the current directory can lead to runnung commands against the wrong files or systems.
In operational environments +, many commands are directory-sensitive, and a small mistake can affect production data, configuration files, or running services.
Verifying location reduces the risk of human error.
