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

Create a branch from the current commit:

```bash
git branch <branch_name>
```

Or create and switch to it in one step:

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

Push a new local branch to the remote repository and set upstream:

```bash
git push -u origin <branch_name>
```

For existing branches, a regular push is sufficient:

```bash
git push
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
git push -u origin <branch_name>
```

2. Create the pull request using GitHub CLI:

```bash
gh pr create --title "Your PR Title" --body "Description of changes"
```

3. After the PR is approved, merge it:

```bash
gh pr merge <id> --squash --delete-branch
```

Alternatively, to merge without squashing:

```bash
gh pr merge <id> --merge --delete-branch
```

4. For more GitHub CLI PR workflow details, see `guides/github-cli.md`.

