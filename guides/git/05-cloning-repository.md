
# Cloning a Repository

## Step 1: Creating SSH Key Pair

Generate an SSH key pair for secure authentication:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

**Notes**:
- Use your GitHub no-reply email for efficiency
- When prompted for filename, enter `~/.ssh/<filename>`
- Do not use a passphrase; just press Enter

## Step 2: Adding Config File for SSH Setup

If you want SSH to use a specific key file, create or edit `~/.ssh/config`:

```bash
code ~/.ssh/config
```

Add the following content:

```
Host github.com
    HostName github.com
    AddKeysToAgent yes
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/<filename>
```

If you are only using a single GitHub account and the default key file, this step is optional.

SSH aliases are useful if you have multiple GitHub accounts. You can set up different aliases (like `Host personal.github.com` and `Host work.github.com`) with different keys, allowing you to clone repos from different accounts on the same system.

## Step 3: Adding SSH Public Key to GitHub

1. Open your GitHub account
2. Go to Settings → SSH and GPG Keys → New SSH Key
3. Add your public key
4. Click "Add SSH Key"

## Step 4: Cloning the Repository

Navigate to the directory where you want to clone the repo and run:

```bash
git clone git@github.com:username/repository.git
```

If you set a custom SSH host alias in `~/.ssh/config`, replace `github.com` with your alias.

## Understanding Remote Origins

In Git terms, `origin` is the default name for the URL of the repository you cloned from.

### Viewing Remote URLs

To see the remote repository URLs that origin points to:

```bash
git remote -v
```

### Renaming Origin

To rename the origin remote:

```bash
git remote rename origin <new_name>
```

