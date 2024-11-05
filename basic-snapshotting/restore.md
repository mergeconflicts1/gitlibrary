# restore

### Git Restore Command: Overview and Usage

The `git restore` command is a versatile tool in Git, introduced in version 2.23, that allows developers to undo changes in the working directory and the staging area. It provides a safer and more explicit alternative to `git reset` for discarding changes, helping manage different restoration scenarios effectively.

#### Basic Explanation

* **Purpose**: `git restore` is used to revert changes made to files in the working directory or the staging area (index) to their last committed state. It allows you to selectively discard edits or unstage files without affecting the commit history.
* **Functionality**: This command helps manage changes by providing options to restore files from specific commits, branches, or tags, making it an essential tool for resetting files to a previous state.

#### Commonly Used Options

* **Restore Working Directory Changes**:
  * `git restore <file>`: Reverts changes in the specified file back to its last committed state. This discards any uncommitted local changes.
* **Unstage Files**:
  * `git restore --staged <file>`: Removes the specified file from the staging area but retains any changes in the working directory.
* **Restore Both Staging Area and Working Directory**:
  * `git restore --source=HEAD --staged --worktree <file>`: Reverts both the staging area and working directory for the specified file to its state at the last commit.
* **Restore from Specific Commit**:
  * `git restore --source=<commit> <file>`: Restores a file to its state at a specific commit, identified by its hash or reference.
* **Interactive Mode**:
  * `git restore --patch <file>`: Allows you to interactively select hunks of changes to be restored, providing fine-grained control over what gets reverted.

#### Practical Example

Here's how you might use `git restore` in a typical workflow:

1.  **Revert Changes in a File**: Suppose you made unwanted changes to `example.txt` and want to discard them:

    ```bash
    git restore example.txt
    ```

    This command reverts `example.txt` back to its last committed state.
2.  **Unstage a File**: If you staged `example.txt` by mistake and want to unstage it:

    ```bash
    git restore --staged example.txt
    ```

    This removes the file from the staging area but keeps your local modifications intact.
3.  **Restore All Changes in Working Directory**: To revert all modified files in your working directory:

    ```bash
    git restore .
    ```

    This command resets all files back to their last committed states without affecting staged changes.
4.  **Restore from a Specific Commit**: If you need to revert a file to its state in a specific commit (e.g., commit `a1b2c3d`):

    ```bash
    git restore --source=a1b2c3d example.txt
    ```
5.  **Interactive Restoration**: For more control over which parts of a file are restored, use interactive mode:

    ```bash
    git restore --patch example.txt
    ```

    This allows you to selectively choose which changes to revert.

By mastering `git restore`, developers can efficiently manage their codebase, ensuring that only intended changes are retained while unwanted modifications are safely discarded. This command is particularly useful for maintaining clean and organized repositories during active development.

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="https://www.udemy.com/course/git-the-complete-guide-to-beginners-and-experienced-users/?referralCode=35B132FCB064AEB4EB91">Git – The Complete Guide to Beginners and Experienced Users</a></td><td></td><td></td><td><a href="../.gitbook/assets/CleanShot-2024-09-05-at-20.04.32 (2).png">CleanShot-2024-09-05-at-20.04.32 (2).png</a></td></tr></tbody></table>

