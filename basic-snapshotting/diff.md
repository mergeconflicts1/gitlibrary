# diff

### Git Diff Command: Overview and Usage

The `git diff` command is a powerful tool in Git that allows developers to compare changes within a repository. It can be used to view differences between commits, branches, files, and more. This command is essential for understanding what modifications have been made before staging or committing changes.

#### Basic Explanation

* **Purpose**: `git diff` shows the differences between two data sets, such as working directory changes compared to the last commit, differences between branches, or changes between specific commits.
* **Functionality**: It provides a detailed line-by-line comparison, highlighting additions and deletions in the code, which helps in reviewing changes before they are staged or committed.

#### Commonly Used Options

* **View Unstaged Changes**:
  * `git diff`: Displays changes in the working directory that have not yet been staged for commit.
* **View Staged Changes**:
  * `git diff --staged` or `git diff --cached`: Shows changes that have been staged for the next commit.
* **Compare Specific Files**:
  * `git diff <file-path>`: Compares the current version of a specific file with its last committed version.
* **Compare Two Commits**:
  * `git diff <commit-id-1> <commit-id-2>`: Shows differences between two specific commits.
* **Summary of Changes**:
  * `git diff --stat`: Provides a summary of changes, showing the number of insertions and deletions per file.
* **Compare Branches**:
  * `git diff <branch-name-1>..<branch-name-2>`: Compares differences between two branches.

#### Practical Example

Here's how you might use `git diff` in a typical workflow:

1.  **View Local Changes**: After making changes to your files, you can check what has been modified before staging them:

    ```bash
    git diff
    ```

    This command will show all unstaged changes in your working directory.
2.  **Check Staged Changes**: Once you stage your changes using `git add`, you can verify what is prepared for commit:

    ```bash
    git add .
    git diff --staged
    ```

    This will display only the changes that are staged for the next commit.
3.  **Compare Specific Files**: To see what has changed in a particular file since the last commit:

    ```bash
    git diff README.md
    ```
4.  **Review Differences Between Commits**: To understand what changed between two commits, use:

    ```bash
    git diff abc1234 def5678
    ```

    Replace `abc1234` and `def5678` with the actual commit hashes you want to compare.
5.  **Summarize Changes**: For a quick overview of what files were changed and how many lines were added or removed:

    ```bash
    git diff --stat
    ```

By mastering `git diff`, developers can gain insights into their code modifications, ensuring that only intended changes are included in commits. This practice helps maintain code quality and facilitates effective collaboration within teams.

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="https://www.udemy.com/course/git-the-complete-guide-to-beginners-and-experienced-users/?referralCode=35B132FCB064AEB4EB91">Git – The Complete Guide to Beginners and Experienced Users</a></td><td></td><td></td><td><a href="../.gitbook/assets/CleanShot-2024-09-05-at-20.04.32 (2).png">CleanShot-2024-09-05-at-20.04.32 (2).png</a></td></tr></tbody></table>

