# os-warmup

This repository is used to store my initial settings of the operational systems
that I am used to use.

## Ubuntu

Just execute the following commands:

```bash
sudo apt update -y ; sudo apt upgrade -y

sudo apt install git

PERSONAL_DIRECTORY=~/Repositories/personal

git clone --bare \
    https://gitlab.com/fabianolothor/os-warmup.git \
    $PERSONAL_DIRECTORY/os-warmup/.git

git -C $PERSONAL_DIRECTORY/os-warmup/.git worktree add ../main

$PERSONAL_DIRECTORY/os-warmup/main/warmup-ubuntu
```

