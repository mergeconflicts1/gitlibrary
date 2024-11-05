# mv

## Understanding `git mv`

The `git mv` command is used for renaming files and moving them from one location to another in a Git repository. It serves as a convenient way to accomplish this task while ensuring that Git tracks the changes properly.

### Commonly Used Options

* **`-f` or `--force`**: Force the move operation even if it will overwrite an existing file.
* **`-k` or `--skip-worktree-check`**: Skip checking if the working tree is clean prior to moving.
* **`-n` or `--dry-run`**: Simulate the move operation without executing it, useful for testing.

### Practical Example

Suppose you want to rename a file from `oldname.txt` to `newname.txt`, the following command can be used:

```bash
git mv oldname.txt newname.txt
```

To move a file `file.txt` from the current directory to a subdirectory `docs/`, use:

```bash
git mv file.txt docs/
```

To rename a file and force overwrite if necessary:

```bash
git mv -f oldfile.txt newfile.txt
```

By using `git mv`, you ensure that the changes are correctly staged and ready for commit, maintaining the integrity of your Git history.

For more information, visit the [official Git documentation](https://git-scm.com/docs/git-mv).
