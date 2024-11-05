---
icon: code-branch
---

# Branching and Merging

### Branching and Merging: Overview

In Git, branching and merging are essential processes for managing parallel development and integrating changes. This section provides an overview of key commands used in branching and merging workflows.

#### Branch Management

* **`git branch`**: This command is used to list, create, or delete branches. It is a fundamental tool for managing different lines of development within a repository.
* **`git checkout`**: Traditionally used for switching branches, restoring files, and checking out specific commits. However, it can be complex due to its multiple functionalities.
* **`git switch`**: Introduced in Git 2.23, this command simplifies the process of switching branches. It is specifically designed for branch operations, making it safer and more intuitive than `git checkout` for this purpose.

#### Merging Changes

* **`git merge`**: Used to integrate changes from one branch into another. This command combines the histories of branches, resolving conflicts if necessary.
* **`git mergetool`**: Aids in resolving merge conflicts by launching an external tool that helps visualize and resolve differences between conflicting files.

#### Managing Workspaces

* **`git worktree`**: Allows you to check out multiple branches at once by creating additional working directories. This is useful for working on different tasks simultaneously without frequent branch switching.

#### Additional Tools

* **`git log`**: Displays the commit history of a branch. It is essential for reviewing changes and understanding the project's evolution.
* **`git stash`**: Temporarily saves changes in your working directory that are not yet ready to be committed. This is helpful when you need to switch contexts quickly without losing progress.
* **`git tag`**: Marks specific points in the repository's history as important, often used for releases or significant milestones.

These commands collectively enable efficient management of code changes, facilitating collaboration and ensuring a smooth development workflow. By mastering these tools, developers can effectively handle complex branching scenarios and maintain a clean project history.

### Learn more about

<table data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td><a href="branch.md"><strong>branch</strong></a></td><td>The <code>git branch</code> command is a powerful tool in Git for managing branches within a repository.</td><td></td></tr><tr><td><a href="checkout.md"><strong>checkout</strong></a></td><td>The <code>git checkout</code> command is a versatile tool in Git used primarily for switching branches and restoring files.</td><td></td></tr><tr><td><a href="switch.md"><strong>switch</strong></a></td><td>The <code>git switch</code> command was introduced in Git version 2.23 to simplify the process of switching branches by separating it from the <code>git checkout</code> command, which also handles file restoration.</td><td></td></tr><tr><td><a href="merge.md"><strong>merge</strong></a></td><td>The <code>git merge</code> command is a fundamental tool in Git used to combine changes from different branches into a single branch.</td><td></td></tr><tr><td><a href="mergetool.md"><strong>mergetool</strong></a></td><td>The <code>git mergetool</code> command is used to resolve merge conflicts in Git by invoking a merge tool.</td><td></td></tr><tr><td><a href="log.md"><strong>log</strong></a></td><td>The <code>git log</code> command is a powerful tool used to display the commit history of a Git repository.</td><td></td></tr><tr><td><a href="stash.md"><strong>stash</strong></a></td><td>The <code>git stash</code> command is a powerful tool in Git that allows developers to temporarily save changes in their working directory without committing them.</td><td></td></tr><tr><td><a href="tag.md"><strong>tag</strong></a></td><td>The <code>git tag</code> command is a useful feature in Git that allows developers to mark specific points in their project's history as important.</td><td></td></tr><tr><td><a href="worktree.md"><strong>worktree</strong></a></td><td>The <code>git worktree</code> command is a powerful feature in Git that allows developers to check out multiple branches simultaneously within the same repository.</td><td></td></tr></tbody></table>

