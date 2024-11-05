# diff

### Git Diff Command

The `git diff` command is used to show changes between commits, commit and working tree, etc. It is a versatile command you can use in various scenarios to review code changes.

#### Commonly Used Options

* `--staged` or `--cached`: Show differences between the staged changes and the last commit.
* `--name-only`: Display only the names of affected files instead of the differences.
* `--stat`: Show statistics about the changes, such as the number of insertions and deletions per file.
* `--color`: Ensure the diff output is colorized for easier reading.

#### Examples

*   **Compare Changes in Working Directory**:

    ```bash
    git diff
    ```
*   **Compare Staged Changes to Last Commit**:

    ```bash
    git diff --staged
    ```
*   **Show Only File Names with Changes**:

    ```bash
    git diff --name-only
    ```
*   **Compare Two Branches**:

    ```bash
    git diff main feature-branch
    ```

For more information, visit the [official Git documentation](https://git-scm.com/docs/git-diff).
