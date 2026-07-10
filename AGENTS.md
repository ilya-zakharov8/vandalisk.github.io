# Agent Instructions for vandalisk.github.io

## Git Authentication & SSH Keys

This repository belongs to the `ilya-zakharov8` GitHub account. 

Because the default `ssh-agent` and global `~/.ssh/config` on this machine are configured to prioritize keys for the `vandalisk` GitHub account, standard `git push` or `git pull` commands over SSH may fail with a "Permission denied to vandalisk" error.

**When interacting with Git for this repository, the agent MUST use the `~/.ssh/id_ed25519` key (associated with zakharuni13@gmail.com) and bypass the `ssh-agent` and SSH config.**

This is already configured locally in the repository via `git config core.sshCommand`, but if you ever need to run raw SSH commands, clone the repository again, or if the config is lost, use the following strict SSH command:

```bash
env SSH_AUTH_SOCK= ssh -i ~/.ssh/id_ed25519 -F /dev/null
```

To configure git locally if it's missing:
```bash
git config core.sshCommand "env SSH_AUTH_SOCK= ssh -i ~/.ssh/id_ed25519 -F /dev/null"
```
