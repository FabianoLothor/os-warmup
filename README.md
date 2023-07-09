# os-warmup

This repository is used to store my initial settings of the operational systems
that I am used to use.

## Ubuntu

Just execute the following commands:

```bash
sudo apt update -y ; sudo apt upgrade -y

sudo apt install git

git clone --bare \
    https://gitlab.com/fabianolothor/os-warmup.git \
    ~/Repositories/personal/os-warmup/.git

git -C ~/Repositories/personal/os-warmup/.git worktree add ../main

~/Repositories/personal/os-warmup/main/warmup-ubuntu
```

