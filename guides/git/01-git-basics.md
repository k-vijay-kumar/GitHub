# Git Basics

## Checking Git Version

To check the installed Git version:

```bash
git --version
```

## Getting Help

To get details about a specific command:

```bash
git help <command_name>
```

## Git Repository Structure

- **`.git` folder**: Contains all repository details
- **`.gitignore` file**: Specifies files that Git should ignore


## HEAD Pointers

Git uses two main HEAD pointers:

1. **HEAD**: Points to the current local branch
2. **origin/HEAD**: Points to the default remote branch

## Understanding Remote Origins

In Git terms, `origin` is the default name for the URL of the repository you cloned from.

### Viewing Remote URLs

To see the remote repository URLs that origin points to:

```bash
git remote -v
```

### Renaming Origin

To rename the origin remote:

```bash
git remote rename origin <new_name>
```