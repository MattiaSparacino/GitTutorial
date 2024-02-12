
# Enhanced Git Tutorial with a Python Calculator Project

Welcome to an enhanced Git tutorial designed to deepen your understanding of version control while working on a Python calculator project. This guide will cover not only the basics but also delve into some intermediate Git concepts, providing a more rounded understanding of branching, merging, stashes, and best practices.

## Prerequisites

- A basic understanding of Python programming.
- Git installed on your local machine. 
- A text editor or Integrated Development Environment (IDE) like VS Code, PyCharm, or Atom.

## Initial Setup

### Creating Your Project Directory

First, let's create a dedicated directory for our project:

```bash
mkdir python_calculator
cd python_calculator
```

### Initializing a Git Repository

Turn this directory into a Git repository to track your project's history:

```bash
git init
```

### Setting Up a Python Virtual Environment (Recommended)

A virtual environment isolates your project's dependencies:

```bash
python3 -m venv venv
# Activate it with:
source venv/bin/activate
```

### Your First Python Script

Create `calculator.py` with a simple addition function:

```python
def add(x, y):
    """Return the addition of x and y."""
    return x + y

# Quick test to verify our function works
print(add(5, 7))
```

### Tracking Your File

Add your script to the staging area and commit it:

```bash
git add calculator.py
git commit -m "Initial commit: Add addition function"
```

## Diving Into Branches

### Creating a Feature Branch

Branches allow you to develop features isolated from the main codebase:

```bash
git checkout -b feature-subtraction
```

### Implementing Subtraction

Enhance `calculator.py` with subtraction function:

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
