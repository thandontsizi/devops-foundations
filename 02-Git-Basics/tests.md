## Git Basics Tests:

### Section 1: Version Control Fundamentals.
### Questions:
1. What is Git and how is it different from GitHub?
2. Explain the difference between a working directory, a staging area, and a repository?
3. Why is committing often better that committing once a month?

### Answers:
1. ---
Git is a distributed version control system used to track changes in source code locallyy.
GitHub is a cloud platform that hosts Git repositories and allows collacoration, backups, and code sharing.
2. ---
Working directory: where files are edited.
Staging Area: holds selected changes that are prepared for a commit.
Repository: stores committed snapshots of the project history.
3. ---
Frequent commits create a clear history, make debugging easier, and reduce the risk of losing work.
Large sparse commits are harder to review and revert because of the bulk.
-------------------------------------------------------------------------

### Section 2: Commands and Usage.
### Questions:
1. How do you check your current branch or the branch you are currently on?
2. Stage a file and commit it with a message.
3. How do you undo your last commit without losing changes?
4. How do you see commit history?
5. Create a new branch called 'feature-x' and switch to it.

### Answers:
1. ---
git branch
2. ---
git add filename.extension
git commit -m "Commit message."
3. ---
git reset --soft HEAD~1
4. ---
git log
git log --oneline (Optional)
5. ---
git checkout -b feature-x
-------------------------

### Section 3: Collaboration.
### Questions:
1. How do you connect a local repo to a remote repo?
2. How do you fetch and merge changes from the remote?
3. How do you resolve a merge conflict?
4. How do you push a branch to a remote repository?
5. How do you pull a specific branch from a remote?

### Answers:
1. ---
git remote add origin <repository-url>
2. ---
git pull
3. ---
Identify conflicting files, manually edit the conflict marker then add and commit the resolved files.
4. ---
git push origin branch-name
5. ---
git pull origin branch-name
