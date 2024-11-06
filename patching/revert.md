# revert

The `git revert` command is a crucial tool in Git for safely undoing changes by creating new commits that reverse the effects of earlier commits. This command is particularly useful when you need to undo changes in a way that preserves the history and integrity of the project, making it ideal for use in collaborative environments. Below is a detailed explanation of the `git revert` command, its commonly used options, and practical examples.

### Basic Explanation

The `git revert` command is used to reverse the changes introduced by a specific commit. Instead of removing the commit from the history, it creates a new commit that undoes the changes made by the original commit. This ensures that the project's history remains intact and traceable, which is important for collaboration and maintaining a clear record of changes.

### Commonly Used Options

* **`--no-edit`**: Prevents Git from opening an editor to modify the default commit message when reverting. The default message includes information about which commit was reverted.
* **`-n` or `--no-commit`**: Applies the revert without automatically committing it. This option allows you to review and possibly modify the changes before committing them.
* **`-m <parent-number>`**: Used when reverting a merge commit. It specifies which parent should be considered the mainline, allowing Git to determine how to apply the revert.
* **`--edit`**: Opens an editor to modify the commit message before completing the revert. This is the default behavior if run from a terminal.

### Example Usage

#### Reverting a Single Commit

To revert a specific commit:

```bash
git revert <commit-hash>
```

Replace `<commit-hash>` with the hash of the commit you want to revert. This creates a new commit that undoes the changes introduced by that specific commit.

#### Reverting Without Committing

If you want to apply a revert but not immediately commit it:

```bash
git revert --no-commit <commit-hash>
```

This leaves the reverted changes in your working directory, allowing you to review or modify them before committing.

#### Reverting Multiple Commits

To revert a range of commits:

```bash
git revert <start-commit>..<end-commit>
```

This reverts all commits from `<start-commit>` (exclusive) to `<end-commit>` (inclusive), creating separate revert commits for each.

#### Reverting a Merge Commit

When dealing with merge commits, specify which parent should be considered:

```bash
git revert -m 1 <merge-commit-hash>
```

Here, `1` indicates that you want to keep changes from the first parent branch and revert changes from the other.

#### Practical Scenario

Imagine you've pushed several commits to a shared branch and later discover that one of them introduced a bug. Instead of using `git reset`, which could disrupt others' work, you use `git revert`:

1. Identify the faulty commit using `git log`.
2.  Run:

    ```bash
    git revert <faulty-commit-hash>
    ```
3.  Push the new revert commit:

    ```bash
    git push origin <branch-name>
    ```

By using `git revert`, you maintain a clear history and ensure that collaborators can easily pull updates without conflicts or confusion.

These examples illustrate how `git revert` can be effectively used to manage changes in your Git repository while preserving project history and facilitating collaboration.
