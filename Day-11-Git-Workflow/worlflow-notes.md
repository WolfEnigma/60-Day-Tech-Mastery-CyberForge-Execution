## What does `git status` show?

`git status` displays the current state of your working directory and staging area. It shows which files have been modified, which files are staged for commit, which files are untracked, and what branch you're currently on.

## Difference between `git add` and `git commit`

`git add` stages changes, moving files from your working directory to the staging area (preparing them for commit). `git commit` takes all staged changes and saves them as a permanent snapshot in your repository's history with a descriptive message.

**Simple analogy:** `git add` is like putting items in a shopping cart, `git commit` is like completing the purchase.

## Why `git pull --rebase` is safer

`git pull --rebase` replays your local commits on top of the remote changes, creating a linear history without merge commits. This is safer because it avoids unnecessary merge conflicts, keeps the commit history clean and readable, and makes it easier to understand the project timeline and revert changes if needed.

**Standard `git pull`** creates a merge commit, which can clutter history. **`git pull --rebase`** integrates changes smoothly without the extra merge noise.

## What happens if I push without pulling

If you push without pulling first and someone else has pushed changes to the same branch, Git will **reject your push** with an error message like "Updates were rejected because the remote contains work that you do not have locally."

**Consequences:**
- Your push fails and is not accepted by the remote repository
- You must first pull the remote changes to integrate them with your local work
- If conflicts exist between your changes and the remote changes, you'll need to resolve them manually
- Only after pulling and resolving conflicts can you successfully push


