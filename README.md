# Setup MacOS Development Environment

## Purpose
Document the applications and dependencies of my macOS development environment.

## System Preferences

Increase accessibility of the Mac Finder with the following commands:

1. Show Library folder:
```bash
chflags nohidden ~/Library
```

2. Show hidden files:
```bash
defaults write com.apple.finder AppleShowAllFiles YES
```

3. Show path bar:
```bash
defaults write com.apple.finder ShowPathbar -bool true
```

4. Show status bar:
```bash
defaults write com.apple.finder ShowStatusBar -bool true
```

5. Go to System Preferences for the following:

- Keyboard > Text > Disable “Correct spelling automatically”
- Keyboard > Text > Disable “Capitalize words automatically”
- Security and Privacy > FileVault > On — makes sure SSD is securely encrypted
- Security and Privacy > Firewall > On
- Security and Privacy > General > Allow App Store and identified developers
- File Sharing > Off


## Install and Configure Homebrew

1. Install [Homebrew](https://brew.sh/)
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Install applications and dependencies with [Homebrew Bundle](https://github.com/Homebrew/homebrew-bundle)

2. Create `Brewfile`. See [`assets/Brewfile`](assets/Brewfile) for example.
```bash
touch Brewfile
```

3. Install applications and dependencies with:
```bash
brew bundle
```

## Configure the Terminal
1. Setup iTerm2 to use the Nerd font
```
iTerm2 > Preferences > Profiles > Text > Font > Change Font
```
Select **English > Hack Nerd Font > Regular** for both **Font** and **Non-ASCII Font**

![alt tex](assets/iTerm2-font-config.png "iTerm2 Font Preferences")

2. Install powerlevel9k theme
```bash
git clone https://github.com/bhilburn/powerlevel9k.git ~/powerlevel9k
```

3. Change the default shell to Zsh.
```bash
chsh -s /bin/zsh
```

The Z-shell (Zsh) resource file, `~/.zshrc`, is a script that is run whenever you start Zsh.

4. Configure Zsh. See [`assets/.zshrc`](assests/.zshrc) for an example.

5. Download [iterm2colorschemes](https://iterm2colorschemes.com/)

6. Configure iTerm2 Color Preset
```
iTerm2 > Preferences > Profiles > Colors > Color Presets > Dracula
```

## Reference and Acknowledgments
  1. [Get your Mac setup to develop, in 2018 by Frankie Valentine](https://medium.com/@frankie.valentine/get-your-mac-setup-to-develop-in-2018-60ce20cd14e7)
  2. [iTerm2, Zsh with Powerlevel9K — Power up your terminal‘s colour scheme and productivity level! by ryanwhocodes](https://medium.com/the-code-review/make-your-terminal-more-colourful-and-productive-with-iterm2-and-zsh-11b91607b98c)