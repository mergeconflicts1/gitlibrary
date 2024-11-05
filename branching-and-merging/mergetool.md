# mergetool

### Overview of `git mergetool`

The `git mergetool` command is used to resolve merge conflicts in Git by invoking a merge tool. This tool provides a visual interface to help developers address conflicts that occur when merging branches. It is typically used after a `git merge` operation when conflicts arise that cannot be automatically resolved by Git\[1]\[2]\[3].

### Commonly Used Options

**1. `-t` or `--tool`**\
This option allows you to specify which merge tool to use. If no tool is specified, Git will use the tool configured in the `merge.tool` configuration variable\[1]\[2].

**2. `-g` or `--gui`**\
Use this option to specify a graphical merge tool if one is configured under `merge.guitool`. If not set, it defaults to the tool configured under `merge.tool`\[1]\[2].

**3. `--no-gui`**\
Overrides any previous GUI settings and uses the default merge tool specified in the configuration\[1]\[2].

**4. `--prompt` and `--no-prompt`**\
These options control whether Git prompts before launching the merge tool for each file. By default, Git does not prompt\[4].

### Configuration

To configure a specific merge tool, you can use:

```bash
git config --global merge.tool <tool_name>
```

For example, to set Meld as your default merge tool:

```bash
git config --global merge.tool meld
```

You can also specify the path to your tool using:

```bash
git config --global mergetool.<tool_name>.path <path_to_tool>
```

### Practical Example

Here's how you can use `git mergetool` in a real-world scenario:

1.  **Create a Conflict:**

    * Create a new branch and make changes to a file.
    * Switch back to the main branch and make conflicting changes to the same file.
    * Attempt to merge the branches, which will result in a conflict.

    ```bash
    git checkout -b feature-branch
    echo "Feature change" >> myfile.txt
    git commit -am "Feature change"
    git checkout main
    echo "Main change" >> myfile.txt
    git commit -am "Main change"
    git merge feature-branch
    ```
2.  **Resolve the Conflict:**

    * Run `git mergetool` to open the configured merge tool.

    ```bash
    git mergetool
    ```
3. **Use the Merge Tool:**
   * The merge tool will display conflicting sections from both branches.
   * Choose which changes to keep or manually edit the content.
   * Save and close the tool once conflicts are resolved.
4.  **Complete the Merge:**

    * After resolving conflicts, commit the changes.

    ```bash
    git commit -m "Resolved merge conflicts"
    ```

Using `git mergetool`, developers can efficiently resolve conflicts with a visual interface, reducing errors and improving workflow\[3]\[4].
