# checkout

### Git Checkout Command

The `git checkout` command is a versatile tool in Git used primarily for switching branches and restoring files. It updates the files in the working directory to match the version stored in the specified branch or commit, and it updates Git's HEAD to point to the specified branch or commit\[1]\[2]\[3].

#### Commonly Used Options

* **Switching Branches**:
  * `git checkout <branch-name>`: Switches to the specified branch.
  * `git checkout -b <new-branch-name>`: Creates a new branch and switches to it\[2]\[3].
* **Checking Out Commits**:
  * `git checkout <commit-hash>`: Checks out a specific commit, putting the repository in a detached HEAD state\[4].
* **Restoring Files**:
  * `git checkout -- <file-name>`: Restores a file to its last committed state\[5].
* **Remote Branches**:
  * `git checkout --track <remote>/<branch>`: Checks out a branch from a remote repository and sets up tracking\[3].

#### Practical Examples

1.  **Switching to an Existing Branch**

    ```bash
    git checkout feature-branch
    ```

    This command switches your working directory to the `feature-branch`, updating all files to match this branch's state\[2].
2.  **Creating and Switching to a New Branch**

    ```bash
    git checkout -b new-feature
    ```

    This command creates a new branch called `new-feature` from the current HEAD and switches to it immediately\[2]\[3].
3.  **Checking Out a Specific Commit**

    ```bash
    git checkout 1a2b3c4d
    ```

    This puts your repository into a detached HEAD state at the commit with hash `1a2b3c4d`, allowing you to inspect or test this particular version of your project\[4].
4.  **Restoring a File**

    ```bash
    git checkout -- README.md
    ```

    This command restores the `README.md` file to its last committed state, discarding any changes made since then\[5].
5.  **Checking Out a Remote Branch**

    ```bash
    git checkout --track origin/feature-branch
    ```

    This sets up a local branch that tracks the remote `feature-branch` from `origin`, allowing you to fetch and merge changes easily\[3].

#### Conclusion

The `git checkout` command is essential for managing branches and revisions in Git. While newer commands like `git switch` have been introduced for clarity, `git checkout` remains widely used due to its versatility. Understanding its options and applications can significantly enhance your Git workflow.
