# reset

### Git Reset: Basic Explanation

`git reset` is a powerful command used to undo changes in the repository's history. This command can modify the state of the working directory and the index.

#### Commonly Used Options

* **`--soft`**: Moves the HEAD pointer to a specified commit without changing the working directory or the staging area. Useful for undoing a commit without losing any changes.
* **`--mixed`**: Default option if no other is specified. Resets the index but not the working directory. Changes remain as unstaged.
* **`--hard`**: Resets the index and the working directory. All changes in the working directory are lost, making it a risky but useful option for discarding unwanted changes.

#### Example Usage

1.  **Undo Last Commit but Keep Changes**:

    ```bash
    git reset --soft HEAD~1
    ```

    This command undoes the last commit while preserving changes in the working directory and staging area.
2.  **Unstage Files After Reset**:

    ```bash
    git reset HEAD
    ```

    Use this to unstage files that were mistakenly added to the staging area.
3.  **Discard Changes Permanently**:

    ```bash
    git reset --hard
    ```

    This command will discard all modifications in the working directory and set it to the last commit state. Use with caution.

#### Tips for Using `git reset` Safely

* **Always check your work**: Before performing a `git reset`, ensure you have backed up any critical changes you don't want to lose.
* **Understand the risks**: Especially when using `--hard`, as this can permanently erase changes.
* **Use `git status` frequently**: To understand the current state of your working directory and what changes you are affecting.
* **Consider alternatives**: Sometimes, `git checkout` or `git revert` may be safer options depending on your needs.

For more information, visit the [official Git documentation](https://git-scm.com/docs/git-reset).
