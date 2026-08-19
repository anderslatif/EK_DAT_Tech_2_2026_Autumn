<div class="title-card">
    <h1>Setup SSH Key in GitHub</h1>
</div>

---

# Motivation

This will make our lives easier when we need to push code to GitHub.

* What are SSH Keys?

You generate a pair of keys: A public key and a private key. You add the public key to GitHub and keep the private key on your computer.

When you connect to GitHub, the keys are used to verify your identity without needing a password.

* Why setup SSH Keys with GitHub?

GitHub has [disabled password authentication](https://github.blog/changelog/2021-08-12-git-password-authentication-is-shutting-down/).

You could create a Personal Access Token (PAT) every time you create a new repository but setting up SSH keys only needs to be done once. 

**Remember**: If you have a home PC, you need to set up SSH keys on that machine as well.

---

# Check if you have an existing SSH key

List the files in the hidden `.ssh` directory which is in your home directory:

```bash
$ ls ~/.ssh
```

If you have files named `id_rsa` and `id_rsa.pub` then you do not need to generate a new SSH key. Just watch along.

---

# Generate an SSH key

Generate an SSH key with with the following command (replace the mail with your GitHub email address):

```bash
$  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Press `Enter` (saves the file to default location which is recommended):

```plaintext
> Enter file in which to save the key (/C/Users/YOU/.ssh/id_ALGORITHM):
```

Press `Enter` without typing again to accept (no passphrase will be set):

```plaintext
Enter passphrase(optional):
```

---

# Check the generated SSH keys

1. List the files in the hidden `.ssh` directory again:

2. Can you show the content of the public and the private keys?

3. Copy your public key to your clipboard. Check that you have it. 


---

# Add the SSH key to your GitHub account

1. Go to: https://github.com/settings/keys

2. Click on `New SSH key`

3. Give it a title (e.g. "My Laptop", "Home Linux Server")

4. Paste your public key into the `Key` field

5. Click on `Add SSH key`

---

# Test the connection

Back in your terminal run:

```bash
$ ssh -T git@github.com
```

Since this is your first time connecting to GitHub, you may see a message like this (to make you verify that you intend to connect to this server for the first time):

```plaintext
Are you sure you want to continue connecting(yes/no/[fingerprint])?
```

Type `yes` and press `Enter`.

You should then see the following message:

```plaintext
Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.
```

---

# Set up SSH for future repositories

The following command will ensure that copying the GitHub URL will use SSH instead of HTTPS:

```bash
$ git config --global url."git@github.com:".insteadOf "https://github.com/"
```


