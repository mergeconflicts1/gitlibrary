---
icon: puzzle-piece
---

# Patching

The "Patching" section in Git involves several commands that are crucial for managing changes, integrating updates, and maintaining a clean project history. Below is an overview of the key commands used in patching, including `apply`, `cherry-pick`, `diff`, `rebase`, and `revert`.

### Overview of Patching Commands

#### **1. git apply**

The `git apply` command is used to apply changes from a patch file to your working directory. A patch file typically contains differences between two sets of files or commits, which can be generated using the `git diff` command. This command is useful for incorporating changes from external sources without immediately committing them, allowing for further testing and adjustments.

**Common Options:**

* `--check`: Verifies if a patch can be applied cleanly.
* `--index`: Applies the patch to both the working directory and the index (staging area).
* `--whitespace=fix`: Corrects any whitespace errors while applying the patch.

**Example Usage:**

```bash
git apply changes.patch
```

#### **2. git cherry-pick**

`git cherry-pick` allows you to apply the changes from a specific commit onto your current branch. This command is particularly useful for selectively integrating bug fixes or features without merging entire branches.

**Common Options:**

* `-x`: Records the original commit hash in the message of the cherry-picked commit.
* `--continue`: Continues after resolving conflicts.
* `--abort`: Aborts the cherry-pick process.

**Example Usage:**

```bash
git cherry-pick <commit-hash>
```

#### **3. git diff**

The `git diff` command displays differences between various data sources in your Git repository, such as files, commits, or branches. It helps track modifications and understand changes over time.

**Common Options:**

* `--staged`: Shows changes staged for the next commit.
* `--name-only`: Lists only the names of changed files.
* `<commit-id1> <commit-id2>`: Compares differences between two specific commits.

**Example Usage:**

```bash
git diff HEAD~1 HEAD
```

#### **4. git rebase**

`git rebase` is used to move or combine a sequence of commits to a new base commit. It helps maintain a linear project history by replaying commits from one branch onto another.

**Common Options:**

* `-i` or `--interactive`: Starts an interactive rebase session to edit, reorder, or squash commits.
* `--onto`: Specifies a new base for rebased commits.
* `--continue`: Continues after resolving conflicts.

**Example Usage:**

```bash
git rebase main
```

#### **5. git revert**

The `git revert` command creates a new commit that reverses the changes made by an earlier commit. This is useful for undoing changes while preserving project history.

**Common Options:**

* `--no-edit`: Uses the default commit message without opening an editor.
* `--no-commit`: Applies changes without committing them immediately.
* `-m <parent-number>`: Specifies which parent to use when reverting a merge commit.

**Example Usage:**

```bash
git revert <commit-hash>
```

These commands collectively provide powerful tools for managing patches, integrating selective changes, and maintaining a coherent project history in Git. By understanding and utilizing these commands effectively, developers can ensure smooth collaboration and efficient version control.

### Learn more about

<table data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td><a href="apply.md"><strong>apply</strong></a></td><td>The <code>git apply</code> command is used to apply patch files to a Git repository. </td><td></td></tr><tr><td><a href="cherry-pick.md"><strong>cherry-pick</strong></a></td><td>The <code>git cherry-pick</code> command is a powerful tool in Git that allows you to apply changes from a specific commit in one branch to another branch.</td><td></td></tr><tr><td><a href="../basic-snapshotting/diff.md"><strong>diff</strong></a></td><td>The <code>git diff</code> command is an essential tool in Git that allows users to view changes between different versions of files, commits, branches, and more. </td><td></td></tr><tr><td><a href="rebase.md"><strong>rebase</strong></a></td><td>The <code>git rebase</code> command is a powerful tool in Git that allows you to rewrite commit history by moving or combining a sequence of commits to a new base commit.</td><td></td></tr><tr><td><a href="revert.md"><strong>revert</strong></a></td><td>The <code>git revert</code> command is a crucial tool in Git for safely undoing changes by creating new commits that reverse the effects of earlier commits.</td><td></td></tr></tbody></table>

