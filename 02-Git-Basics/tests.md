## Git Basics Tests:

### Section 1: Version Control Fundamentals.
### Questions:
1. What is Git and how is it different from GitHub?
2. Explain the difference between a working directory, a staging area, and a repository?
3. Why is committing often better that committing once a month?

### Answers:
1. _
- Git is a distributed version control system used to track changes in source code locally.
- GitHub is a cloud platform that hosts Git repositories and allows collaboration, backups, and code sharing.
2. _
- Working directory: where files are edited.
- Staging Area: holds selected changes that are prepared for a commit.
- Repository: stores committed snapshots of the project history.
3. _
- Frequent commits create a clear history, make debugging easier, and reduce the risk of losing work.
- Large sparse commits are harder to review and revert because of the bulk.
-------------------------------------------------------------------------

### Section 2: Commands and Usage.
### Questions:
1. How do you check your current branch or the branch you are currently on?
2. Stage a file and commit it with a message.
3. How do you undo your last commit without losing changes?
4. How do you see commit history?
5. Create a new branch called 'feature-x' and switch to it.

### Answers:
1. _
- git branch
2. _
- git add filename.extension
- git commit -m "Commit message."
3. _
-  git reset --soft HEAD~1
4. _
- git log
- git log --oneline (Optional)
5. _
- git branch feature-x
- git checkout -b feature-x
-------------------------

### Section 3: Collaboration.
### Questions:
1. How do you connect a local repo to a remote repo?
2. How do you fetch and merge changes from the remote?
3. How do you resolve a merge conflict?
4. How do you push a branch to a remote repository?
5. How do you pull a specific branch from a remote?

### Answers:
1. _
- git remote add origin <repository-url>
2. _
- git pull
3. _
- Identify conflicting files, manually edit the conflict marker then add and commit the resolved files.
4. _
- git push origin branch-name
5. _
- git pull origin branch-name
