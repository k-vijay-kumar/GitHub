# Git File Workflow

## Git Areas

Git works with a few simple places:

1. **Working Directory**: The files you edit on your computer.
2. **Staging Area**: The files prepared to be committed.
3. **Local Repository**: The committed history stored in the `.git` folder.
4. **Remote Repository**: The copy of the repository on GitHub.

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

The `-u` flag sets the upstream for this branch, so later you can use `git push` without the remote and branch name.

If the upstream is already set, use:

```bash
git push
```
