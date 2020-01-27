# tmux-vi-yank
Tmux copy to clipboard vi mode

## OSX Requirements

```bash
brew install reattach-to-user-namespace
```

## Linux Requirements

```bash
# debian
sudo apt install xsel

# fedora
sudo dnf install xsel
```

## Windows
Let me know if it works :smile:

## tmux.conf
Add `set -g @plugin 'casonadams/tmux-vi-yank'` to plugins in config file.  `ctrl+b I` to install.

```bash
if "test ! -d ~/.tmux/plugins/tpm" \
     "run 'git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm && ~/.tmux/plugins/tpm/bin/install_plugins'"

set -g @plugin 'casonadams/tmux-vi-yank'

run -b '~/.tmux/plugins/tpm/tpm'
```

## Usage
|Command|Result|
|-------|------|
|`ctrl+b enter`|Enter copy mode|
|`v`|vi visual selection mode|
|`shift + v`| vi line copy mode|
|`y` `enter`|Copy selected text to clipboard|

# Special Thanks to
https://github.com/gpakosz/.tmux
