# Homebrew Individual Installs

This is an alternative to the mass installs shown in the README.md. This is for those who want to install individual packages. It assumes that Google Chrome, Dropbox and iTerm are already installed.

## GitHub CLI
Install GitHub CLI:
```
brew install gh
gh auth login # and follow the prompts
```
Configure git, e.g. `git config –-global user.name “your name”` to configure your name. This is the basis for making other configuration changes, see [here](https://makersacademy.teachable.com/courses/makers-academy-mastery-precourse/lectures/3989157).

See my gitconfig configurations [here](https://docs.google.com/document/d/13pMs0KbL6SVWEqR7BREaDErzdEvKye507XLXTd21dW8/edit?usp=sharing).
NOTE: in the terminal, `cat .gitconfig` will show the .gitconfig file.

## Install Oh My ZSH 
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Aliases for ZSH
Set up alias’ for command line. My aliases can be found in [this Google Doc](https://docs.google.com/document/d/13pMs0KbL6SVWEqR7BREaDErzdEvKye507XLXTd21dW8/edit?usp=sharing).

## Install VSCode
Sign in and turn sync on to sync all settings.
```
brew install --cask visual-studio-code
```

## Intellij IDEA
This is for the Ultimate edition. Code for the Community edition is lower down the page.
```
brew install --cask intellij-idea
```
If IntelliJ IDEA is installed, it will need to be registered. Currently I have a free license for 12 months through Makers. Registering can be done from the main menu and choose to log in to JetBrains account. This opens a browser page where my account details have been saved. This expires in November 2024.

## Install Slack, Zoom and iTerm
```
brew install --cask slack
brew install --cask zoom
```

## Nodemon, MongoDB, Mongoose for MERN stack
To install all of the below and start the MongoDB server. For an individual breakdown of the commands, see [here](https://github.com/pablisch/dev-environment-setup/blob/main/mongodb_etc.md)
```
brew tap mongodb/brew
brew update
brew install mongodb-community@7.0
brew services start mongodb-community
npm install -g nodemon mongoose express
brew install --cask mongodb-compass
```

## Postgres
Install PostgreSQL:
```
brew install postgresql@15
brew services start postgresql@15 # and open a new terminal to open the connection
```
Additional information from Makers [here](https://github.com/makersacademy/databases/blob/main/sql_bites/01_setting_up_database.md).

## TablePlus
Install TablePlus (GUI for databases): 
```
brew install --cask tableplus
```
See [here](https://github.com/pablisch/dev-environment-setup/blob/main/configuring_tableplus.md) for [configuring TablePlus](https://github.com/pablisch/dev-environment-setup/blob/main/configuring_tableplus.md) and [Makers info](https://github.com/makersacademy/databases/blob/main/sql_bites/06_using_table_plus.md).

## Postman
```
brew install --cask postman
```

## Xcode for React Native
**Easiest to install from the App Store.**

## Android Studio for React Native
```
brew install --cask android-studio
```

## Other normal apps to install depending on usage
```
brew install --cask gimp 
brew install --cask discord
brew install --cask vlc 
brew install --cask firefox 
brew install --cask  whatsapp 
brew install --cask  balenaetcher 
brew install --cask  rectangle
brew install --cask epic-games
```

## Others apps to consider
```
brew install --cask eqmac
brew install --cask  google-drive
# below is the community edition of IntelliJ
brew install --cask intellij-idea-ce
```

## Ruby
Install RVM (Ruby version manager) - see my notes [here](https://docs.google.com/document/d/16G3-ixyX0yHJAy9MevqVIQ8Km5e01OAUD8epqg4h7v0/edit#heading=h.yo6xrg8msfu7) rather than the Makers’ guide.

Assuming that homebrew and xcode command line tools are already installed.
Then, from here, 
```
brew install gnupg
gpg --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```
Then to install rvm itself: 
```
\curl -sSL https://get.rvm.io | bash -s stable 
source ~/.rvm/scripts/rvm 
```
To install the latest stable version of Ruby:
```
rvm get master # to update the known list of Ruby versions
rvm list known # to show new list of available stable versions
rvm install 3.2.2 # <= example code to install version 3.2.2
rvm install 3.0.2 # <= example code to install version 3.0.2
rvm docs generate-ri # to install documentation
rvm –default use 3.0.2 # to nominate 3.0.2 as the default version
```