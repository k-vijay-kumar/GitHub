# Local Git Configuration

## Configuring User Information

To configure your workspace with user details:

```bash
git config --global user.name "your_name"
git config --global user.email "your_email"
```

**Note**: Use your real name and email so commits are linked to you.

## Configuring difftool

To configure your workspace with the difftool

```bash
git config --global diff.tool <toolname>
git config --global difftool.<toolname>.path "C:/Path/to/<toolname>.exe"
git config --global difftool.prompt false
```

Note: tkdiff/meld is a common choice

## Setting Default Branch Name

If you want new repositories to start with a branch name other than `main`, you can set:

```bash
git config --global init.defaultBranch <name>
```

This is optional; skip it if you are okay with the default branch name `main`.


## To view all the configurations

```bash
git config --global --list
```

## To remove a configuration

```bash
git config --global --unset <key>
```