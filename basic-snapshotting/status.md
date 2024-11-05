# status

## Git `status` Command

The `git status` command provides essential information about the current state of the working directory and staging area. It displays changes that have been staged, changes that have not been staged, and files that are not being tracked by Git.

### Common Options

* `-s` or `--short`: Provides a shorter, more concise output.
* `-b` or `--branch`: Shows the branch and tracking information, along with the status summary.

### Usage Examples

#### Basic Usage

```bash
git status
```

Displays the full status of the current Git repository, detailing which changes are staged, unstaged, or untracked.

#### Short Status

```bash
git status -s
```

Provides a quick overview of the status with a simplified and compact format.

#### Branch Information

```bash
git status -b
```

Shows additional branch information along with the regular status output, useful for assessing branch tracking details.

For more details, see the [official Git documentation on git status](https://git-scm.com/docs/git-status).
