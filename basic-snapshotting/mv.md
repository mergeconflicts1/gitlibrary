# mv

### Git Mv Command: Overview and Usage

The `git mv` command is a convenient tool in Git that enables developers to rename or move files and directories within a repository. It simplifies the process by combining the file system operation with staging changes, ensuring that Git's index is updated correctly.

#### Basic Explanation

* **Purpose**: `git mv` is used to rename or move files and directories within a Git repository. It updates the Git index automatically, making it easier to track changes without manually staging them.
* **Functionality**: This command effectively combines the actions of moving a file, removing the old path from the index, and adding the new path to the index. It ensures that the history of the file is preserved through the renaming or moving process.

#### Commonly Used Options

* **Force Overwrite**:
  * `git mv -f <source> <destination>`: Forces the move or rename operation even if a file already exists at the destination. Use this option with caution as it can overwrite existing files.
* **Skip Errors**:
  * `git mv -k <source> <destination>`: Skips any errors that occur during the move or rename operation, such as when a destination file already exists.
* **Dry Run**:
  * `git mv -n <source> <destination>`: Performs a dry run, showing what changes would occur without actually executing them. This is useful for verifying operations before making changes.
* **Verbose Output**:
  * `git mv -v <source> <destination>`: Provides detailed output of the files being moved or renamed, useful for tracking operations in larger projects.

#### Practical Example

Here's how you might use `git mv` in a typical workflow:

1.  **Rename a File**: To rename a file from `oldname.txt` to `newname.txt`, use:

    ```bash
    git mv oldname.txt newname.txt
    ```

    This command renames the file and stages it for commit, updating Git's index accordingly.
2.  **Move a File to a Different Directory**: If you want to move `file.txt` from its current location to a directory named `docs/`, execute:

    ```bash
    git mv file.txt docs/file.txt
    ```

    This moves the file and updates its path in Git's index.
3.  **Force Move Over Existing File**: To overwrite an existing file at the destination, use:

    ```bash
    git mv -f source.txt destination.txt
    ```
4.  **Perform a Dry Run**: Before executing a move operation, check what will happen with:

    ```bash
    git mv -n oldfile.txt newfile.txt
    ```
5.  **Verbose Output for Large Moves**: For detailed feedback during large operations, use:

    ```bash
    git mv -v *.txt archive/
    ```

By using `git mv`, developers can efficiently manage file and directory structures within their repositories while preserving history and ensuring that changes are properly tracked. This command simplifies project organization and helps maintain a clean and consistent codebase.

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="https://www.udemy.com/course/git-the-complete-guide-to-beginners-and-experienced-users/?referralCode=35B132FCB064AEB4EB91">Git – The Complete Guide to Beginners and Experienced Users</a></td><td></td><td></td><td><a href="../.gitbook/assets/CleanShot-2024-09-05-at-20.04.32 (2).png">CleanShot-2024-09-05-at-20.04.32 (2).png</a></td></tr></tbody></table>

