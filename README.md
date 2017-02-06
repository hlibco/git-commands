## Clone, Fetch, Merge, Remote, Push

> git clone <remote-path>
Create a copy of a remote Git repository.

> git remote
List remote repositories.

> git remote add <remote-name> <remote-path>
Add a remote repository.
Example: git remote add origin git@github.com:<user>/<repo>.git

> git fetch <remote-name>
Download remote branch information, but do not merge anything.

> git merge <remote-name>/<branch-name>
Merge a remote branch into the checked-out branch.

> git branch -r
List remote branches.

> git push <remote-name> <branch-name>
Push a local branch to another repository.
Example: git push -u origin master

> git push -u origin --all
Push all branches to origin.

> git push <remote-name> <tag-name>
Push a tag to another repository.

---

## Checkout, Revert, Reset, Clean

> git checkout <commit-id>
View a previous commit.

> git revert <commit-id>
Undo the specified commit by applying a new commit.

> git reset --hard
Reset tracked files to match the most recent commit.

> git clean -f
Remove untracked files.

> git reset --hard / git clean -f
Permanently undo uncommitted changes.

---

## Tags

> git tag -a <tag-name> -m "<description>"
Create an annotated tag pointing to the most recent commit.

> git tag -a <tag-name> <commit-id>

> git tag
List tags.

> git tag -l "v1.8.5*"
List tags versions.

> git show <tag-name>
View tag information.

> git push origin <tag-name>
Push tag-name to remote origin.

> git push origin --tags
Push all tags to remote origin.

> git push -u origin --tags
Push all tags to remote origin.

---

## Branch, Merge

> git branch
List all branches.

> git branch <branch-name>
Create a new branch using the current working directory as its base.

> git checkout <branch-name>
Make the working directory and the HEAD match the specified branch.

> git branch -d <branch-name>
Delete branch

> git branch -d -r <branch-name>
Delete branch from local and remote

> git branch -D <branch-name>
Force the removal of an unmerged branch (be careful: it will be lost forever).

> git merge <branch-name>
Merge the branch-name into master

---

## Archive, Bundle, Clone, Bundle, Diff, Reset

> git archive <branch-name> --format=zip --output=<file>
Export a single snapshot to a ZIP archive called <file>.

> git bundle create <file> <branch-name>
Export an entire branch, complete with history, to the specified file.

> git clone repo.bundle <repo-dir> -b <branch-name>
Re-create a project from a bundled repository and checkout <branch‑name>.

> git stash
Temporarily stash changes to create a clean working directory.

> git stash apply
Re-apply stashed changes to the working directory.

> git diff <commit-id>..<commit-id>
View the difference between two commits.

> git diff
View the difference between the working directory and the staging area.

> git diff --cached
View the difference between the staging area and the most recent commit.

> git reset HEAD <file>
Unstage a file, but don’t alter the working directory or move the current branch.

---

## Rebase, commit, merge

> git rebase <new-base>
Move the current branch’s commits to the tip of <new-base>, which can be either a branch name or a commit ID.

> git rebase -i <new-base>
Perform an interactive rebase and select actions for each commit.

> git commit --amend
Add staged changes to the most recent commit instead of creating a new one.

> git rebase --continue
Continue a rebase after amending a commit.

> git rebase --abort
Abandon the current interactive rebase and return the repository to its former state.

> git merge --no-ff <branch-name>
Force a merge commit even if Git could do a fast-forward merge.
