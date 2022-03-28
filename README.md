# rebase_fun
Just a repo to explore and demo git rebase

### Amend the last commit
*This is only for changes that have not been pushed to a remote repository*
- Checkout `amend_last_commit`
- Create a new file
- Stage file with add
- Commit new file with a typo in the message
- `git commit --amend`
    - Just update the typo in the message
- Wait, what if I made a simple mistake in this commit and forgot to include a file?
- Create forgotten file 
- Stage forgotten file with add
- `git commit --amend`
    - Update commit and note that the added file is now included in this commit
- Exit out of your text editor and verify the updated history with git log

### Remove a commit
*This is only for changes that have not been pushed to a remote repository*
- Checkout `remove_a_commit`
- `git log --oneline` and note all the commits in the log 
- For example purposes we will choose one of these commits to delete.
- After noting the number of commits we want to target in the rebase:
    - `git rebase -i HEAD~12`
- Looking at interactive mode, we see we have multiple options available to us
- There are 2 ways to remove a particular commit. Either use “drop” or delete the line
- Exit out of your text editor and verify the updated history with git log

### Squash commits
*This is only for changes that have not been pushed to a remote repository*
- Checkout `squash_a_commit`
- `git log --oneline` and note all the commits in the log 
- For example purposes we will choose a few commits to squash together
- After noting the number of commits we want to target in the rebase:
    - `git rebase -i HEAD~12`
- Exit out of your text editor and verify the updated history with git log

### Reorder commits
*This is only for changes that have not been pushed to a remote repository*
- Checkout `reorder_commits`
- `git log --oneline` and note all the commits in the log 
- After noting the number of commits we want to target in the rebase:
    - `git rebase -i HEAD~12`
- Copy and paste the commits into the order you want
- Exit out of your text editor and verify the updated history with git log
