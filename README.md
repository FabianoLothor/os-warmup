# os-warmup

This repository is used to store my initial settings of the operational systems
that I am used to use.

## Ubuntu

Just execute the following commands:

```bash
# For a smoke test: docker run -ti --rm ubuntu /bin/bash

PERSONAL_DIRECTORY=~/Repositories/personal
SUDO="$(sudo --version >/dev/null 2>&1 && echo 'sudo' || echo '')"

$SUDO apt -y update ; $SUDO apt -y upgrade

$SUDO apt -y install git

git clone --bare \
    https://gitlab.com/fabianolothor/os-warmup.git \
    $PERSONAL_DIRECTORY/os-warmup/.git

git -C $PERSONAL_DIRECTORY/os-warmup/.git worktree add ../main

$PERSONAL_DIRECTORY/os-warmup/main/warmup-ubuntu
```

