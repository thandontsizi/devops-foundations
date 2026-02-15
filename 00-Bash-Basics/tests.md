# Bash Basics: Tests.

## Instructions:
- Answer in your own words.
- For command questions, write the command exactly.
- For scripting questions, write small code blocks.

---------------------------------------------------

## Section 1: Shell Basics.
1. What is the difference between 'bash script.sh' and './script.sh'?
2. What does 'chmod +x script.sh' do?
3. Write the command to print your current directory.
4. Write the command to list hidden files too.

----------------------------------------------

## Section 2: Variables and Outputs.
1. Create a variable called 'NAME' with value 'your_name' and print it.
2. What is the difference between a normal variable and an exported variable?
3. What does '$?' represent?

----------------------------

## Section 3: Redirection and Pipelines.
1. Write a command that saves the output of 'ls' into 'files.txt' (overwrite).
2. Write a command that appends the output of 'date' to 'logs.txt'.
3. What does '2>' do?
4. Explain what a pipeline '|' does using an example.

-----------------------------------------------------

## Section 4: Conditionals.
1. Write a test that checks if a file called 'report.txt' exists.
2. Write a test that checks if a folder called 'scripts' exists.
3. What does '-f' mean in '[ -f file ]'?
4. What does '-d' mean in '[ -d folder ]'?

------------------------------------------

## Section 5: Loops and Functions.
1. Write a 'for' loop that prints numbers 1 to 5.
2. Write a function called 'log_info' that prints: '[INFO] <message>'.
3. Explain with one reason how functions improve scripts.

---------------------------------------------------------

## Section 6: Scenario-Based Exercises/Questions.
### Scenario 1: System Health Report.
1. You need to generate a system report file named with the current date/time.
	- What variable pattern would you use for the file name?
	- What command would you use to write the first line into the file?
2. List 5 commands you would include in a system health report and say what each one contributes.

### Scenario 2: User Provisioning.
1. You want to create a user if they don't currently exist.
	- What command checks if a user exists?
	- What is a safe conditional pattern for this?
2. You need to add a user to the 'sudo' group. Write the command.
3. A provisioning script should fail fast if something breaks.
	- What strict mode line do you end near the top of the script?

### Scenario 3: Professional Workflow.
1. Write a "usage" block that a script should show if the user runs it incorrectly (just the text, not the code required).
2. In one sentence: why is clear usage output "operational efficiency"?

-----------------------------------------------------------------------

## Section 7: Practical Mini-Builds.
1. Write a tiny script (10-20 lines max) that:
- prints hostname, date, uptime.
- writes output to a timestamped report file.
- ends by printing the file name created.

2. Write a tiny script outline for provisioning:
- checks for username argument,
- checks if user exists,
- creates user if not,
- prints a
