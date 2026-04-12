# Working with Branches

## Viewing Available Branches

To see all available branches:

```bash
git branch
```

## Creating a New Branch

To create a new branch from a specific commit (get commit ID from `git log --oneline`):

```bash
git branch <branch_name> <commit_id>
```

## Switching Branches

To move into a branch:

```bash
git checkout <branch_name>
# or
git switch <branch_name>
```

## Deleting Branches

### Local Branch

To delete a local branch:

```bash
git branch -d <branch_name>
```

### Remote Branch

To delete a remote branch:

```bash
git push origin -d <branch_name>
```

## Pushing Branch Changes

To push local branch changes to a remote branch:

```bash
git push -u origin <branch_name>
```

## Merging Branches

### Local Merge

To merge a branch locally:

```bash
git checkout main
git pull origin main
git merge <branch_name>
git push origin main
```

### Using Pull Requests

To merge using a pull request:

```bash
git checkout <branch_name>
git push origin <branch_name>
gh pr create --title "Your PR Title" --body "Description of changes"
gh pr merge --squash --delete-branch
```


