
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

## Step 2: Adding Config File for Multiple GitHub Accounts

Create a config file for efficient SSH usage:

```bash
cd ~/.ssh/
mkdir config
cd config
# Edit the config file (using your preferred editor, e.g., vim config)
```

Add the following content to the config file:

```
Host <your_hostname> github.com
    Hostname github.com
    AddKeysToAgent yes
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/<filename>
```

## Step 3: Adding SSH Public Key to GitHub

1. Open your GitHub account
2. Go to Settings → SSH and GPG Keys → New SSH Key
3. Add your public key
4. Click "Add SSH Key"

## Step 4: Cloning the Repository

Navigate to the directory where you want to clone the repo and run:

```bash
git clone git@<your_hostname>:username/repository.git
```

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

