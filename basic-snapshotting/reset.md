# reset

### Git Reset Command: Overview and Usage

The `git reset` command is a powerful tool in Git that allows developers to undo changes in their repository. It can modify the commit history, the staging area, and the working directory, depending on the mode used. This command is particularly useful for correcting mistakes but must be used with caution as it can lead to data loss.

#### Basic Explanation

* **Purpose**: `git reset` is used to move the current `HEAD` to a specified commit, adjusting the staging area and/or working directory accordingly. It helps in undoing commits, unstaging files, or discarding changes.
* **Functionality**: The command operates on three levels of Git's "three trees": the Commit Tree (`HEAD`), the Staging Index, and the Working Directory.

#### Modes of Git Reset

1. **Soft Reset** (`--soft`):
   * **Usage**: `git reset --soft <commit>`
   * **Functionality**: Moves the `HEAD` to a specified commit without altering the index or working directory. This effectively undoes commits while keeping changes staged.
   *   **Example**: Undo the last commit but keep changes staged:

       ```bash
       git reset --soft HEAD^
       ```
2. **Mixed Reset** (`--mixed`):
   * **Usage**: `git reset <commit>` or `git reset --mixed <commit>`
   * **Functionality**: Moves the `HEAD` and resets the index to match the specified commit, but does not change the working directory. This unstages changes but keeps them in your files.
   *   **Example**: Unstage changes from the last commit:

       ```bash
       git reset HEAD^
       ```
3. **Hard Reset** (`--hard`):
   * **Usage**: `git reset --hard <commit>`
   * **Functionality**: Moves the `HEAD`, resets both the index and working directory to match the specified commit. This discards all local changes.
   *   **Example**: Completely revert to a previous commit:

       ```bash
       git reset --hard HEAD~3
       ```

#### Practical Example

Here's how you might use `git reset` in a typical workflow:

1.  **Undo a Commit but Keep Changes Staged**: Suppose you committed too early and want to make additional changes before committing again:

    ```bash
    git reset --soft HEAD~
    ```

    This command undoes your last commit but leaves your changes staged.
2.  **Unstage Changes Without Losing Them**: If you added files to the staging area by mistake:

    ```bash
    git reset HEAD
    ```

    This removes files from staging while retaining your modifications in the working directory.
3.  **Discard All Local Changes**: To completely discard all changes and revert your working directory to a clean state:

    ```bash
    git reset --hard HEAD
    ```
4.  **Reset to Match Remote Branch**: If you need your local branch to exactly match a remote branch:

    ```bash
    git fetch origin
    git reset --hard origin/main
    ```

By mastering `git reset`, developers can effectively manage their project's history and rectify mistakes, ensuring a clean and organized codebase. However, due caution should be exercised, especially with `--hard`, as it can permanently delete data.

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="https://www.udemy.com/course/git-the-complete-guide-to-beginners-and-experienced-users/?referralCode=35B132FCB064AEB4EB91">Git – The Complete Guide to Beginners and Experienced Users</a></td><td></td><td></td><td><a href="../.gitbook/assets/CleanShot-2024-09-05-at-20.04.32 (2).png">CleanShot-2024-09-05-at-20.04.32 (2).png</a></td></tr></tbody></table>

