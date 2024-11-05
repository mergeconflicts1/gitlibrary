# init

### `git init` Command Overview

The `git init` command initializes a new Git repository. It creates a new subdirectory named `.git` that contains all the necessary files for version control of your project. This command is the first step in creating a new repository.

#### Common Options

* `--bare`: Create a bare repository where the working tree is omitted. Useful for sharing a repository.
* `--quiet`, `-q`: Suppress output messages to provide a minimal feedback experience.

#### Usage Example

```bash
# Initialize a regular Git repository
git init

# Initialize a bare Git repository
git init --bare /path/to/repository.git

# Initialize a Git repository in quiet mode
git init -q
```

Utilize these options and examples to effectively set up your Git repositories tailored to your project's needs.

For further details, refer to the [official Git documentation on git init](https://git-scm.com/docs/git-init).
