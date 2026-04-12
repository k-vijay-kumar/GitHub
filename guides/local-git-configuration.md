# Local Git Configuration

## Configuring User Information

To configure your workspace with user details:

```bash
git config --global user.name "your_name"
git config --global user.email "your_email"
```

**Note**: Use your GitHub no-reply email for the email address.

## Setting Default Branch Name

To configure the default branch name for new repositories:

```bash
git config --global init.defaultBranch <name>
```

## Caching Credentials

To cache credentials for 1 hour to avoid repeated logins:

```bash
git config --global credential.helper 'cache --timeout=3600'
```