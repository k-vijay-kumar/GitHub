# Git File Workflow

## Git Areas

Git operates with three main areas:

1. **Local (Working Directory)**: The cloned repository on your machine
2. **Stage (Staging Area)**: Caching area before committing to remote
3. **Remote (GitHub Repository)**: The remote repository

## File Modifications

Files on your local machine can be modified or new files added. These changes need to go through the staging area before committing to the local repository.

## Adding Files to Staging Area

To add modified files to the staging area:

```bash
git add <filename>
```

## Restoring Files

To remove modifications in a file after the previous commit:

```bash
git restore <filename>
```

## Committing Changes

To commit the files in the staging area to the local repository:

```bash
git commit -m "message_for_this_commit"
```

## Pushing to Remote

To update changes from the local repository to the remote repository:

```bash
git push -u origin <branch_name>
```

The `-u` flag sets the upstream, allowing future pushes with just `git push`. Alternatively, you can push without setting upstream using:

```bash
git push origin <branch_name>
```
