---
layout: page
title: Assignments
---

1. [Enter your GitHub ID here](https://airtable.com/shrC6aW5Pxfra4pL3)
2. Once you've been added, you can access the GitHub classroom [invitation link](https://classroom.github.com/a/2tl5BtAx). 
3. Accept the assignment by accessing the GitHub classroom link provided
  - This will import starter code and create a private repository in your GitHub account
4. Log into Jupyter Hub: https://data.jupyter.brown.edu
5. Setup key using Terminal: `gitconfig -u github-username -n "Your Name" -e your@email.com`. Note that Terminal is one of the things you can launch instead of a notebook when you open a new window. You will be prompted for your GitHub password, and note that the cursor won't move as you type a password in the Terminal. You should see "Hi! You've successfully authenticated, but GitHub does not provide shell access."
6. Clone the repository: on github.com, open your repo and click the green "clone or download" button. Copy that, and in your JupyterHub terminal do `git clone ` and then paste in what you copied from the GitHub page and press enter.
7. Periodically commit changes to GitHub:
  - https://docs.ccv.brown.edu/jupyterhub/git-basics/saving-and-uploading-git-commit-push
8. If changes are made to the starter code, you can get those by merging the upstream repo: `git pull https://github.com/data1010-fall2019/data1010-hw00.git master` (note that this command has to be run from within the repo folder, which looks like `hw00-your-username`. You should `cd` to get into that directory. If you're not familiar with getting around a Unix shell, there is a Data Gymnasia [section on that](https://mathigon.org/course/data-science-utilities/unix)). If there are merge conflicts, [resolve them](https://help.github.com/en/articles/resolving-a-merge-conflict-using-the-command-line) and commit those changes. 
9. Generate a PDF and submit it to [Gradescope](https://www.gradescope.com/courses/56764/) by the deadline (23:00 Friday 06 September). See [this page](/hwsubmit) for more details (in particular, make sure to put `\newline` in a Markdown cell after each problem so that the mapping from pages to problem numbers is a function).