## Install iTerm2:
https://iterm2.com/downloads.html

## Install ZSH:
https://ohmyz.sh/
 
## Setting up custom profile:
iTerm2 -> Preferences -> Profiles -> Add new profile -> Set as default profile

### Recommended Theme: https://github.com/wesbos/Cobalt2-iterm
Under the Colors tab import the cobalt2.itermcolors file via the Load Presets drop-down.
Open up your ZSH preferences at ~/.zshrc and change the theme variable to ZSH_THEME=cobalt2
open file using: nano ~/.zshrc  

Or use powerlevel9k: https://github.com/bhilburn/powerlevel9k
https://medium.com/@alex285/get-powerlevel9k-the-most-cool-linux-shell-ever-1c38516b0caa

### Powerline Fonts: https://github.com/powerline/fonts
### Recommended: Inconsolata
git clone https://github.com/powerline/fonts
cd fonts
./install.sh

Access the Preferences pane on the Profiles tab -> Under the Text tab change the font for each type (Regular and Non-ASCII) to 'Inconsolata for Powerline'. 

## Jump around folders using z:
https://github.com/rupa/z

## Install trash:
npm install --global trash-cli

## Setting up plugins:
Open .zshrc file to setup plugins:
nano ~/.zshrc  

## Folder with ZSH Themes & Templates:
open ~/.oh-my-zsh

## A video series on learning modern command line:
https://commandlinepoweruser.com/

## ZSH supported Command:
take test1 -> creates a folder and then cd to that newly created folder 

**Sample .zshrc**

[Sample .zshrc](https://github.com/arkhangelsk/STT-Notes/blob/master/zshrc%20(sample-settings))


