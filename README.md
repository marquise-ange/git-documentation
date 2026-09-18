## 1. What is Git?

Git is a distributed version control system used to track changes in files and manage different versions of a project.

### Why Use Git?

- Tracks changes in a project
- Allows developers to work on different versions
- Makes it possible to restore previous versions
- Supports collaboration between developers


## 2. What is GitHub?

GitHub is a platform that hosts Git repositories online. It allows developers to store, share, review, and collaborate on projects.

### Git vs GitHub

- Git is the version control tool.
- GitHub is an online platform for hosting and collaborating on Git repositories.

---

## 3. Git Repository

A Git repository is a project folder that Git tracks.

### Create a Repository

git init


## 4. Git Status

### Description

"git status" shows the current state of the working directory and staging area.

### Syntax
git status

---

## 7. Git Branches

### Description

A branch is a separate line of development in a Git repository. Branches allow developers to work on features or changes without directly affecting the main branch.

### View Branches

git branch
Create a Branch
git branch feature-login
Switch to a Branch
git switch feature-login
Create and Switch to a New Branch
git switch -c feature-login

Use Case

Branches are useful when different developers need to work on different features at the same time.

8. Git Merge
Description

git merge combines changes from one branch into another branch.

Syntax

git merge <branch-name>
Example

git switch main
git merge feature-login

## 9. Git Remote

### Description

A remote repository is a version of a Git repository hosted on another server, such as GitHub.

### Add a Remote

git remote add origin <repository-url>
View Remotes
git remote -v
Use Case

Use a remote repository to connect your local project to GitHub and share your work with others.

10. Git Push
Description

git push uploads local commits to a remote repository.

Syntax
git push origin <branch-name>
Example
git push origin main
Use Case

Use git push to send your local commits to GitHub.

11. Git Pull
Description

git pull downloads the latest changes from a remote repository and integrates them into the current branch.

Syntax:
git pull origin main

Example:
git switch main
git pull origin main
Use Case

Use git pull to update your local project with the latest changes from GitHub.

 12. Git Fetch

### Description

`git fetch` downloads the latest information from a remote repository without merging the changes into the current branch.

### Syntax

git fetch origin

 13. Merge Conflicts

### Description

A merge conflict happens when Git cannot automatically combine changes from different branches.

### Example

git switch main
git merge feature-branch


14. Undoing Changes

### Description

Git provides commands that allow developers to undo changes when something goes wrong.

### Discard Changes in a File


git restore <file>
