# commit

### Git Commit Command

The `git commit` command is used to save changes to the local repository. Committing captures a snapshot of the project's current changes. It's an essential part of version control that allows developers to document their work history.

#### Commonly Used Options

* `-m <message>`: Use this option to include a commit message. It's a short description of the commit.
* `-a`: Automatically stage files that have been modified and deleted, skipping the manual staging phase.
* `--amend`: Modify the most recent commit. Useful for changing the commit message or adding forgotten changes.
* `--no-edit`: Keep the existing commit message when amending a commit.

#### Example Usage

Create a new commit with a message:

```bash
git commit -m "Add user authentication feature"
```

Automatically stage and commit changes with a message:

```bash
git commit -am "Fix bug in login function"
```

Amend the last commit without changing the commit message:

```bash
git commit --amend --no-edit
```

#### Best Practices

* Always write clear and informative commit messages.
* Keep commits focused on a single topic or change.
* Commit frequently to avoid large, unwieldy changesets.

#### Additional Tips

* Review all code and commit changes before merging into the main branch.
* Use branching strategies effectively to manage feature development and bug fixes.
* Ensure commits are atomic and can be reverted if necessary.
* Collaborate with team members for code reviews to maintain code quality.
* Utilize version control tools and commands efficiently to track progress and development.

For more information, visit the [official Git documentation](https://git-scm.com/docs/git-commit).
