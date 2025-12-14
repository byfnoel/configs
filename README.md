# My Neovim configuration

## Introduction

A starting point for Neovim that is:

* Small
* Modular
* Completely Documented
* Extendable

## Installation

### Install Neovim

Install the latest stable version
['stable'](https://github.com/neovim/neovim/releases/tag/stable) and latest

### Install External Dependencies

External Requirements:

* Basic utils: `git`, `make`, `unzip`, C Compiler (`gcc`)
* [ripgrep](https://github.com/BurntSushi/ripgrep#installation),
  [fd-find](https://github.com/sharkdp/fd#installation)
* A [Nerd Font](https://www.nerdfonts.com/): optional, provides various icons
  * if you have it set `vim.g.have_nerd_font` in `init.lua` to true
* Language Setup:
  * If you want to write Typescript, you need `npm`
  * If you want to write Golang, you will need `go`
  * etc.

### Install Kickstart

> [!NOTE]
> [Backup](#faq) your previous configuration (if any exists)

Find your configuration under the following paths, depending on your OS:

| OS | PATH |
| :- | :--- |
| Linux, MacOS | `$XDG_CONFIG_HOME/nvim`, `~/.config/nvim` |

#### Recommended Step

[Fork](https://github.com/byfnoel/configs.git) this repo so that you have
your own copy that you can modify. Then install by cloning the fork to your
machine using one of the commands below, depending on your OS.

> [!NOTE]
> Your fork's URL will be something like this:
> `https://github.com/<username>/configs.git`

You likely want to remove `lazy-lock.json` from your fork's `.gitignore` file too
and track it in version control.

#### Clone the repo

> [!NOTE]
> If following the recommended step above (i.e., forking the repo), replace
> `nvim-lua` with `<your_github_username>` in the commands below

<details><summary> Linux and Mac </summary>

```sh
git clone https://github.com/byfnoel/configs.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```

### Post Installation

Start Neovim
```sh
nvim
```

That's it! Lazy will install all the plugins you have. Use `:Lazy` to view
the current plugin status. Hit `q` to close the window.

#### Read The Friendly Documentation

Read through the `init.lua` file in your configuration folder for more
information about extending and exploring Neovim. That also includes
examples of adding popularly requested plugins.

> [!NOTE]
> For more information about a particular plugin check its repository's documentation.

### FAQ

* What should I do if I already have a pre-existing Neovim configuration?
  * You should back it up and then delete all associated files.
  * This includes your existing init.lua and the Neovim files in `~/.local`
    which can be deleted with `rm -rf ~/.local/share/nvim/`
* What if I want to "uninstall" this configuration:
  * See [lazy.nvim uninstall](https://lazy.folke.io/usage#-uninstalling) information
