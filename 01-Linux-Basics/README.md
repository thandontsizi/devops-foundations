# Linux Basics: Navigation and Inspection.

This section covers foundational Linux commands used to safely navigate and inspect a system.
These commands are used daily in DevOps, cloud support, and IT operations roles.

## 1. pwd:
**What it does:**
Prints the current working directory.

**Why it matters in real working systems:**
Before running any command that modifies files, it is crucial to know exactly where you are.
Running commands in the wrong directory can cause data loss or service outages.

**Common mistake:**
Assuming your location instead of checking it.


## 2. ls:
**What it does:**
Lists files and directories.

**Why it matters in real working systems:**
Used to confirm the presence of configuration files, logs, scripts, or deployment artifacts before interacting with them.

**Common mistake:**
Using destructive commands without first inspecting directory contents.

## 3. cd:
**What it does:**
Changes the current directory.

**Why it matters in real working systems:**
Most administrative actions are directory-sensitive.
Being in the wrong directory while running commands can impact the wrong system or application.

**Common mistake:**
Moving into directories without confirming permissions or contents.

## 4. tree:
**What it does:**
Displays a directory structure as a tree.

**Why it matters in real working systems:**
Allows fast understanding of unfamiliar projects, applications, or configuration layouts without manually exploring each directory.

**Common mistake:**
Running tree on very large directories without limiting depth.

## 5. man:
**What it does:**
Displays the manual page for a command.

**Why it matters in real working systems:**
On production servers, internet access is often restricted.
Manual pages are the primary source of accurate command usage.

**Common mistake:**
Copying commands from the internet without understanding flags or behaviour.
