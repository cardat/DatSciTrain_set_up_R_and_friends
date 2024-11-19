---
layout: default
title: Git Setup
---

# Setting up Git

Git is a version control system that helps you track changes in your code.

## Windows Installation

1. Download Git from [git-scm.com](https://git-scm.com/)
2. Run the installer
3. Use the following recommended settings:
   - Use Git from Git Bash only
   - Use the OpenSSL library
   - Checkout Windows-style, commit Unix-style line endings
   - Use MinTTY
   - Enable file system caching

## Mac Installation

1. Open Terminal
2. Run `xcode-select --install`
3. Follow the prompts to install Git

## Configuration

After installation, open Terminal (Mac) or Git Bash (Windows) and run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
