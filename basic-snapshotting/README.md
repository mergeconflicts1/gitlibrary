---
icon: camera-retro
---

# Basic Snapshotting

### Basic Snapshotting: Overview

In Git, basic snapshotting involves capturing the current state of your project at various points in time. This process is crucial for version control, allowing developers to track changes, revert to previous states, and manage the project history effectively. The following commands are essential for basic snapshotting in Git:

#### Adding and Staging Changes

* **`git add`**: This command stages changes in your working directory, preparing them for a commit. It moves files from the working directory to the staging area, allowing you to select specific changes for inclusion in your next commit.

#### Checking Status and Differences

* **`git status`**: Provides detailed information about the current state of your working directory and staging area. It shows which changes have been staged, which have not, and which files are untracked by Git\[1]\[2].
* **`git diff`**: Displays differences between various states of your repository. It can show changes between your working directory and the staging area, or between different commits. This command is essential for reviewing modifications before committing them.

#### Committing Changes

* **`git commit`**: Records a snapshot of the staged changes in your repository's history. Each commit includes a message that describes the changes made, helping maintain a clear project timeline.

#### Managing Notes and Restoring Changes

* **`git notes`**: Allows you to attach additional information to commits without altering them. This is useful for adding metadata or comments that enhance commit messages.
* **`git restore`**: Reverts changes in the working directory or staging area to their last committed state. It provides a safe way to discard unwanted modifications without affecting the commit history.

#### Resetting and Removing Files

* **`git reset`**: Moves the current `HEAD` to a specified commit, adjusting the staging area and/or working directory accordingly. It can be used to undo commits or unstage files\[6].
* **`git rm`**: Removes files from both the working directory and the staging area, ensuring they are no longer tracked by Git. This command helps clean up unnecessary files from your repository.

#### Moving and Renaming Files

* **`git mv`**: Renames or moves files within the repository, updating Git's index automatically. This command simplifies file management by combining file system operations with staging changes.

By mastering these commands, developers can effectively manage their project's snapshots, ensuring that all changes are tracked accurately and that the repository remains organized. These tools are fundamental for maintaining a robust version control system, facilitating collaboration, and preserving project history.

### Learn more about

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="add.md"><strong>add</strong></a></td><td>The <code>git add</code> command is used to stage changes in your working directory for the next commit. By using this command, you can prepare your changes to be recorded in the Git </td><td></td><td><a href="add.md">add.md</a></td></tr><tr><td><a href="status.md"><strong>status</strong></a></td><td>The <code>git status</code> command provides essential information about the current state of the working directory and staging area. </td><td></td><td><a href="status.md">status.md</a></td></tr><tr><td><a href="diff.md"><strong>diff</strong></a></td><td>The <code>git diff</code> command is used to show changes between commits, commit and working tree, etc. It is a versatile command you can use in various scenarios to review code changes.</td><td></td><td><a href="diff.md">diff.md</a></td></tr><tr><td><a href="commit.md"><strong>commit</strong></a></td><td>The <code>git commit</code> command is used to save changes to the local repository. </td><td></td><td><a href="commit.md">commit.md</a></td></tr><tr><td><a href="notes.md"><strong>notes</strong></a></td><td>Git <code>notes</code> is a versatile command that allows you to attach additional information to specific commits without modifying the original commit history.</td><td></td><td><a href="notes.md">notes.md</a></td></tr><tr><td><a href="restore.md"><strong>restore</strong></a></td><td>The <code>git restore</code> command is used to undo changes in the working directory or the staging area.</td><td></td><td><a href="restore.md">restore.md</a></td></tr><tr><td><a href="reset.md"><strong>reset</strong></a></td><td><code>git reset</code> is a powerful command used to undo changes in the repository's history. </td><td></td><td><a href="reset.md">reset.md</a></td></tr><tr><td><a href="rm.md"><strong>rm</strong></a></td><td>The <code>git rm</code> command is used to remove files from the working directory and the staging area.</td><td></td><td><a href="rm.md">rm.md</a></td></tr><tr><td><a href="mv.md"><strong>mv</strong></a></td><td>The <code>git mv</code> command is used for renaming files and moving them from one location to another in a Git repository.</td><td></td><td><a href="mv.md">mv.md</a></td></tr></tbody></table>

