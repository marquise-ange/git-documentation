# Git and GitHub Documentation

This project provides documentation about Git and GitHub commands, workflows, and collaboration.

1. Initial Partner Contribution
What is it?

An initial partner contribution is the first work added to the shared project by a team member. It establishes the starting point of the project and gives the team a version that can be tracked using Git.

Why is it important?
It creates the first version of the project.
It allows other team members to get the project.
Git records who made the contribution and when.
It provides a starting point for future development.
Example commands
git init
git add .
git commit -m "Initial partner contribution"
git branch -M main
git remote add origin https://github.com/username/repository.git
git push -u origin main
Example contribution

A partner could create:

index.html
style.css
README.md

Then commit:

git add .
git commit -m "Initial partner contribution"
git push
Documentation

The initial contribution represents the first working version of the project. The files are added to Git's staging area and committed to create a permanent record. The commit can then be pushed to GitHub so that other collaborators can access the project.

2. Git Clone & Configuration
What is Git Clone?

git clone is used to create a local copy of a repository that already exists on GitHub or another Git server.

Command
git clone https://github.com/username/repository.git

This downloads the repository, including its files and Git history.

Example
git clone https://github.com/marquise-ange/team-collaboration.git

Then enter the project:

cd team-collaboration
Git Configuration

Before working with Git, you should configure your name and email.

git config --global user.name "Iradukunda Flora"
git config --global user.email "your-email@example.com"

To check the configuration:

git config --global --list
Why configuration is important

Git uses your name and email to identify the person who created each commit.

Documentation

Cloning allows a collaborator to obtain an existing project from GitHub and work on it locally. Git configuration identifies the developer responsible for commits. After cloning and configuring Git, the developer can create branches, modify files, commit changes, and synchronize the work with GitHub.

3. Git Checkout & Switch
What is a branch?

A branch is a separate line of development. It allows developers to work on features without directly changing the main branch.

git checkout

git checkout can be used to switch between branches.

git checkout flora

It can also create and switch to a new branch:

git checkout -b flora
git switch

git switch is the newer and more focused command for changing branches.

git switch flora

Create and switch to a new branch:

git switch -c flora
Check branches
git branch
Example workflow
git switch -c flora

Make changes, then:

git add .
git commit -m "Add Flora's contribution"
Documentation

Branches help collaborators work independently without interfering with the main project. git checkout can switch branches and perform some other operations, while git switch is specifically designed for branch switching. Using separate branches makes collaboration safer and makes it easier to review changes before merging them.