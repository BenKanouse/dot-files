# dot-files

## Installing dotfiles

```
cd ~/
echo 'alias dotfiles="/usr/bin/git --git-dir=$HOME/.dotfiles.git/ --work-tree=$HOME"' >> $HOME/.zshrc
source ~/.zshrc
echo ".dotfiles.git" >> .gitignore
git clone --bare https://www.github.com/username/repo.git $HOME/.dotfiles.git
dotfiles checkout
dotfiles config --local status.showUntrackedFiles no
```

## Items to install

### Homebrew https://brew.sh/

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

brew install postgresql
brew services start postgresql
brew cask install atom
brew cask install sublime-text
brew install neovim
brew install tmate
brew install neovim
# install https://github.com/junegunn/vim-plug
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
# Then Run `:PlugInstall` inside of nvim.
brew install fzf
$(brew --prefix)/opt/fzf/install
brew install ag
```

### rvm

Follow the instructions here: https://rvm.io/rvm/install

### ohmyzsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

NOTE: this will overwrite the .zsh file so you might need to consolidate your old file and the new one created.

NOTE: there are some prerequisites that I happened to have already installed for more information read their github page https://github.com/ohmyzsh/ohmyzsh
