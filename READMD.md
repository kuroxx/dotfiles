# Dotfiles

## 1. Shell Configuration

To configure the zsh shell with oh-my-zsh, Powerlevel10k theme, and the syntax highlighting and auto-suggestions plugins, run the following commands:

### Install oh-my-zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Install Powerlevel10k theme

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
sed -i -e '11s/.*/ZSH_THEME="powerlevel10k\/powerlevel10k"/' ~/.zshrc
source ~/.zshrc
```

Follow instructions to configure as desired.

### Install plugins

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
sed -i -e '80s/.*/plugins=(git zsh-syntax-highlighting zsh-autosuggestions)/' ~/.zshrc
source ~/.zshrc
```

**Note:** If Python is already installed via conda, run the command `~/{insert-conda-installation-path}/bin/conda init zsh` to update `.zshrc`

## 2. Vim Configuration

Run the following commands to populate Vim config:

```bash
cd ~
ln -s ./dotfiles/.vimrc .vimrc
```

## 3. TMUX Configuration

Basic configuration to preserve terminal colors in Vim:

```bash
cd ~
ln -s ./dotfiles/.tmux.conf .tmux.conf
```

## 4. Git Configuration

Set up Git with useful aliases, settings, and configurations:

```bash
cd ~
ln -s ./dotfiles/.gitconfig .gitconfig
```
