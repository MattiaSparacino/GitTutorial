Welcome to this comprehensive Git tutorial, where you'll learn the essentials of using Git through the command line while working on a small Python calculator project. By the end of this tutorial, you'll have a solid understanding of basic and intermediate Git operations, including stashes, branches, and merging.

Prerequisites:
- Basic knowledge of Python programming.
- Git installed on your machine.
- A text editor or IDE of your choice.

Setting Up Your Project:

1. Create a New Directory for Your Project
Open your terminal or command prompt and run:

- mkdir python_calculator
- cd python_calculator

2. Initialize a Git Repository

- git init

3. Create a Python Virtual Environment (Optional)

- python -m venv venv

4. Create Your First File
Using your text editor, create a file named calculator.py in your project directory. Add the following Python code:

def add(x, y):
    return x + y

# Test the function
print(add(5, 7))
5. Add and Commit Your File
bash
Copy code
git add calculator.py
git commit -m "Add basic addition function"
Branching Out
1. Create a New Branch
Let's add more functionality, but on a new branch:

bash
Copy code
git branch feature-subtraction
git checkout feature-subtraction
Or, in one command:

bash
Copy code
git checkout -b feature-subtraction
2. Add Subtraction Feature
Edit calculator.py to add a subtraction function:

python
Copy code
def subtract(x, y):
    return x - y

# Test the function
print(subtract(10, 5))
3. Commit Your Changes
bash
Copy code
git add calculator.py
git commit -m "Add subtraction function"
Stashing Changes
Imagine you need to switch branches to work on something else, but you're not ready to commit your current changes. Use git stash:

bash
Copy code
# Make some changes to calculator.py then:
git stash
You can return to your original branch and apply your stashed changes later with:

bash
Copy code
git stash pop
Merging Your Work
Once you're happy with your new feature, merge it into the main branch:

bash
Copy code
git checkout main
git merge feature-subtraction
Resolve any merge conflicts if they arise.

Pushing to a Remote Repository (e.g., GitHub)
1. Create a Repository on GitHub
Go to GitHub and create a new repository.
Do not initialize it with a README, .gitignore, or license.
2. Link Your Local Repository to GitHub
Replace YOUR-REPO-URL with your repository's URL:

bash
Copy code
git remote add origin YOUR-REPO-URL
git branch -M main
git push -u origin main
Conclusion
Congratulations! You've just completed a basic yet comprehensive Git tutorial using a Python calculator project as your context. You've learned how to manage your code with Git, including branching, stashing, and merging changes. These skills are foundational for any software development project, and you're now well-equipped to use Git for your own projects.

For a more visual and interactive experience, consider adding screenshots of your terminal at key steps, or even GIFs showing the commands in action. This tutorial can be expanded with more complex Git operations like rebasing, working with remote repositories, and handling merge conflicts in more detail.


