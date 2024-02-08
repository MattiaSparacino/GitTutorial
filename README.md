Comprehensive Git Tutorial for CS Students:

Introduction:

This tutorial is crafted for computer science students embarking on the journey of understanding and utilizing Git, the cornerstone of modern version control systems. By integrating a small coding project, this guide aims not only to teach the commands but also to provide a context for their application, ensuring students are well-equipped to use Git in their future projects.

Prerequisites:

Before we begin, ensure you have:

- Git is installed on your computer

Installation guides for different operating systems can be found at Git's official site:
- A basic understanding of the command line interface (CLI).
- A text editor (VSCode, Sublime Text, Atom, etc.) installed.
- Setting Up Your First Git Repository
- Installation Check and Configuration

First, verify that Git is correctly installed and then configure your user information.

Verify Installation: Open your terminal or command prompt and type:

bash
Copy code
git --version
This command should return the installed Git version, confirming its installation.

Configure User Information: Git uses a username and email to associate commits with an identity. Set your username and email using the following commands:

bash
Copy code
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
Creating and Initializing a New Repository
Creating a repository (repo) is the first step to tracking your project with Git.

Create a Project Directory: Choose a location on your computer and create a new directory for your project:

bash
Copy code
mkdir my_git_project
cd my_git_project
Initialize the Repository: Turn this directory into a Git repository by running:

bash
Copy code
git init
This command creates a hidden .git directory, where Git begins tracking changes.

Your First Commit
Commits are snapshots of your project, capturing the current state of the code.

Create a Simple Program: Let's start with a "Hello, World!" script. Create a file named hello_world.py (or another language file) and write:

python
Copy code
print("Hello, World!")
Stage the File: Before committing, you need to stage changes. Add your file to the staging area with:

bash
Copy code
git add hello_world.py
Commit the Changes: Now, commit your staged changes to the repository:

bash
Copy code
git commit -m "Initial commit"
The -m flag allows you to add a commit message inline.

Branching Out
Understanding Branches
Branches are a powerful feature in Git, enabling parallel lines of development without affecting the main codebase.

Creating and Switching Branches
Branches allow you to work on new features or fixes in isolation.

Create a New Branch: To create a branch named feature-greeting, use:

bash
Copy code
git branch feature-greeting
Switch to the New Branch: Change your working directory to the new branch with:

bash
Copy code
git checkout feature-greeting
Alternatively, create and switch in one command:

bash
Copy code
git checkout -b feature-greeting
Enhancing Your Project in a Branch
Let's add a new feature in this branch.

Modify Your Program: Update hello_world.py to ask for the user's name and then greet them.

Stage and Commit Changes: After making changes, stage and commit them:

bash
Copy code
git add hello_world.py
git commit -m "Add personalized greeting feature"
Stashing Your Work
The Purpose of Stashing
Stashing temporarily shelves changes, allowing you to switch contexts without committing half-done work.

How to Stash Changes
Make Preliminary Changes: Suppose you've started work but need to switch branches. You have changes not ready to commit.

Stash Your Changes: Save your work in progress:

bash
Copy code
git stash push -m "WIP: Adding user input"
List and Apply Stashes: To see your stashed changes:

bash
Copy code
git stash list
Apply the most recent stash:

bash
Copy code
git stash pop
Merging and Rebasing
Merging Explained
Merging is how you integrate changes from one branch into another.

Performing a Merge
Switch to the Main Branch: Ensure you're on the branch that will receive the changes:

bash
Copy code
git checkout main
Merge Your Feature Branch: Bring the changes from feature-greeting into main:

bash
Copy code
git merge feature-greeting
Resolve Conflicts: If there are conflicts, Git will alert you. Open the conflicting files, resolve the differences, and then commit.

Rebasing Explained
Rebasing is an alternative to merging, offering a way to integrate changes by reapplying commits on top of another base.

Performing a Rebase
Switch to Your Feature Branch: If not already there:

bash
Copy code
git checkout feature-greeting
Rebase onto Main: Apply your branch's commits onto the main branch:

bash
Copy code
git rebase main
Resolve Conflicts: Similar to merging, resolve any conflicts that arise during the rebase, then continue with git rebase --continue.

Conclusion
You've now navigated through the foundational aspects of Git, from basic setup and commits to advanced branching, stashing, and merging/rebasing strategies. This knowledge equips you to manage your projects with version control effectively, a critical skill in software development.

Additional Resources
To further enhance your understanding and skills in Git, explore:

Pro Git Book - An in-depth book on Git.
Git Documentation - The official Git documentation.
Interactive Git Branching Tutorial - A fun, interactive way to learn about Git's branching features.
Remember, mastery comes with practice. Use Git in your daily coding activities to solidify your understanding and discover more advanced features and workflows.
