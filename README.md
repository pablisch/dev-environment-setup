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

Install Dropbox for Keyboard Maestro macros:
```
brew install --cask  dropbox
```

NOTE: My preferred terminal profile can be found [here](https://drive.google.com/drive/folders/1PqfaIsI-swLBF5ibFG5yhHAJUCXU6crN?usp=sharing). Terminal > Preferences… > Profiles > … > import

Install VSCode (Assuming settings sync is ON, all VSCode settings sync once signed in), Slack, Zoom and iTerm (command line):
```
brew install --cask visual-studio-code
brew install --cask slack
brew install --cask zoom
brew install --cask iterm2
```
Install Oh My ZSH (command line) - currently: 
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
## JavaScript
nvm is distributed using GitHub. Find the latest version [here](https://github.com/nvm-sh/nvm#installing-and-updating).
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash # to install nvm
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
command -v nvm # to verify installation
```
Then install and run node:
```
nvm install node # here, node is an alias for the latest stable version of node
nvm use node
```
To verify install of node, run it by entering `node`.
```
npm install -g esbuild # js build tool install globally
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
## GitHub CLI
Install GitHub CLI:
```
brew install gh
gh auth login # and follow the prompts
```
Configure git, e.g. `git config –-global user.name “your name”` to configure your name. This is the basis for making other configuration changes, see [here](https://makersacademy.teachable.com/courses/makers-academy-mastery-precourse/lectures/3989157).

See my gitconfig configurations [here](https://docs.google.com/document/d/13pMs0KbL6SVWEqR7BREaDErzdEvKye507XLXTd21dW8/edit?usp=sharing).
NOTE: in the terminal, `cat .gitconfig` will show the .gitconfig file.

Set up alias’ for command line. My aliases [here](https://docs.google.com/document/d/13pMs0KbL6SVWEqR7BREaDErzdEvKye507XLXTd21dW8/edit?usp=sharing).
## Postgres
Install PostgreSQL:
```
brew install postgresql@15
brew services start postgresql@15 # and open a new terminal to open the connection
```
Additional information from Makers [here](https://github.com/makersacademy/databases/blob/main/sql_bites/01_setting_up_database.md).
## More
Install TablePlus (GUI for databases): 
```
brew install --cask tableplus
```
See [here](https://github.com/pablisch/dev-environment-setup/blob/main/configuring_tableplus.md) for [configuring TablePlus](https://github.com/pablisch/dev-environment-setup/blob/main/configuring_tableplus.md) and [Makers info](https://github.com/makersacademy/databases/blob/main/sql_bites/06_using_table_plus.md).

Install Postman (HTTP client GUI):
```
brew install --cask postman
```
BELOW are other useful apps but not directly needed for the coding environment:
```
brew install --cask google-drive 
brew install --cask gimp 
brew install --cask vlc 
brew install --cask firefox 
brew install --cask  whatsapp 
brew install --cask  balenaetcher 
```








