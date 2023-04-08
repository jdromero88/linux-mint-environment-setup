# Linux Mint Environment Setup

## 0 Update your System
- `sudo apt update`
- `sudo apt upgrade`

## 1 Install [VS Code](https://code.visualstudio.com/Download)
- Download the .deb
- In a terminal type: `sudo dpkg -i filename.deb`

## 2 Install Node.js v14.x and npm
- `curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -`
- `sudo apt install -y nodejs`
- Check node version `node --version`
- Check npm version `npm --version`

#### You may also need development tools to build native addons: *optional*
- `sudo apt install gcc g++ make`
#### To install the Yarn package manager, run: *optional*
- `curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null`
- `echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list`
- `sudo apt-get update && sudo apt-get install yarn`

## 3 Install build tools *optional*
- `sudo apt install -y build-essential`

## 4 Install Git and config Github
- `sudo apt install git`
- `ssh-keygen`
- `cat ~/.ssh/id_rsa.pub` then go to your github [SSH ang GPG keys page](https://github.com/settings/keys) and add the new SSH key.
- `git config --global user.email "you@example.com"`
- `git config --global user.name "Your Name"`
- Github is ready now you can clone, pull and push.

## 5 Install Homebrew
- `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

## 6 Install [nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
- `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
