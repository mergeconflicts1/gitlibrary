---
icon: camera-retro
---

# Basic Snapshotting

## Basic Snapshotting

Snapshotting in Git involves capturing the state of your project at a specific point in time. This is an essential feature of Git as it allows you to record changes and revert back to previous states when necessary. Below, we summarize what each command does in the context of snapshotting:

* **git add**: Stages changes in your working directory for the next commit, allowing you to decide what changes you want to snapshot.
* **git status**: Displays the status of your working directory and staging area, showing what changes have been staged or are yet to be staged.
* **git diff**: Shows the differences between changes in your working directory and the staging area, or between commits, helping review what you're about to commit.
* **git commit**: Records a snapshot of the changes in the staging area to the repository, creating a new commit in the history.
* **git notes**: Allows you to add or inspect notes attached to objects, useful for adding annotations without altering commits directly.
* **git restore**: Aids in restoring working tree files, undoing changes to either specific files or the entire tree from a commit or staging area.
* **git reset**: Undoes changes in your working directory and can move the HEAD to a specified commit, effectively altering commit history.
* **git rm**: Removes files from your working directory and stages the removal for the next commit, effectively taking them out of the snapshot.
* **git mv**: Moves or renames files in your working directory and stages both the removal of the old path and addition of the new path for the next commit.

By mastering these commands, you can effectively manage snapshots of your project, maintaining a clean and efficient version history.

### Learn more about

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="add.md"><strong>add</strong></a></td><td>The <code>git add</code> command is used to stage changes in your working directory for the next commit. By using this command, you can prepare your changes to be recorded in the Git </td><td></td><td><a href="add.md">add.md</a></td></tr><tr><td><a href="status.md"><strong>status</strong></a></td><td>The <code>git status</code> command provides essential information about the current state of the working directory and staging area. </td><td></td><td><a href="status.md">status.md</a></td></tr><tr><td><a href="diff.md"><strong>diff</strong></a></td><td>The <code>git diff</code> command is used to show changes between commits, commit and working tree, etc. It is a versatile command you can use in various scenarios to review code changes.</td><td></td><td><a href="diff.md">diff.md</a></td></tr><tr><td><a href="commit.md"><strong>commit</strong></a></td><td>The <code>git commit</code> command is used to save changes to the local repository. </td><td></td><td><a href="commit.md">commit.md</a></td></tr><tr><td><a href="notes.md"><strong>notes</strong></a></td><td>Git <code>notes</code> is a versatile command that allows you to attach additional information to specific commits without modifying the original commit history.</td><td></td><td><a href="notes.md">notes.md</a></td></tr><tr><td><a href="restore.md"><strong>restore</strong></a></td><td>The <code>git restore</code> command is used to undo changes in the working directory or the staging area.</td><td></td><td><a href="restore.md">restore.md</a></td></tr><tr><td><a href="reset.md"><strong>reset</strong></a></td><td><code>git reset</code> is a powerful command used to undo changes in the repository's history. </td><td></td><td><a href="reset.md">reset.md</a></td></tr><tr><td><a href="rm.md"><strong>rm</strong></a></td><td>The <code>git rm</code> command is used to remove files from the working directory and the staging area.</td><td></td><td><a href="rm.md">rm.md</a></td></tr><tr><td><a href="mv.md"><strong>mv</strong></a></td><td>The <code>git mv</code> command is used for renaming files and moving them from one location to another in a Git repository.</td><td></td><td><a href="mv.md">mv.md</a></td></tr></tbody></table>

