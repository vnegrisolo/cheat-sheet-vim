# vim-cheat-sheet

My Vim cheat-sheet

Vim is a simple and powerful text editor and also very customizable.

As a developer we spend a lot of time on select/cut/copy/paste and there's where vim is so efficient.

To open **vim** type:

```bash
vim <folder_or_file>
```

## file

To manipulate the current opened file:

- `:q` => quit
- `:q!` => force quit (loose changes)
- `:w` => save
- `:qw` or `:x` => save and quit
- `:w foo.bar` => save as `foo.bar`
- `:r foo.bar` => read from file `foo.bar` and paste it on new line

## folder browsing

- `s` => change file sort
- `i` => change folder display layout

## open file

- `:e` + file => open file
- `:tabedit` + file => open file in a new tab
- `:sp` + file => open file in a new horizontal split
- `:vs` + file => open file in a new vertical split
- `]f` => go to next file
- `[f` => go to previous file

## move

- `h` => left
- `j` => down
- `k` => up
- `l` => right
- `0` => beginning of line
- `^` => first character of line
- `$` => end of line
- `w` => next word
- `b` => beginning of word
- `e` => end of word
- `gg` => beginning of file
- `G` => end of file
- `:5` or `5G` => go to line 5
- `<Ctrl>i` => jump to next cursor location
- `<Ctrl>o` => jump to previous cursor location
- `%` => go to matching openning/closing: `()[]{}<>`

## panes and tabs

- `gt` => go to next tab
- `gT` => go to previous tab
- `<Ctrl>w` + `h` => go to left pane
- `<Ctrl>w` + `j` => go to down pane
- `<Ctrl>w` + `k` => go to up pane
- `<Ctrl>w` + `l` => go to right pane
- `<Ctrl>w` + `H` => move current pane to left pane
- `<Ctrl>w` + `J` => move current pane to down pane
- `<Ctrl>w` + `K` => move current pane to up pane
- `<Ctrl>w` + `L` => move current pane to right pane
- `<Ctrl>w` + `w` => go to next pane inside the tab
- `<Ctrl>w` + `o` => close all panes from current tab except current pane
- `<Ctrl>w` + `r` => rotate panes inside current tab
- `<Ctrl>w` + `T` => move current pane to a new tab
- `<Ctrl>w` + `5+` => increase 5 lines height on current pane
- `<Ctrl>w` + `5-` => decrease 5 lines height on current pane
- `<Ctrl>w` + `=` => normalize pane sizes

## insert mode

- `i` => under cursor
- `I` => beginning of line
- `a` => append cursor
- `A` => append to the end of line
- `o` => new line
- `O` => new previous line
- `<Esc>` => exit insert mode
- `yo` => new line with paste option
- `yO` => new previous line with paste option

## visual mode

- `v` + move command => select whatever move command defines
- `V` => select the whole line
- select text + `p` => replace selected text with yanked text
- `gv` => re-select last visual selection
- `p` => paste will replare the selected text

## visual block mode

- `<Ctrl>v` => visual **block** mode
- `<Ctrl>v` + move command + `I` => preppend text into multiple lines
- `<Ctrl>v` + move command + `A` => append text into multiple lines
- `gv` => re-select last visual selection
- `o` => change cursor to its diagonal
- `O` => change cursor to opposite side
- `p` => paste will append to the selected text

## cut

- `d` + move command => cut whatever move command defines
- `d$` or `D` => cut to the end of line
- `dl` or `x` => cut next character
- `dh` or `X` => cut previous character
- `dd` => delete whole line and new line character
- `0d$` => delete whole line content

## copy

- `y` + mode commmand => copy whatever move command defines
- `y$` or `Y` => copy to the end of line
- `yy` => copy whole line and new line character
- `0y$` => copy whole line content

## paste

- `p` => paste after
- `P` => paste before

## registers

- `:registers` or `:reg` => list all cut/copy/macro/special registers

## change => replace and set insert mode

- `c` + move command => change whatever mode command defines and set insert mode
- `c$` or `C` => change to the end of line
- `cl` or `s` => change character under cursor
- `0c$` or `cc` or `S` => change the whole line

## replace => replace and keep normal mode

- `r` => replace a character

## undo / redo

- `u` => undo
- `<Ctrl>r` => redo

## search

- `/foo` => search for `foo`
- `?foo` => search backwards for `foo`
- `n` => next search result
- `N` => previous search result
- `*` => search for the word under the cursor
- `#` => search backwards for the word under the cursor

## indent

- `>` + move command => add indentation
- `<` + move command => remove indentation

## find and replace

- `%s/foo/bar/gc` => find all `foo` and prompt for replace to `bar` in the whole file

## commands

- `:!ls` => execute shell command `ls`

## arglist => run commands to multiple files

- `:arg` => list files in arglist
- `:argdelete *` => clean arglist
- `:argadd **/*.rb` => add files to arglist
- `:argdo %s/foo/bar/gc` => replace **foo** by **bar** in arglist
- `:argdo update` => save changes to arglist
- `:argdo undo` => undo changes to arglist
- `[a` => go to the previous file in arglist
- `]a` => go to the next file in arglist
- `[A` => go to the first file in arglist
- `]A` => go to the last file in arglist

## plugins

- [tpope/vim-pathogen](https://github.com/tpope/vim-pathogen)
- [altercation/vim-colors-solarized](https://github.com/altercation/vim-colors-solarized)
- [tpope/vim-surround](https://github.com/tpope/vim-surround)
- [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive)
- [godlygeek/tabular](https://github.com/godlygeek/tabular)
- [tpope/vim-commentary](https://github.com/tpope/vim-commentary)
- [tpope/vim-markdown](https://github.com/tpope/vim-markdown)
