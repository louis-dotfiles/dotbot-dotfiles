# Dotbot dotfiles README

This is the _installation script_ for all of my dotfiles.

It is powered by [Dotbot](https://github.com/anishathalye/dotbot) which
basycally links / copies the configuration files in the correct places. The
various configuration are stored in their own repositories, and included in
this project as [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

## Configurations

Running this dotbot config will attempt to install all of the folloing dotfiles:
- My [Alacritty terminal emulator](https://github.com/louis-dotfiles/alacritty).
- My [ZSH shell dotfiles](https://github.com/louis-dotfiles/zsh).
- My [shell aliases](https://github.com/louis-dotfiles/shell-aliases).
- My [terminal prompt configuration (Starship.rs)](https://github.com/louis-dotfiles/starship).
- My [Neovim editor](https://github.com/louis-dotfiles/neovim).
- My [Tmux configuration](https://github.com/louis-dotfiles/tmux).

## Prerequisites

You need `python3` to be installed on your system.

## Installation

```sh
git clone --recurse-submodules <this_repo_url> dotfiles
cd dotfiles
chmod +x install
./install
```

## Updating

If you want to update an existing dotfiles installation to the latest commit
on the `main` branch, all you need to do is run the `install` script again.

If you have conflicting changes on your local dotfiles, the script may fail to
update a specific configuration (e.g. neovim) but should be able to update the
rest nonetheless.

## Is that it?

Yes. It is going to pull additional dotfile git repositories from Github (as
submodules). And link each of these repo (or particular files within these
repos) to their intended place on the system. Usually in `~/.config/`.

