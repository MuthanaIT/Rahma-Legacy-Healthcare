# Rahma Legacy Healthcare Changes
To use this repo, simply clone this repository to your local machine.
```bash
git clone https://github.com/MuthanaIT/Rahma-Legacy-Healthcare.git
cd Rahma-Legacy-Healthcare
```
Initialize the directory with git and navigate to the config and paste the following configurations.
```bash
git init
sudo vim .git/config
```
Paste the following configuration for (delta)[https://dandavison.github.io/delta/get-started.html] for easier navigation for the code changes.
```ini
[core]
    pager = delta

[interactive]
    diffFilter = delta --color-only

[delta]
    navigate = true    # use n and N to move between diff sections

    # delta detects terminal colors automatically; set one of these to disable auto-detection
    dark = true
        line-numbers = true
        side-by-side = true
    # light = true

[merge]
    conflictstyle = zdiff3
[remote "origin"]
        url = https://github.com/MuthanaIT/Rahma-Legacy-Healthcare.git
        fetch = +refs/heads/*:refs/remotes/origin/*
[user]
        name = MuthanaIT
        email = muthanaali@warithit.com
[branch "master"]
        remote = origin
        merge = refs/heads/master
```
