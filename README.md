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
