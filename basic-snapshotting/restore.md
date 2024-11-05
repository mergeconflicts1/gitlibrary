# restore

### Git Restore Command

The `git restore` command is used to undo changes in the working directory or the staging area. It offers a more focused approach to reapplying the state of the codebase, specifically catering to the needs of adjusting and amending changes.

#### Commonly Used Options

* **`--source=<tree>`**: Specify the tree to restore from.
* **`--staged`**: Restore changes to the staging area (index).
* **`--worktree`**: Restore changes to the working directory.
* **`--patch`**: Interactively select portions of the file to restore.

#### Example Usage

```bash
# Restore changes to a specific file in the working directory
git restore path/to/file.txt

# Restore changes to the staging area for a specific file
git restore --staged path/to/file.txt

# Interactively restore parts of the file
git restore --patch path/to/file.txt
```

These examples demonstrate how you can leverage the `git restore` command to manage changes meticulously, whether it's reapplying specific adjustments, modifying staged content, or interactively selecting changes to modify.

For more information, visit the [official Git documentation](https://git-scm.com/docs/git-restore).
