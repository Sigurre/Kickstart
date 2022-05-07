# Module 1.2 Tidbits

As you've seen, the capabilities of `git` are pretty robust, and also a bit complicated when working with it. Practice makes perfect in this case, so I recommend utilizing this repo to practice as much as paossible. As usual, I'm gonna walk through how I would approach the tasks assigned in this submodule.

# TASK 1

You'll be using a lot of the same commands in a row here, namely `add`, `commit`, and `push`.

First you'll create a new branch off of your personal one:

```
#Switch to your personal branch
git checkout personal
git pull # It's always good practice to pull to make sure you're up to date
# Now create a new branch.
git branch mod1
git checkout mod1
#you can also run `git checkout -b mod1` to do both of those commands in one!
```
Once you've made your changes you'll add it to the working tree, make a commit, then push it to the remote (for the first push to GH you'll need to set the upstream origin)

```
# You can either put a specific file name, or put a "." to indicate " everything that's here"
git add .
#The -m argument lets you add a message in the "Commit message"command, otherwise it will open your text editor to make a message
git commit -m 
#Set our upstream origin since it's the first push
git push --set-upstream origin mod1
```
You'll then follow similar steps for your second commit.

```
git add .
git commit -m "Message"
git push
```

Next up we're adding a file and a commit to our local branch, but not pushing it to the remote yet.

```
git add .
git commit -m "Message"
```
You'll need to the commit hash to identify which commit you want to revert. You can either get it directly from GH, or by using `git log`. If you're reverting a commit that is *only* on your local branch, you'll have to use the latter method.

```
git log
# you'll see a list of commits, and each one will have a long hash at the top
# HEAD indicates where the "top" of the branch is
git revert 15b0ffec0e8a25039f42814fdc79e945af13ff1f
# If for whatever reason you need to reset everything you can use `git-reset`
git push
```

Once you're ready to merge everything into your personal branch you'll switch to it, then use `git merge` to merge your working branch onto it

```
git checkout personal
git pull
git merge mod1
# Push to GH if you want to track the change on the remote
git push
```

# TASK 2

You can either make a new branch off of `main` for the Pull Request (PR), or you can use your personal branch. Keep in mind though that if you open a PR with your personal branch you'll be requesting to merge in *all* of the changes on that branch.

```
git checkout main
git pull
git checkout -b task2
# After you've made PRTest.txt
git add .
git commit -m "Message"
git push --set-upstream origin task2
# Then go to GH and navigate to your branch.
# When viewing a branch you'll get the option to open a PR
```

Once I've reviewed and requested a change you can make it on your local branch, then commit and push

```
# After you've made the change
git add .
git commit -m "Message"
git push
```
Once it's approved you'll merge it via the GH website.

# TASK 3

Rebasing can be a bit cumbersome, especially since you'll have to resolve conflicting changes in files that someone else may have made. Again, this will get easier with practice. For this exercise though we're trying to keep it simple.

```
git checkout personal
git pull
git branch branch1
git branch branch2
git checkout branch1
# Make 3 different changes + commits on branch1
git checkout branch2
# Make two different changes on the second branch
# If you make them in files separate from the changes in the first branch
# it'll make the rebase easier, since there won't be conflicts
# If you decide to make changes in the same files you'll be asked 
# to resolve the conflicts during rebase. Feel free to give a try to see what it's like!
git checkout personal
git merge branch1
# Now we'll checkout branch2 and rebase personal onto it
# This will "fast forward" branch2 to catch up with personal
git checkout branch2
git rebase personal
## Resolve any conflicts, then switch to personal and merge
git checkout personal
git merge branch2
```
