# merge

### Git Merge Command

The `git merge` command is a fundamental tool in Git used to combine changes from different branches into a single branch. It integrates the history of these branches, ensuring that all updates are consolidated into a new merge commit.

#### Basic Usage

*   **Merge a Branch into the Current Branch**: To merge changes from one branch into your current branch, use:

    ```bash
    git merge <branch-name>
    ```

    Example: To merge changes from `feature-branch` into your current branch, run:

    ```bash
    git merge feature-branch
    ```

#### Common Options

*   **--no-commit**: Perform the merge but stop before creating a merge commit. This allows you to inspect and tweak the merge result before committing.

    ```bash
    git merge --no-commit <branch-name>
    ```
*   **--squash**: Combine all changes from the merged branch into a single commit on the current branch, without creating a merge commit.

    ```bash
    git merge --squash <branch-name>
    ```
*   **--abort**: Abort the merge process and return to the state before the merge began. This is useful if you encounter too many conflicts.

    ```bash
    git merge --abort
    ```
*   **-s** : Specify a merge strategy to use. Common strategies include `recursive` (default) and `ours`.

    ```bash
    git merge -s recursive <branch-name>
    ```

#### Practical Examples

1.  **Basic Merge**: Suppose you have two branches, `main` and `feature`, and you want to incorporate changes from `feature` into `main`:

    ```bash
    git checkout main
    git merge feature
    ```
2.  **Squash Merge**: If you want to combine all changes from `feature` into a single commit on `main`, use:

    ```bash
    git checkout main
    git merge --squash feature
    git commit -m "Merge feature with squash"
    ```
3.  **Handling Conflicts**: When merging branches, conflicts may arise if both branches have modified the same part of a file. Git will pause the merge process and allow you to manually resolve these conflicts. After resolving conflicts, continue with:

    ```bash
    git add <resolved-files>
    git commit -m "Resolved conflicts"
    ```
4.  **Aborting a Merge**: If you start a merge but decide not to proceed due to complex conflicts, you can abort it:

    ```bash
    git merge --abort
    ```

#### How Git Merge Works

When performing a `git merge`, Git identifies the common base commit where the branches diverged, calculates diffs from this base to each branch, and applies these diffs to create a new commit on the target branch. This new commit is called a "merge commit" and has two parent commits: one from each of the merged branches\[1]\[2]\[3]. If there are no conflicts, this process is automatic; otherwise, manual conflict resolution is required\[4]\[5].
