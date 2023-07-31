# os-warmup

This repository is used to store my initial settings of the operational systems
that I am used to use.

## Ubuntu

Just execute the following commands:

```bash
PERSONAL_DIRECTORY=~/Repositories/personal
SUDO="$(sudo --version >/dev/null 2>&1 && echo 'sudo' || echo '')"

$SUDO apt -y update ; $SUDO apt -y upgrade

$SUDO apt -y install git

git clone --bare \
    https://gitlab.com/fabianolothor/os-warmup.git \
    $PERSONAL_DIRECTORY/os-warmup/.git

git -C $PERSONAL_DIRECTORY/os-warmup config remote.origin.fetch "+refs/heads/*:refs/remotes/origin/*"
git -C $PERSONAL_DIRECTORY/os-warmup fetch

git -C $PERSONAL_DIRECTORY/os-warmup worktree add main -B main FETCH_HEAD

$PERSONAL_DIRECTORY/os-warmup/main/warmup-ubuntu

# To run smoke tests you can use docker:
docker pull ubuntu:latest ; docker run -ti --rm ubuntu /bin/bash
```

