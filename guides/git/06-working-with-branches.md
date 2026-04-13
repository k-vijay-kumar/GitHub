# Working with Branches

## Viewing Available Branches

To list local branches:

```bash
git branch
```

To list all branches, including remote:

```bash
git branch -a
```

## Creating a New Branch

Create a new branch and switch to it:

```bash
git switch -c <branch_name>
```

If you only want to create the branch without switching:

```bash
git branch <branch_name>
```

Create a branch from a specified commit_id

```bash
git branch <branch_name> <commit_id>
```

## Switching Branches

Switch to an existing branch:

```bash
git checkout <branch_name>
# or
git switch <branch_name>
```

## Deleting Branches

### Delete a local branch

```bash
git branch -d <branch_name>
```

### Delete a remote branch

```bash
git push origin --delete <branch_name>
```

## Pushing Branch Changes

Push a new local branch to the remote repository:

```bash
git push origin <branch_name>
```

## Merging Branches

### Local merge workflow

1. Switch to the target branch (for example `main`):

```bash
git checkout main
# or
git switch main
```

2. Update the target branch:

```bash
git pull origin main
```

3. Merge the feature branch:

```bash
git merge <branch_name>
```

4. Push the merged result:

```bash
git push origin main
```

### Merge using GitHub pull requests

1. Make sure the feature branch is pushed to the remote:

```bash
git checkout <branch_name>
git push origin <branch_name>
```

2. Go to your GitHub repository in a web browser.
3. Click "Compare & pull request" (GitHub will suggest it for the new branch).
4. Add a title and description for the pull request.
5. Click "Create pull request".
6. After review and approval, click "Merge pull request" on GitHub (choose merge, squash, or rebase).

   - **Squash**: Combines all branch commits into one commit.
   - **Rebase**: Replays branch commits on top of main for a linear history.
   - **Merge**: Creates a merge commit preserving both branch histories.

**Note**: For creating and merging pull requests using GitHub CLI, see `guides/github-cli.md`.

