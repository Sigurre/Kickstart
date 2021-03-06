# Module 1.2 - Git

Git is the most widely used SCM (Source Control Manager) in the industry. It's used primarily as a way for groups of developers to collaborate and organize their code in a variety of ways, and you'll need to have a basic understanding of how to use it to succeed. But first, an important distinction:

**Git** is the name of the tool/program, and it utilizes a structure known as a **repository** (repo for short). A repo serves as a central collection of code which is typically hosted on a centralized server. You can have a local Git repo that never leaves your machine, but typically a company or group will host their repo on their own hardware or with a 3rd party. Two common hosts are **Bitbucket** and **GitHub** (GH), with the latter being the most popular. That's what we're using for this project!

A very brief overview of how Git works:

* There's typically one central "branch". Traditionally this is called `main`, although you may see some older projects that use the name `master`. The term `master` has been abandoned due to its racist roots, but you'll still come across some projects that still use it due to structural/technical reasons.
* When someone wants to make a change to the codebase they will `checkout` a branch from `main`, make their changes, and then `commit` them to their local branch.
* They can then `push` their changes to the host repo, either directly to `main` or they'll `push` their branch to the repo and open a "Pull Request" (PR). 
	* Most organizations require a Pull Request to `merge` your change in to `main`, usually with the approval of a peer or a "codeowner"/admin.
	* Many organizations also have a suite of automated tests that are required to pass on these changes to ensure stability. This is known as CI/CD (Continuous Integration/Continuous Development), and is what DevOps Engineers like myself work with.
	* Once the PR is approved they will then `merge` their branch in to `main` and the change will be reflected on any new pulls on the repo.

## INFO: How this repo works

This repo is protected, and requires a PR with an approval in order to merge it in to `main`. This means you can't make a change with `main` checked out on your local machine, then push directly to the repo. You *can* however make your own branch and then `push` it to GitHub. This can be a handy way to save and publish your work, but it's also how you'll submit your code to the project.

The typical workflow you'll want to follow when submitting your code to the `main` branch of this repo:

1. Make a branch on your local machine off of `main`.
2. Make changes and `commit` them.
3. Push your branch to GH, then open a Pull Request and ask me for review via the GH UI.
4. If changes are requested you'll make them on your local machine on your branch, `commit` them, then `push` to your branch on GH.
5. Once your change is approved you will `merge` your branch in to `main`.

You'll only need to do this a few times throughout the project for practice. The rest of the time you can keep your code on a "personal branch". You can `push` any of your changes to this branch at will without the need for a pull request, and request code reviews at your discretion when you'd like feedback.

1. Go to the root of the repo on your machine and switch to `main` by running `git checkout main`
2. Make sure it's up to date with `git pull`
3. Make a new branch that you'll use for your work throughout the project by running `git branch`. I'll be using "sig" as my branch name: `git branch sig`
4. Switch to the new branch with `git checkout`, ie: `git checkout sig`
5. Make a new file in the Module 1.2 folder. I'll be using the traditional "Hello World": `cd Module_1/1.2_Git; touch HelloWorld.txt`
6. Add the file to Git via `git add` (Note: you can add all changed files from your current directory down to the subdirectories by appending a `.` instead of the filename), ie: `git add .`
7. Commit your change with `git commit -m` followed by a comment in quotes, like: `git commit -m "Initial commit to my personal branch"`. All commits require a message attached to them.
8. Now we can push the branch to GH by setting its upstream origin branch: `git push --set-upstream origin sig`
9. Now whenever you make a change on this branch you can commit and push them up to the branch on GH: `git add .` -> `git commit -m "message"` -> `git push`

I recommend commiting fairly frequently, and pushing whenever you have some "finalized" changes. Not only will this help save your work, but you can easily revert a specific commit while keeping everything else in tact. For example, lets say I made the following changes to a folder on my branch (and made a separate commit for each one) in this order:

* File 1 -> Added 8 lines -> commit 001
* File 2 -> Deleted 2 lines -> commit 002
* File 3 -> Deleted File -> commit 003
* File 4 -> Created file, added 27 lines -> commit 004

Then I pushed them to the upstream branch on GH... and realized "uh oh, I shouldn't have deleted those two lines in File 2". Instead of having to completely revert all the changes in the push I made (or manually adding the two lines back in) I can instead `revert` commit 002 and push that to GH, while preserving the changes in the other commits.

# TASK 1

Alright let's get down to business... Create a new branch using the personal one you created in the Info section as the base branch, then accomplish the following:

* Create a new file with some text in it, commit it to the newly created branch, and push the branch to GH.
* Create another file with some text and push it to the same branch on GH
* Create a folder named `1.2.1` with 3 empty files in it and push it to the same branch on GH
* Add some text to one of the files in the folder, but don't push it yet!
* Remove the second file you pushed to the branch on GH via a revert commit
* Push all of your changes to the branch
* Lastly, add or remove some text in the first file you created and commit/push to GH

After doing this you should have a branch on GH that is based off your personal branch, with 1 file with some text in it that you edited one time as well as a folder with 2 empty files and 1 non-empty file in it.

Finally, merge your changes so that they appear in your personal branch on GH.

# TASK 2

As I mentioned, this will be one of the few (if not the only) time you'll open a PR to send to `main`. 

Make a PR against `main` that adds a file called `PRTest.txt` to the module folder with "Lorem ipsum" as the contents, then request review from me (Sigurre). I'll make a request for change. Once the change has been approved on GH you'll merge it in to `main`.

# TASK 3

You'll frequently come across a situation where the `main` branch has had oodles of changes merged in to it by other people since you first checked it out, and now your branch is behind. There are several ways to resolve this, but the best and most common way is with `git rebase`. Accomplish the following:

* Create two branches with your personal branch as the base
* Create 3 or more commits on the first branch, then make two different changes on the second branch
* Merge the first branch onto your personal branch
* Rebase the second branch onto your personal branch, then merge it in to your personal branch

NOTE: Rebasing can be a little hard to wrap your head around, even though it's deceptively simple. Consider requesting my review via a PR on the second branch to help explain things if you're at all confused.

# TASK 4

There are. afew file types associated with Git that you'll come across. Take some time to read up on what the `.gitignore`, `.gitconfig`, and `.gitattributes`are for.

# Resources

There's a lot of stuff that Git can do, and even though it's conceptually simple it's complicated in practice. When in doubt, refer to the [Git documentation](https://git-scm.com/doc) as well as [GitHub's docs](https://docs.github.com/en).

A dead simple overview of how Git works can be found at [git - the simple guide](https://rogerdudler.github.io/git-guide/)
