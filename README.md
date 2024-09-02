# zsh-minimal

Document my minimal zsh setup with [oh-my-zsh](https://ohmyz.sh) + [starship](https://starship.rs) (in case I forget).

## Install oh-my-zsh

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install plugins

```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Activate the plugin in ~/.zshrc:

```
plugins=( [plugins...] zsh-syntax-highlighting zsh-autosuggestions)
```

Install [fzf](https://github.com/junegunn/fzf)

## Install starship

```sh
curl -sS https://starship.rs/install.sh | sh
# Disable venv or conda prompt
echo "export PYENV_VIRTUALENV_DISABLE_PROMPT=1" >> ~/.zshrc
conda config --set changeps1 False
# Add starship to zshrc
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
```
