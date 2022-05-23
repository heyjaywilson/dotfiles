# dotfiles
My dot files I use for various macOS configuration


## Setup

Add this code to your `~/.zshrc` file

```bash
# Fig pre block. Keep at the top of this file.
. "$HOME/.fig/shell/zshrc.pre.zsh"
for conf in "$HOME/Developer/personal/dotfiles/"*.zsh; do #make sure to change this to the directory where the dotfiles is cloned
  source "${conf}"
done
unset conf

for conf in "$HOME/Developer/personal/dotfiles/private_files/"*.zsh; do
  source "${conf}"
done
unset conf

# Fig post block. Keep at the bottom of this file.
. "$HOME/.fig/shell/zshrc.post.zsh"
```