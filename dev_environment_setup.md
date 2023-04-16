# Setting dev environment from scratch OS

It is likely to get to this point, you will already have installed Homebrew and Chrome, if not…

Install homebrew: 
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
NOTE: This automatically install xcode command line tools.

Install Chrome: 
```
brew install --cask google-chrome
```

NOTE: Makers’ setup guide [here](https://github.com/makersacademy/getting-started/blob/main/setting-up-your-mac.md).

Suggested order from this point…

Setup keyboard maestro - all details [here](https://docs.google.com/document/d/10Tu7gZg3YSOjEJppylCtM4W_PvpOlSa6TabENkKWP18/edit?usp=sharing).

NOTE: My preferred terminal profile can be found [here](https://drive.google.com/drive/folders/1PqfaIsI-swLBF5ibFG5yhHAJUCXU6crN?usp=sharing). Terminal > Preferences… > Profiles > … > import

Install VSCode (Assuming settings sync is ON, all VSCode settings sync once signed in), Slack, Zoom and iTerm (command line):
```
brew install --cask visual-studio-code
rew install --cask slack
brew install --cask zoom
brew install --cask iterm2
```
Install Oh My ZSH (command line) - currently: 
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Install RVM (Ruby version manager) - see my notes here rather than the Makers’ guide.
Assuming that homebrew and xcode command line tools are already installed.
Then, from here, brew install gnupg   .
Then gpg --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB   .
Then to install rvm itself: \curl -sSL https://get.rvm.io | bash -s stable   .
Then, from here, source ~/.rvm/scripts/rvm   .
To install the latest stable version of Ruby:
rvm get master to update the known list of Ruby versions which always seems to be way behind.
rvm list known to show new list of available stable versions
rvm install 3.2.2  <= example code to install version 3.2.2
To install Ruby version 3.0.2, rvm install 3.0.2   .
For documentation, run, rvm docs generate-ri   .
To install Ruby version 2.7.3, rvm install 2.7.3   .
If more than one version was installed you may choose to rvm –default use 3.2.2 to nominate a default version.

Install GitHub CLI - brew install gh
Then gh auth login and follow the prompts.
Configure git, e.g. git config –-global user.name “your name” to configure your name. This is the basis for making other configuration changes, see here.   .
See my gitconfig configurations here.
NOTE: in the terminal, cat .gitconfig will show the .gitconfig file.

Set up alias’ for command line. My aliases here.

Install PostgreSQL - brew install postgresql@15 followed by brew services start postgresql@15 and open a new terminal to open the connection.
Additional information from Makers here.

Install TablePlus (GUI for databases) - brew install --cask tableplus    .
See below for configuring TablePlus and Makers info.

Install Postman (HTTP client GUI) - brew install --cask postman    .

BELOW are other useful apps but not directly needed for the coding environment

Install Google Drive (optional) - brew install --cask google-drive   .

Install gimp (graphics editor) (optional) - brew install --cask gimp   .

Install vlc (media player) (optional) - brew install --cask vlc   .

Install firefox (internet browser) (optional) - brew install --cask firefox   .

Install whatsapp (optional) - brew install --cask  whatsapp   .

Install etcher (optional) - brew install --cask  balenaetcher   .


Setting up TablePlus
Open TablePlus and right-click to start a  new connection:

Choose PostgreSQL (for PostgreSQL obviously):

The default values should work fine:

Every time I have done this, I have got an error that the database <username>, e.g. pablojoyce, does not exist. 

To fix this, in terminal, enter createdb <username>, e.g. createdb pablojoyce. Then try again to open the new connection.







