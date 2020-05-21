# wl-clipboard-manager

This is a simple wrapper over [wl-clipboard](https://github.com/bugaevc/wl-clipboard) that implements a clipboard manager.

## Features

- Preview window for multi-line entries (even somewhat colorized)
- Picture preview using [vui](https://github.com/atanunq/viu)

![demo](https://user-images.githubusercontent.com/1177900/82594404-51f25800-9ba4-11ea-9242-0278100964ea.gif)

## Dependencies

It is currently heavily dependent on specific tools that I use, but I don't oppose making the script more generic - if there is an interest, just open a PR and let's discuss!

- [dmenu-term](https://github.com/maximbaz/dmenu-term) - my own `dmenu` implementation that allows providing `\0`-separated strings (important for multi-line entries) and custom preview (for colorizing the text, or image preview)
- [viu](https://github.com/atanunq/viu) - for image preview that can work in a terminal
- [bat](https://github.com/sharkdp/bat) - for colorizing text
- [fzf](https://github.com/junegunn/fzf) - current preview syntax depends on `--preview-window` from `fzf`
