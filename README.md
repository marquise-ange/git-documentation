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

4. Git Tag
What is a Git tag?

A Git tag is a label attached to a specific commit. Tags are commonly used to identify important versions or releases of a project.

For example:

v1.0.0
v1.1.0
v2.0.0
Create a tag
git tag v1.0.0
View tags
git tag
Push a tag to GitHub
git push origin v1.0.0

Or push all tags:

git push origin --tags
View information about a tag
git show v1.0.0
Annotated tag

A more detailed tag can be created with:

git tag -a v1.0.0 -m "First project release"
Documentation

Git tags provide permanent labels for important points in the project's history. For example, after completing the first version of a project, the team can create v1.0.0. This makes it easy to identify and return to important versions later

5. Git Revert
What is Git Revert?

git revert is used to undo the effect of a previous commit while keeping the existing Git history.

This is particularly useful when a commit has already been pushed to GitHub and should be undone safely.

Find commits
git log --oneline

Example:

abc1234 Add contact page
def5678 Add homepage

To revert the first commit:

git revert abc1234

Git creates a new commit that reverses the changes made by the selected commit.

Example

Suppose you accidentally committed:

Add broken navigation

You can use:

git revert <commit-hash>

Then push:

git push
Revert vs Reset

git revert:

Old commit → New revert commit

The history remains.

git reset can move the branch pointer backward and can be dangerous when used on shared branches.

Documentation

Git revert is useful when a previous change needs to be undone without deleting the project's history. Instead of removing the old commit, Git creates a new commit that reverses its changes. This approach is safer for collaborative repositories because other team members may already have the original commit.

6. Git Cherry-pick
What is Git Cherry-pick?

git cherry-pick allows you to take one specific commit from another branch and apply it to your current branch.

This is useful when you need one particular change but do not want to merge the entire branch.

Find the commit
git log --oneline

Example:

a123456 Add contact form
b789012 Update homepage

Switch to the branch where you want the change:

git switch main

Cherry-pick the required commit:

git cherry-pick a123456
Example

Suppose your partner has:

partner branch
    |
    ├── Add homepage
    ├── Add contact form
    └── Add footer

You only need the contact form.

You can use:

git cherry-pick <contact-form-commit>

You get the contact-form changes without merging the entire partner branch.

If a conflict occurs

Git may stop and ask you to resolve the conflict.

After fixing the files:

git add .
git cherry-pick --continue

To cancel the cherry-pick:

git cherry-pick --abort
Documentation
Cherry-pick is useful in collaborative development when a specific commit from another branch is needed. Instead of merging all changes from the branch, the developer can select and apply only the required commit. This gives developers more control over which changes are introduced into their branch.

7. Git Remote Branches
What is a remote branch?

A remote branch is a branch that exists on a remote repository such as GitHub.

For example:

origin/main
origin/flora
origin/partner

origin normally refers to the GitHub repository from which the project was cloned.

View local branches
git branch
View remote branches
git branch -r
View all branches
git branch -a
Download information about remote branches
git fetch origin

fetch updates your local knowledge of the remote repository without automatically changing your current files.

Create a local branch from a remote branch
git switch -c partner origin/partner
Push a local branch
git push -u origin flora
Documentation

Remote branches allow collaborators to share and access different lines of development on GitHub. Developers can use git fetch to obtain information about changes made remotely, inspect remote branches, and create local branches from them. This is important when multiple team members are working on the same repository.

8. GitHub Issues & Discussions
GitHub Issues
What are Issues?

GitHub Issues are used to track tasks, bugs, improvements, and other work related to a project.

Examples:

Issue #1: Fix navigation menu
Issue #2: Add contact page
Issue #3: Improve mobile responsiveness
Typical Issue information

An issue can contain:

Title
Description
Labels
Assignee
Comments
Status
Example

Title:

Add responsive navigation

Description:

The navigation menu does not display correctly
on small screens. Update the CSS to make it responsive.
Why Issues are useful

They help the team:

Organize tasks
Report bugs
Assign work
Track progress
Discuss solutions
GitHub Discussions

GitHub Discussions are designed for conversations and questions that do not necessarily represent a specific task or bug.

Examples:

Question: Should we use CSS Grid or Flexbox?
Idea: Add a dark mode to the website
General: Project structure discussion
Issues vs Discussions
Issues	Discussions
Track specific work	General conversation
Bugs	Questions
Tasks	Ideas
Feature requests	Community discussion
Work assignments	Sharing knowledge
Documentation

GitHub Issues and Discussions support communication between collaborators. Issues are mainly used to organize actionable work such as bugs and features, while Discussions are useful for questions, ideas, and broader conversations. Using these tools makes project communication more organized and transparent.