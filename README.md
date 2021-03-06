# wl-clipboard-manager

This is a simple wrapper over [wl-clipboard](https://github.com/bugaevc/wl-clipboard) that implements a clipboard manager.

## Features

- Preview window for multi-line entries (even somewhat colorized)
- Picture preview using kitty icat protocol

![demo](https://user-images.githubusercontent.com/1177900/82936718-4da4b100-9f8f-11ea-9dd5-c49b0726e825.gif)

## Dependencies

It is currently heavily dependent on specific tools that I use, but I don't oppose making the script more generic - if there is an interest, just open a PR and let's discuss!

- [dmenu-term](https://github.com/maximbaz/dmenu-term) - my own `dmenu` implementation that allows providing `\0`-separated strings (important for multi-line entries) and custom preview (for colorizing the text, or image preview)
- [bat](https://github.com/sharkdp/bat) - for colorizing text
- [fzf](https://github.com/junegunn/fzf) - current preview syntax depends on `--preview-window` from `fzf`
- [sqlite3](https://www.sqlite.org) - to store clipboard entries
- [python](https://www.python.org) - to retrieve entries from database

## Installation

On Arch Linux you can use [wl-clipboard-manager](https://aur.archlinux.org/packages/wl-clipboard-manager/) package.

Alternatively, use `sudo make install`.

## Usage

- Start the daemon by running `wl-clipboard-manager daemon` or a systemd user service
- Launch dmenu using `wl-clipboard-manager dmenu`
- To copy sensitive text without saving it in clipboard history, use `wl-clipboard-manager lock; <your-command>; wl-clipboard-manager unlock`
