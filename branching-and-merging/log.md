# log

### Overview of `git log`

The `git log` command is a powerful tool used to display the commit history of a Git repository. By default, it lists all commits in reverse chronological order, showing details such as the commit hash (SHA), author, date, and commit message\[1]\[2]\[5]. This command is essential for tracking changes and understanding the evolution of a codebase.

### Commonly Used Options

**1. `--oneline`**\
This option condenses the output to show each commit on a single line. It displays the abbreviated commit hash and the commit message, making it easier to scan through commit history\[1]\[2].

**2. `--stat`**\
Displays a summary of changes in each commit, including the files modified and the number of lines added or removed\[1].

**3. `-p` or `--patch`**\
Shows the differences introduced in each commit, similar to a patch file. This option is useful for reviewing changes in detail\[1]\[5].

**4. `--graph`**\
Visualizes the branch structure and merge history as a graph. It can be combined with other options like `--oneline` for a concise view\[1].

**5. `-n <number>`**\
Limits the output to the specified number of commits. For example, `git log -3` shows only the last three commits\[3]\[5].

**6. `--author=<author>`**\
Filters commits by a specific author, allowing you to see contributions from individual developers\[3].

### Practical Example

Here's how you can use `git log` in practice:

1.  **Basic Usage:**

    * To view all commits in a repository:

    ```bash
    git log
    ```
2.  **Condensed View:**

    * To see a brief overview of recent commits:

    ```bash
    git log --oneline
    ```
3.  **Detailed Changes:**

    * To examine what changes were made in each commit:

    ```bash
    git log -p
    ```
4.  **Graphical History:**

    * To visualize the branching and merging history:

    ```bash
    git log --graph --oneline
    ```
5.  **Limit Output:**

    * To view only the last two commits:

    ```bash
    git log -2
    ```
6.  **Filter by Author:**

    * To see commits by a specific author:

    ```bash
    git log --author="John Doe"
    ```

By using these options, developers can tailor the output of `git log` to suit their needs, whether they are reviewing recent changes or analyzing the entire project history.
