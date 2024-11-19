---
layout: default
title: GitHub Setup
---

# Setting up GitHub

GitHub is a platform for hosting and collaborating on code repositories.

1. Create an account at [GitHub](https://github.com/)
2. Set up SSH keys for secure communication:
   ```bash
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```
3. Add the SSH key to your GitHub account:
   - Copy the public key
   - Go to GitHub → Settings → SSH and GPG keys
   - Click "New SSH key"
   - Paste your key and save

## Connecting Git to GitHub

Test your connection:
```bash
ssh -T git@github.com
```

You should see a message confirming successful authentication.
