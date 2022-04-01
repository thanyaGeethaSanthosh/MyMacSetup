# MyMacSetup

## Chrome / Brave / Firefox
- Click [here](https://www.google.com/chrome/?brand=CHBD&gclsrc=ds&gclsrc=ds) to Install _**Chrome**_
- Click [here](https://brave.com/download/) to Install _**Brave**_
- Click [here](https://www.mozilla.org/en-US/firefox/new/) to Install _**Firefox**_

### Plugins for Chrome  
1. [Lastpass](https://www.mozilla.org/en-US/firefox/new/)
2. [Octotree](https://chrome.google.com/webstore/detail/octotree-github-code-tree/bkhaagjahfmjljalopjnoealnfndnagc)

### Plugins for Firefox
1. [Lastpass](https://addons.mozilla.org/en-US/firefox/addon/lastpass-password-manager/)
2. [Oktotree](https://addons.mozilla.org/en-US/firefox/addon/octotree/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)
 
 ***
 ### Copy clip
 [CopyClip](https://apps.apple.com/in/app/copyclip-clipboard-history/id595191960?mt=12)
***
### Bitwarden Password Manager
[Bitwarden](https://apps.apple.com/us/app/bitwarden-password-manager/id1137397744)
 
 ## Iterm
 - Click [here](https://www.iterm2.com/downloads.html) to Install _**Iterm2**_
 
 ***
 
 ## Home Brew
- Install _**Home Brew**_
by running this scipt on the terminal ([Reference](https://brew.sh/))
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
- Run these two commands in your terminal to add Homebrew to your PATH:
```
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/thanyac/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"
 ```
 
***
 
 ## Zsh [(Reference)](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
  - Install _**zsh**_
  ```
  brew install zsh
  ```
  - Make _**zsh**_ as *default shell*
  ```
  chsh -s /usr/local/bin/zsh
  ```
  - Get .zshrc file [here](https://github.com/charliechaplinn/MyMacSetup/blob/main/.zshrc)
  - Add this file as ```~/.zshrc```
  
***
  
 ## Oh My Zsh [(Reference)](https://github.com/ohmyzsh/ohmyzsh)
  - Install _**ohmyzsh**_
  ```
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended"
  ```
  
***

 ## Powerlevel10k [(Reference)](https://github.com/romkatv/powerlevel10k#oh-my-zsh)
 - Install _**Powerlevel10k**_
    * Install _**Manually**_
    ```
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
    echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc
    ```
    _**OR**_
    
    * Using _**ohmyzsh**_
    ```
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
    ```
    _**OR**_
    * Using _**Home Brew**_
    ```
    brew install romkatv/powerlevel10k/powerlevel10k
    echo 'source /usr/local/opt/powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc
    ```
 - Configure _**Powerlevel10k**_
 ```
 p10k cofigure (sometimes need to restart before this)
 ```
 
 ***
 
 ## Zsh Auto Suggestion
 - Install _**zsh Autho suggestion**_ [(Reference)](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)
    * Install _**Mannually**_
    ```
    git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
    ```
    then add the following to your .zshrc
    ```
    source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
    ```
    _**OR**_
    
    * Using _**oh my zsh**_
    ```
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```
    then add this line in your .zshrc
    ```
    plugins=(zsh-autosuggestions)
    ```

***

## Zsh Syntax Highlighing
- Install _**zsh syntax highlighting**_ [(Reference)](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
    * Install _**Mannually**_
    ```
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
    echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
    ```
    _**OR**_
    
    * Using _**oh my zsh**_
    ```
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    ```
    then
    ```
    plugins=(zsh-syntax-highlighting)
    ```
***

## Vim
- Get vim configuration file [here](https://github.com/charliechaplinn/MyMacSetup/blob/main/.vimrc)
- Add this file as ```~/.vimrc```

***
    
## VS Code
- Click [here](https://code.visualstudio.com/) to Install _**VS Code**_
  ### Extensions
  - Code Spell Checker
  - ES Lint
  - Git History
  - Git Lens
  - Prettier
  - C/C++
  - Quokka.js
  - SQLite
  
  ### Theme
  - Molokai (Dark)
  
***

## ShiftIt
  - Install _**ShiftIt**_ [(Reference)](https://github.com/fikovnik/ShiftIt)
  ```
  brew cask install shiftit
  ```
***

## Github SSH configuration
- Create a directory .ssh in your home if it is not existing.
```
mkdir $HOME/.ssh
```
- Copy your Github email id (the email id provided by github)
- Generate your SSH key pair
```
ssh-keygen -t rsa -b 4096 -C <your@email.com>
```
- Verify ```id_rsa``` and ```id_rsa.pub``` are generated in .ssh directory
```
ls -al ~/.ssh 
```
- Add your SSH key to ssh-agent
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```
- Copy your public SSH key
```
cat ~/.ssh/id_rsa.pub | pbcopy
```
- Add the publich SSH key to github
- Test your authentication
```
ssh -T git@github.com
```
- Give necessary confirmation if it asks for
- [Reference](https://www.freecodecamp.org/news/git-ssh-how-to/)

***

## Other Applications

- [**Slack**](https://slack.com/intl/en-in/downloads/mac)
- [**Discord**](https://discord.com/download)
- [**Zoom**](https://zoom.us/download)
- [**Evernote**](https://evernote.com/download)
- [**Node.js**](https://nodejs.org/en/download/)
- [**Postman**](https://www.postman.com/downloads/)
- [**XMind**](https://www.xmind.net/download/)
- [**VLC Player**](https://www.videolan.org/vlc/download-macosx.html)
- [**Google Backup**](https://www.google.com/intl/en-GB_ALL/drive/download/backup-and-sync/)
- [**Virtual Box**](https://www.virtualbox.org/wiki/Downloads)

## Other Tools

- **nvm**
`brew install nvm)`
- **docker**
`brew install docker)`
- **Autojump**
`brew install autojump`

## Other Applications from Apple App Store

- **Bandwidth+**
- **CopyClip**
- **Imovie**

#### More reference

[mac setup doc](https://www.robinwieruch.de/mac-setup-web-development/)
