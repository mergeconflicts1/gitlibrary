# rebase

The `git rebase` command is a powerful tool in Git that allows you to rewrite commit history by moving or combining a sequence of commits to a new base commit. It is particularly useful for maintaining a clean and linear project history, which can simplify collaboration and code review processes. Below is a detailed explanation of the `git rebase` command, its commonly used options, and practical examples.

### Basic Explanation

Rebasing in Git involves taking the commits from one branch and replaying them on top of another branch. This process changes the base of your branch from one commit to another, effectively rewriting the commit history to create a linear sequence of commits. Unlike merging, which creates a new commit to combine branches, rebasing integrates changes directly into the base branch.

### Commonly Used Options

* **`-i` or `--interactive`**: Initiates an interactive rebase session, allowing you to edit, reorder, squash, or drop commits.
* **`--onto`**: Allows you to specify a new base for the rebased commits, useful for more complex rebasing scenarios.
* **`--continue`**: Continues the rebase process after resolving conflicts.
* **`--abort`**: Aborts the rebase process and returns the branch to its original state before the rebase started.
* **`--skip`**: Skips the current commit during a rebase if it cannot be applied cleanly.

### Example Usage

#### Basic Rebase

To rebase your current branch onto another branch (e.g., `main`):

```bash
git checkout feature-branch
git rebase main
```

This reapplies the commits from `feature-branch` on top of `main`, creating a linear history.

#### Interactive Rebase

To start an interactive rebase for the last few commits:

```bash
git rebase -i HEAD~3
```

This opens an editor where you can reorder, squash, or edit commits. For example:

```
pick 1fc6c95 Commit A
squash 6b2481b Commit B
reword dd1475d Commit C
```

* **pick**: Use the commit as-is.
* **squash**: Combine this commit with the previous one.
* **reword**: Edit the commit message.

#### Using `--onto`

To move a branch onto a different base:

```bash
git checkout feature-branch
git rebase --onto new-base old-base feature-branch
```

This command moves all commits from `feature-branch` that are not in `old-base`, applying them onto `new-base`.

#### Handling Conflicts

If conflicts occur during rebasing:

1. Resolve conflicts in your files.
2.  Continue with:

    ```bash
    git add <resolved-files>
    git rebase --continue
    ```

If you decide not to proceed with the rebase:

```bash
git rebase --abort
```

#### Practical Scenario

Suppose you have a feature branch that diverged from `main`. After some time, `main` has been updated with important changes. You can use rebasing to incorporate these changes into your feature branch without creating additional merge commits:

```bash
git checkout feature-branch
git pull origin main --rebase
```

This command updates your local `feature-branch` by rebasing it onto the latest state of `main`.

By using `git rebase`, you can maintain a cleaner project history and facilitate smoother integration of changes across branches. However, it's important to use rebasing carefully, especially when working with shared branches, as it rewrites commit history and can affect collaborators.
