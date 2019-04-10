# Introduction to version control workflow with git and GitHub

`git clone https://github.com/garrettgsb/intro-to-git-workflow.git` to clone this repo
`git log` to look at the log
`git checkout -b my-new-branch` to create a new branch (and check it out)
`git checkout my-old-branch` to check out an existing branch
`git merge master` to merge what's on master into your currently checked-out branch

## Basic workflow

**1) Choose a ticket to work on**

* Navigate to the Issues tab on GitHub
* Assign yourself to an Issue

**2) Get to work**

* `git checkout master` and `git pull` to make sure you're up to date
* Check out a new **feature branch** with the format: My name, ticket number, descriptive branch name
  - e.g. `git checkout -b garrett-6-april-fools-prank-2019`
* Do some coding, committing atomically
* Push to GitHub: `git push` (or, for the first time you push a new branch, copy-pasta the thing it gives you: `git push --set-upstream origin my-branch-name`)

**3) Pull request**

* Go to the relevant GitHub repo
* In the Code tab, click "New pull request"
* Give it a title
* Give it a description that says:
  - Which issue it resolves (GitHub magic: "Resolves #20")
  - What you changed (plain English summary)
  - How to tell that it works (i.e. a testing plan)
* Assign a reviewer (or reviewers)
* Optional: Ping the reviewer on Slack

**4) Code review**

* Navigate to the Pull Request
* Look at the "Files changed," auditing code for:
  - Readability
  - Correctness
  - Style
* Add comments to specific lines
* Click the big green "Review Changes" button, summarize the review, and either Approve, Request Changes, or just Comment
* Optional: Ping the developer on Slack

**5) Merge it in**

* Click the big green Merge button on the Pull Request
* You're done!

**6) Epilogue**

* Now everybody's `master` is out of date
* Everybody needs to:
  - `git checkout master`
  - `git pull`
  - Go back to their own working branch
  - `git merge master`
* Okay now you're really done!
