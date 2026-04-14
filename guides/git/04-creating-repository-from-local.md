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

To link the remote repository:

### step 1: Create a remote repo

Create an empty repo at the Github without any Readme, Lisence or .gitignore file

### step 2: Configure the origin 

```bash
git remote add origin <git@github.com:username/repository.git>.git
```

or

### Use github-cli

```bash
gh repo create <repo_name> --private --source=.
```

Note: gh by-default adds the origin with `github.com` as Host. If you have custom SSH host alias, replace `github.com` with your alias using below command

```bash
git remote set-url origin git@alias:username/repository.git
```

## Pushing to Remote

To push the contents to the remote repository:

```bash
git push origin main
```

If your default branch is different, replace `main` with the correct branch name.
