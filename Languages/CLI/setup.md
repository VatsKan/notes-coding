# Configure Terminal 

### To look pretty

- install:
zsh
oh-my-zsh
iterm2
powerline fonts

- in .zshrc file can change oh-my-zsh theme to agnoster. 

- need to install [powerline fonts](https://github.com/powerline/fonts) for this theme to work properly. 
To install powerline fonts on mac, run these commands (instructions in the repo also)
```
# clone
git clone https://github.com/powerline/fonts.git --depth=1
# install
cd fonts
./install.sh
# clean-up a bit
cd ..
rm -rf fonts
```

- (note if zsh isn't your default log in terminal, will need to set this in iterm2.)

- in iterm2, go to: preferences > profiles > text.
change the font to a powerline font.

  In preferences > profiles > colors can select a different color preset. e.g. pastel


### Autocompletion

To add autocompletion feature: uncomment out ```plugins=(git z)``` in your ```.zshrc``` file. 