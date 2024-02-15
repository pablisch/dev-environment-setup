# Setting dev environment from scratch OS

This file is personal notes on setting up the dev environment as a personal tool.

## MacOS Settings

This is a good place to start. See separate `md` file, [Mac OS Settings](https://github.com/pablisch/dev-environment-setup/blob/main/macos_settings.md).

It is likely to get to this point, you will already have installed Homebrew and Chrome, if not…

## Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
NOTE: This automatically installs xcode command line tools.

## Google Chrome 
```
brew install --cask google-chrome
```

NOTE: Makers’ setup guide [here](https://github.com/makersacademy/getting-started/blob/main/setting-up-your-mac.md).

Suggested order from this point…

## Dropbox and Keyboard Maestro (and iTerm)
```
brew install --cask dropbox
brew install --cask iterm2
```
**Setup keyboard maestro** - see [this Google doc](https://docs.google.com/document/d/10Tu7gZg3YSOjEJppylCtM4W_PvpOlSa6TabENkKWP18/edit?usp=sharing).

## Install Oh My ZSH 
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Aliases for ZSH
Set up alias’ for command line. My aliases can be found in [this Google Doc](https://docs.google.com/document/d/1NFcRVQaIo6sxUpB81nq6v9t7C74MZl1j4ILKNrtp7ng/edit?usp=sharing).

## iTerm & Terminal profiles
My preferred iTerm & terminal profiles can be found [here](https://drive.google.com/drive/folders/1PqfaIsI-swLBF5ibFG5yhHAJUCXU6crN?usp=sharing). 

For iTerm: `iTerm2 > Settings > Profiles > … > import`
For Terminal: `Terminal > Settings... > Profiles > … Other Actions > Import JSON Profiles...`

## GitHub CLI
Install GitHub CLI:
```
brew install gh
gh auth login # and follow the prompts
```
Configure git, e.g. `git config –-global user.name “your name”` to configure your name. This is the basis for making other configuration changes, see [here](https://makersacademy.teachable.com/courses/makers-academy-mastery-precourse/lectures/3989157).

See my gitconfig configurations [here](https://docs.google.com/document/d/13pMs0KbL6SVWEqR7BREaDErzdEvKye507XLXTd21dW8/edit?usp=sharing).
NOTE: in the terminal, `cat .gitconfig` will show the .gitconfig file.

## nvm and Node
nvm is distributed using GitHub. Find the latest version [here](https://github.com/nvm-sh/nvm#installing-and-updating).
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash # to install nvm
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
command -v nvm # to verify installation
```
Then install and run node:
```
nvm install node # here, 'node' is an alias for the latest stable version of node
nvm use node
```
To verify install of node, run it by entering `node`.
```
npm install -g esbuild # js build tool install globally
```

## Homebrew group installs

**NOTE:** This includes some npm commands and **must** only be run after installing node and npm.
If you wish to install individual packages, see [here](https://github.com/pablisch/dev-environment-setup/blob/main/individual_installs.md)

```
brew install --cask visual-studio-code
brew install --cask slack
brew install --cask zoom
brew tap mongodb/brew
brew update
brew install mongodb-community@7.0
brew services start mongodb-community
npm install -g nodemon mongoose express
brew install --cask mongodb-compass
brew install postgresql@15
brew services start postgresql@15 # and open a new terminal to open the connection
brew install --cask tableplus
brew install --cask postman
brew install --cask gimp 
brew install --cask vlc 
brew install --cask firefox 
brew install --cask  whatsapp 
brew install --cask  balenaetcher 
brew install --cask  rectangle
brew install --cask epic-games
brew install --cask android-studio
# NOTE community edition of IntelliJ is shown on other apps to consider
brew install --cask intellij-idea
```

## Xcode for React Native
**Easiest to install from the App Store.**

## Visual Studio Code
Sign in and turn sync on to sync all settings.

## Intellij IDEA
If IntelliJ IDEA is installed, it will need to be registered. Currently I have a free license for 12 months through Makers. Registering can be done from the main menu and choose to log in to JetBrains account. This opens a browser page where my account details have been saved. This expires in November 2024.

## Postgres
Installed in group installs above.
Additional information from Makers [here](https://github.com/makersacademy/databases/blob/main/sql_bites/01_setting_up_database.md).

## TablePlus
Installed in group installs above.
See [here](https://github.com/pablisch/dev-environment-setup/blob/main/configuring_tableplus.md) for [configuring TablePlus](https://github.com/pablisch/dev-environment-setup/blob/main/configuring_tableplus.md) and [Makers info](https://github.com/makersacademy/databases/blob/main/sql_bites/06_using_table_plus.md).

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