# commit

### Git Commit Command: Overview and Usage

The `git commit` command is a fundamental aspect of Git, serving as the primary method for recording changes in your repository. It captures a snapshot of the project's current state, preserving it in the repository's history.

#### Basic Explanation

* **Purpose**: `git commit` saves a snapshot of the staged changes in your project. This snapshot is stored in your local repository, allowing you to track the project's history over time.
* **Functionality**: Each commit represents a point in the project's timeline, complete with a message that describes the changes. This helps maintain a clear and navigable history of modifications.

#### Commonly Used Options

* **Commit with Message**:
  * `git commit -m "Your commit message"`: Commits staged changes with a message provided directly from the command line. The message should be concise and descriptive of the changes made.
* **Commit All Changes**:
  * `git commit -a -m "Your commit message"`: Automatically stages all modified and deleted files before committing them. This option skips the explicit staging step but does not include new untracked files\[1]\[2].
* **Amend Last Commit**:
  * `git commit --amend`: Modifies the most recent commit by adding new changes or altering the commit message. This is useful for correcting mistakes in the last commit.
* **Verbose Output**:
  * `git commit --verbose`: Displays the diff of what is being committed, allowing you to review changes as part of the commit process.

#### Practical Example

Here's how you might use `git commit` in a typical workflow:

1.  **Stage Changes**: First, stage the files you want to include in your commit using `git add`:

    ```bash
    git add file1.txt file2.txt
    ```
2.  **Commit Staged Changes**: Once your changes are staged, use `git commit` to save them:

    ```bash
    git commit -m "Add feature X and update documentation"
    ```

    This command records the staged changes with a descriptive message.
3.  **Commit All Modified Files**: If you want to quickly commit all modified files without staging them individually:

    ```bash
    git commit -a -m "Fix bugs in module Y"
    ```
4.  **Amend a Commit**: If you need to modify your last commit (e.g., to correct a typo in the message or include additional changes):

    ```bash
    git add forgotten-file.txt
    git commit --amend
    ```

    This opens an editor to update the commit message or includes additional staged changes.
5.  **Review Commit History**: After committing, use `git log` to view your project's history and verify your commits:

    ```bash
    git log --oneline
    ```

By mastering `git commit` and its options, developers can efficiently manage their project's history, ensuring that each change is well-documented and organized. This practice enhances collaboration and maintains a clear record of development progress.
