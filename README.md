# Linux Mint Environment Setup
## Step 0
*Make sure everything is up to date.*
* `sudo apt-get update`
* `sudo apt-get upgrade`

###### Install Atom (text editor)
* `sudo add-apt-repository ppa:webupd8team/atom`
* `sudo apt-get update`
* `sudo apt-get install atom`


## Step 1
*Open the terminal, select Edit > Profile Preferences. Then on the Title and Command tab, check off 'Run command as login shell'*

## Step 2
*Set up group*
* `sudo groupadd npm`
* `sudo usermod -a -G npm,staff $USER`

## Step 3
*The essentials*
* `sudo apt-get -y install curl postgresql libpq-dev default-jre build-essential phantomjs`
* `curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -`
* `sudo apt-get install -y nodejs`


## Step 4
*Setting file permissions*
* `sudo chown root:staff /usr/bin`
* `sudo chmod 0775 /usr/bin`
* `sudo chown -R root:npm /usr/lib/node_modules`
* `sudo chmod 0775 /usr/lib/node_modules`

## Step 5
*Only if you are a Flatiron School you will need this to use the learn gem. Set up .netrc file for the learn gem*
* `touch ~/.netrc && chmod 0600 ~/.netrc`

## Step 6
*Installing RVM*
* `gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3`
* `\curl -sSL https://get.rvm.io | bash`
* `echo "[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" # Load RVM into a shell session *as a function*"`
* `rvm install 2.6.1`
* `rvm use 2.6.1 --default`

## Step 7
*Setting up (and getting) Ruby gems*
* `echo "gem: --no-ri --no-rdoc" > $HOME/.gemrc`
* `gem update --system`
* `gem install learn-co (Only if you are a Flatiron student)`
* `gem install phantomjs`
* `gem install pg`
* `gem install sqlite3`
* `gem install bundler`
* `gem install rails`

## Step 8
*Installing a Node Pacakge*
* `sudo npm install -g n`
* `sudo npm install -g protractor`

## Step 9
*Setting up your computer up with Github*
* `ssh-keygen`
* `cat ~/.ssh/id_rsa.pub`
* `git config --global user.email "you@example.com"`
* `git config --global user.name "Your Name"`

## Step 10
*Configure the Learn-Co gem (only if you are a Flatiron student and you need to use the learn gem)*
* `learn whoami`

## Step 11
*Adding dotfiles*
* `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/irbrc" -o "$HOME/.irbrc"`
* `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/ubuntu-gitignore" -o "$HOME/.gitignore"`
* `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/linux_bash_profile" -o "$HOME/.bash_profile"`
* `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/linux_gitconfig" -o "$HOME/.gitconfig"`
* `xed $HOME/.gitconfig`

## Step 12
*Install useful apps*
* `Chrome`
* `Slack`
* `Atom`

#### Config Postgres
* `sudo -u postgres createuser --superuser $USER`
* `sudo -u postgres createdb $USER`

*I used the Ubuntu Environment Setup from Flatiron-School and adapted for Linux Mint.
 Here is the link for the Ubuntu Environment Setup*
[Ubuntu Environment Setup](https://github.com/learn-co-curriculum/linux-env-setup)
