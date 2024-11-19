# Directory structure first:
.
├── _config.yml
├── _layouts
│   └── default.html
├── assets
│   └── css
│       └── style.scss
├── index.md
├── r-installation.md
├── rstudio-setup.md
├── git-setup.md
└── github-setup.md

# _config.yml
title: Data Science Setup Guide
description: Guide for setting up R, RStudio, Git, and GitHub for data science training
url: ""
baseurl: ""
theme: minima

# Add navigation
header_pages:
  - r-installation.md
  - rstudio-setup.md
  - git-setup.md
  - github-setup.md

# _layouts/default.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }} - {{ site.title }}</title>
    <link rel="stylesheet" href="{{ '/assets/css/style.css' | relative_url }}">
</head>
<body>
    <div class="container">
        <div class="sidebar">
            <h2>Navigation</h2>
            <ul>
                <li><a href="{{ '/' | relative_url }}">Home</a></li>
                <li><a href="{{ '/r-installation' | relative_url }}">R Installation</a></li>
                <li><a href="{{ '/rstudio-setup' | relative_url }}">RStudio Setup</a></li>
                <li><a href="{{ '/git-setup' | relative_url }}">Git Setup</a></li>
                <li><a href="{{ '/github-setup' | relative_url }}">GitHub Setup</a></li>
            </ul>
        </div>
        <div class="content">
            {{ content }}
        </div>
    </div>
</body>
</html>

# assets/css/style.scss
---
---

@import "{{ site.theme }}";

.container {
    display: flex;
    min-height: 100vh;
}

.sidebar {
    width: 250px;
    padding: 20px;
    background-color: #f5f5f5;
    border-right: 1px solid #ddd;
}

.content {
    flex: 1;
    padding: 20px;
}

.sidebar ul {
    list-style: none;
    padding: 0;
}

.sidebar li {
    margin-bottom: 10px;
}

.sidebar a {
    text-decoration: none;
    color: #333;
}

.sidebar a:hover {
    color: #0366d6;
}

# index.md
---
layout: default
title: Home
---

# Welcome to the Data Science Setup Guide

This guide will help you set up all the necessary tools for participating in our data science training sessions. Please follow the installation guides in order:

1. R Installation
2. RStudio Setup
3. Git Setup
4. GitHub Setup

Each guide provides detailed instructions for both Windows and Mac operating systems. If you encounter any issues during the setup process, please reach out for assistance.

# r-installation.md
---
layout: default
title: R Installation
---

# Installing R

R is the core programming language we'll be using for data analysis. Follow the instructions below for your operating system.

## Windows Installation

1. Go to [CRAN website](https://cran.r-project.org/)
2. Click on "Download R for Windows"
3. Click on "base"
4. Download the latest version of R
5. Run the installer and follow the default installation settings

## Mac Installation

1. Go to [CRAN website](https://cran.r-project.org/)
2. Click on "Download R for macOS"
3. Download the latest .pkg file for your Mac's processor (Intel or Apple Silicon)
4. Open the downloaded file and follow the installation instructions

# rstudio-setup.md
---
layout: default
title: RStudio Setup
---

# Setting up RStudio

RStudio is an Integrated Development Environment (IDE) that makes working with R much easier.

## Installation

1. Visit [RStudio Download Page](https://posit.co/download/rstudio-desktop/)
2. Download the free RStudio Desktop version for your operating system
3. Run the installer

## Recommended Settings

After installing RStudio, we recommend the following settings:

1. Tools → Global Options
   - Appearance:
     - Choose a theme (we recommend 'Tomorrow Night Blue' or 'Cobalt')
     - Font size: 12
   - Code:
     - Enable "Show line numbers"
     - Enable "Highlight selected word"
   - Pane Layout:
     - Ensure you have the following arrangement:
       - Top-left: Source
       - Top-right: Environment
       - Bottom-left: Console
       - Bottom-right: Files/Plots/Packages/Help

# git-setup.md
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

# github-setup.md
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
