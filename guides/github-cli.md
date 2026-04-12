# GitHub CLI Guide

## Installing GitHub CLI

Install GitHub CLI on Windows using:

```powershell
winget install --id GitHub.cli
```

## Authenticating with GitHub

Run the following command and complete the interactive login flow:

```bash
gh auth login
```

## Working with Pull Requests

### List all pull requests

```bash
gh pr list --state "all"
```

### Check pull request status

```bash
gh pr status
```

### Create a pull request

Switch to the branch you want to merge, then create the PR:

```bash
git checkout <branch_to_be_merged>
gh pr create --title "Your PR Title" --body "Description of changes" --reviewer "username1,username2" --assignee "@me"
```

- `--reviewer` requests a code review from one or more users
- `--assignee` assigns the PR to a user for follow-up or merging

### View pull request details

Use the pull request ID or URL to inspect details:

```bash
gh pr view <id>
```

### Checkout a pull request branch

To switch to the branch associated with a pull request:

```bash
gh pr checkout <id>
```

### Merge a pull request after reviewer's approval

After the PR is approved, merge it using one of these options:

- Squash and merge:

```bash
gh pr merge <id> --squash --delete-branch
```

- Merge without squashing:

```bash
gh pr merge <id> --merge --delete-branch
```

- Rebase and merge:

```bash
gh pr merge <id> --rebase --delete-branch
```

The `--delete-branch` flag removes the branch after merge. Use the merge style that matches your repository workflow.