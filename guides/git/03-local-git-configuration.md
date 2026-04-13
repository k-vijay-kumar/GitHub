# Local Git Configuration

## Configuring User Information

To configure your workspace with user details:

```bash
git config --global user.name "your_name"
git config --global user.email "your_email"
```

**Note**: Use your real name and email so commits are linked to you.

## Setting Default Branch Name

If you want new repositories to start with a branch name other than `main`, you can set:

```bash
git config --global init.defaultBranch <name>
```

This is optional; skip it if you are okay with the default branch name `main`.
