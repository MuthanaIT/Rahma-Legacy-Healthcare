# Rahma Legacy Healthcare Changes
To use this repo, simply clone this repository to your local machine.
```bash
git clone https://github.com/MuthanaIT/Rahma-Legacy-Healthcare-Changes.git
cd Rahma-Legacy-Healthcare-Changes
```
Initialize the directory with git and navigate to the config and paste the following configurations.
```bash
git init
git remote add clean clean
git remote add custom
git fetch clean
git fetch custom
sudo vim .git/config
```
Paste the following configuration for [delta](https://dandavison.github.io/delta/introduction.html) for easier navigation for the code changes.
```ini
[core]
    pager = delta

[interactive]
    diffFilter = delta --color-only

[delta]
    navigate = true    # use n and N to move between diff sections

    # delta detects terminal colors automatically; set one of these to disable auto-detection
    dark = true
    # light = true
    line-numbers = true
    side-by-side = true

[merge]
    conflictstyle = zdiff3
```
How to use delta with specifying the file extensions needed and filtering out changes in file modes.
```bash
git diff clean/master custom/master -- '*.py' '*.js' '*.json' | sed '/^diff --git a\/.* b\/.*/{N;N;d;}' | delta
```
