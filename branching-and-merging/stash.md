# stash

### Git Stash Command: Overview and Usage

The `git stash` command is a powerful tool in Git that allows developers to temporarily save changes in their working directory without committing them. This is particularly useful when you need to switch branches or work on something else without losing your current progress.

#### Basic Explanation

* **Purpose**: `git stash` temporarily saves your changes, allowing you to revert your working directory to the last committed state\[1]\[2].
* **Functionality**: It acts like a clipboard for your changes, storing them in a "stash" that you can apply later\[3].

#### Commonly Used Options

* **Stash Changes**:
  * `git stash`: Saves all tracked changes.
  * `git stash -u` or `git stash --include-untracked`: Includes untracked files in the stash\[3].
  * `git stash -a` or `git stash --all`: Stashes all files, including ignored ones\[4].
* **View Stashed Changes**:
  * `git stash list`: Lists all stashes with their index and description\[1]\[5].
  * `git stash show [stash@{n}]`: Shows a summary of changes in a specific stash. Use `-p` for a detailed diff\[1].
* **Apply Stashed Changes**:
  * `git stash apply [stash@{n}]`: Applies the changes from a specified stash without removing it from the list\[2]\[3].
  * `git stash pop [stash@{n}]`: Applies the changes and removes the stash from the list\[1]\[4].
* **Delete Stashed Changes**:
  * `git stash drop [stash@{n}]`: Removes a specific stash\[5].
  * `git stash clear`: Clears all stashes\[1]\[5].

#### Practical Example

Here's a step-by-step example of how you might use `git stash`:

1.  **Save Changes**: You're working on branch A and need to switch to branch B quickly.

    ```bash
    git stash
    ```

    This command saves your current work and cleans your working directory.
2.  **Switch Branches**:

    ```bash
    git checkout branch-B
    ```

    You can now switch to another branch without losing your work.
3. **Work on Branch B**: Make necessary changes, commit them, and push if needed.
4.  **Return to Branch A**:

    ```bash
    git checkout branch-A
    ```
5.  **Retrieve Your Changes**:

    ```bash
    git stash pop
    ```

    This retrieves your stashed changes and removes them from the stash list.

By using these commands, developers can efficiently manage their workflow without committing incomplete work or losing progress when switching tasks.
