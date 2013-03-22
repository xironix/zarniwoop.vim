zarniwoop.vim
==============

A colorful, dark color scheme, inspired by [Jellybeans](https://github.com/nanotech/jellybeans.vim).

Designed primarily for a graphical Vim, but includes support for 256, 88, 16,
and 8 color terminals. On a 16 or 8 color terminal, replace its colors with
those in `ansi-term-colors.txt` for best results.

This script is [vimscript #4483](http://www.vim.org/scripts/script.php?script_id=4483) at Vim.org.

Scroll down for [screenshots](#screenshot)!

## Options

### Custom Highlights

If you prefer slightly different colors from what Zarniwoop defines,
you can set `g:zarniwoop_overrides` in your .vimrc to a dictionary of
custom highlighting parameters:

    let g:zarniwoop_overrides = {
    \    'Todo': { 'guifg': '303030', 'guibg': 'f0f000',
    \              'ctermfg': 'Black', 'ctermbg': 'Yellow',
    \              'attr': 'bold' },
    \}

This removes the need to edit Zarniwoop directly, simplifying
upgrades. In addition, RGB colors specified this way are run through
the same color approximation algorithm that the core theme uses, so
your colors work just as well in 256-color terminals.

If you can pick better colors than the approximator, specify them
in the `256ctermfg` and `256ctermbg` parameters to override
its choices.

### Low-Color Black (16 and 8 color terminals)

Since the background on a dark terminal is usually black already,
Zarniwoop appropriates the black ANSI color as a dark grey and
uses no color when it really wants black.

If you can’t or don’t want to change your terminal’s color
mappings, add

    let g:zarniwoop_use_lowcolor_black = 0

to your .vimrc to render “black” text as Vim’s grey (ANSI white).

## Screenshot

![zarniwoop.vim on OS X](http://dl.dropbox.com/u/698619/Pictures/GitHub/zarniwoop.png)
