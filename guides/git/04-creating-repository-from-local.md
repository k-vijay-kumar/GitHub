# Creating a Repository from Local Machine

## Initializing a Local Repository

To initialize the project in the current workspace as a Git repository:

```bash
git init
```

## Committing Your Project

To commit your project files to the local repository:

```bash
git add <files>
git commit -m "msg_for_commit"
```

## Configuring the Remote Repository

To add the remote repository URL:

```bash
git remote add origin <repo_url>.git
```

## Pushing to Remote

To push the contents to the remote repository for the first time:

```bash
git push origin main
```

If your default branch is different, replace `main` with the correct branch name.
