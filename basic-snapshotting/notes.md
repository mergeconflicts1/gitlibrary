# notes

### Git Notes Command Overview

Git `notes` is a versatile command that allows you to attach additional information to specific commits without modifying the original commit history.

#### Commonly Used Options

* **`git notes add`**: Add a note to the specified commit. If no commit is specified, the tip of the current branch is used.
* **`git notes show`**: Display the notes for a specific commit. Defaults to the current HEAD if no commit is specified.
* **`git notes edit`**: Edit the note attached to a specified commit.
* **`git notes remove`**: Remove the notes from a specified commit.

#### Practical Example

1.  **Adding a Note**:

    ```bash
    git notes add -m "This commit fixes issue #42"
    ```

    This command adds the note "This commit fixes issue #42" to the current commit.
2.  **Viewing a Note**:

    ```bash
    git notes show
    ```

    Displays the note attached to the current commit.
3.  **Editing a Note**:

    ```bash
    git notes edit
    ```

    Opens the default text editor to modify the note on the current commit.
4.  **Removing a Note**:

    ```bash
    git notes remove
    ```

    Deletes the note associated with the current commit.

By using `git notes`, you can maintain a clean commit history while still providing essential context and details for specific commits.

For more information, visit the [official Git documentation](https://git-scm.com/docs/git-notes).
