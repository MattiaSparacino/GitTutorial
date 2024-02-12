
# Enhanced Git Tutorial with a Python Calculator Project

Welcome to this comprehensive Git tutorial, where you'll learn the essentials of using Git through the command line through making a simple Python calculator. By the end of this tutorial, you'll have a good understanding of basic and intermediate Git operations, including stashes, branches, and merging.

## Prerequisites

- A basic understanding of Python programming.
- Git installed on your local machine. 
- A text editor or Integrated Development Environment (IDE) like VS Code, PyCharm, or Atom.

## Initial Setup

### Creating Your Project Directory

First, let's create a  directory for the project:

```bash
mkdir python_calculator
cd python_calculator
```

### Initializing a Git Repository

Turn this directory into a Git repository to track the history:

```bash
git init
```

### Setting Up a Python Virtual Environment 

```bash
python3 -m venv venv
# Activate it with:
source venv/bin/activate
```

###  First Script

Create `calculator.py` with a simple addition function:

```python
def add(x, y):
    """Return the addition of x and y."""
    return x + y

# Quick test to verify it works
print(add(5, 7))
```

### Tracking the File

Add the script to the staging area and commit it:

```bash
git add calculator.py
git commit -m "Initial commit: Add addition function"
```

## Branches

### Creating a Feature Branch

Branches allow you to make features isolated from the main code:

```bash
git checkout -b feature-subtraction
```

### Implementing Subtraction

Make `calculator.py` better with subtraction function:

```python
def subtract(x, y):
    """Return the subtraction of y from x."""
    return x - y

# Testing our new function
print(subtract(10, 5))
```

### Committing Your New Feature

Save your changes to the new branch:

```bash
git add calculator.py
git commit -m "Add subtraction function"
```

## Stashing Your Work

Stashes are useful for saving work-in-progress without committing the actual changes themselves:

```bash
# Assuming you've made changes that aren't ready to commit:
git stash
# Do something else, then come back:
git stash pop
```

## Merging and Conflict Resolution

Merge your feature branch back into the main branch:

```bash
git checkout main
git merge feature-subtraction
```

## Pushing to GitHub

### Setting Up a Remote Repository

1. Create a new repository on GitHub without initializing it.
2. Link your local repository to GitHub:

```bash
git remote add origin <YOUR-REPO-URL>
git branch -M main
git push -u origin main
```

Replace `<YOUR-REPO-URL>` with the URL of your GitHub repository.

## Conclusion

Congratulations on completing this enhanced Git tutorial! You've learned to manage a Python project using Git, covering the creation of repositories, branching, stashing, and merging. 

```
