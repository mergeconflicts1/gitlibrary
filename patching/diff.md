# diff

The `git diff` command is an essential tool in Git that allows users to view changes between different versions of files, commits, branches, and more. This command is crucial for tracking modifications and understanding the differences in your codebase over time. Below is a comprehensive guide to using `git diff`, including its basic usage, commonly used options, and practical examples.

### Basic Explanation

The `git diff` command outputs the differences between two data sets in a Git repository. These data sets can be files, commits, branches, or even the working directory versus the staging area. By default, `git diff` shows changes that have been made but not yet staged for commit.

### Commonly Used Options

* **`--staged` or `--cached`**: Shows changes that have been staged for the next commit. This is useful after running `git add` but before committing.
* **`--stat`**: Provides a summary of changes, showing which files have changed and the number of lines added or deleted.
* **`--name-only`**: Displays only the names of changed files without showing the actual changes.
* **`--name-status`**: Shows file names along with their status (added, modified, deleted).
* **`<commit-id1> <commit-id2>`**: Compares differences between two specific commits.
* **`<branch1>..<branch2>`**: Compares differences between two branches.

### Example Usage

#### Viewing Unstaged Changes

To see what changes have been made in your working directory that are not yet staged:

```bash
git diff
```

This will display all modifications made since the last commit.

#### Viewing Staged Changes

To view changes that are staged for the next commit:

```bash
git diff --staged
```

This command is equivalent to `git diff --cached`.

#### Comparing Specific Files

To see changes in a specific file compared to its last committed state:

```bash
git diff <file-path>
```

Replace `<file-path>` with the path to your file.

#### Comparing Two Commits

To compare changes between two commits:

```bash
git diff <commit-id1> <commit-id2>
```

This will show what has changed from `<commit-id1>` to `<commit-id2>`.

#### Comparing Branches

To compare changes between two branches:

```bash
git diff <branch1>..<branch2>
```

This shows differences from `<branch1>` to `<branch2>`.

#### Summary of Changes

To get a summary of which files have changed and how many lines were added or removed:

```bash
git diff --stat
```

This provides a concise overview of the impact of changes across files.

#### Exporting Diff to a File

To save the output of a diff to a file for later review or sharing:

```bash
git diff > diff_output.txt
```

This writes the diff output into `diff_output.txt`.

These examples illustrate how `git diff` can be used to track and analyze changes within a Git repository effectively. By mastering these options and commands, you can gain better insight into your project's history and current state.
