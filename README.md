# skyline.vim

skyline.vim is a simple statusline plugin for Vim.

It is a much slimmer alternatives to plugins like [powerline](https://github.com/powerline/powerline), [vim-airline](https://github.com/vim-airline/vim-airline), or [lightline.vim](https://github.com/itchyny/lightline.vim). But, of course, it is not as feature-packed. That being said, if you are looking for a minimal, functional statusline that expands upon (and is easier to configure than) the default `:h statusline`, look no further.

The notable features of `skyline.vim` are:

* a dynamic mode module, whose color and text changes to indicate your editing mode
* word and line count modules, perfect Vimmers that are writers
* a git branch module, supported by [vim-fugitive](https://github.com/tpope/vim-fugitive) or plugin-less
* show and hide many modules at will with simple `g:skyline*` variables

## Installation

### [vim-plug](https://github.com/junegunn/vim-plug)

1. Add to your `.vimrc` or `init.vim`

```
Plug 'ourigen/skyline.vim'
```

2. Install with `:PlugInstall`

### [Native `:packadd`](https://vimhelp.org/repeat.txt.html#packages)

```sh
### Vim ###
mkdir -p ~/.vim/pack/bundle/start
cd ~/.vim/pack/bundle/start
git clone https://github.com/ourigen/skyline.vim
# generating helptags for `:h skyline.vim`
vim -u NONE -c "helptags skyline.vim/doc" -c q

### NeoVim ###
mkdir -p  ~/.config/nvim/pack/bundle/start
cd ~/.config/nvim/pack/bundle/start
git clone https://github.com/ourigen/skyline.vim
# generating helptags for `:h skyline.vim`
nvim -u NONE -c "helptags skyline.vim/doc" -c q
```

## Options

* `g:skyline_gitbranch` Set `let g:skyline_gitbranch = 1` if you want to show the branch of your file. Defaults to 0.

* `g:skyline_path` Set `let g:skyline_path = 0` if you only want the tail (file name) of the path. Defaults to 1 for full relative path.

* `g:skyline_preview` Set `let g:skyline_preview = 1` if you want `[Preview]` flag on applicable buffers. Defaults to 0.

* `g:skyline_fileformat` Set `let g:skyline_fileformat = 0` if you want to hide the file format. Defaults to 1.

* `g:skyline_encoding`  Set `let g:skyline_encoding = 0` if you want to hide the file encoding. Defaults to 1.

* `g:skyline_wordcount` Set `let g:skyline_wordcount = 1` if you want to show the total word count of the file / visual selection. Defaults to 0.

* `g:skyline_linecount` Set `let g:skyline_linecount = 1` if you want to show the total line count of the file. Defaults to 0.

* `g:skyline_percent` Set `let g:skyline_percent = 0` if you want to hide the percentage through file. Defaults to 1.

* `g:skyline_lineinfo` Set `let g:skyline_lineinfo = 0` if you want to hide the line : column position. Defaults to 1.

## Screenshots

### Standard Statusline
![](asset/normal.png)

### "Writer" Statusline
![](asset/writer.png)

### Dynamic Mode Module
![](asset/mode.png)

### Dynamic Word Count Module
![](asset/word.png)

## Author's Notes

* For more information, refer to the [skyline.vim documentation](doc/skyline.txt).
* This plugin is licensed under [GNU General Public License](LICENSE.md).
* This repository is a mirror of [my repository hosted on Gitlab](https://gitlab.com/maister/skyline.vim). Development will arrive at Gitlab first, but I will keep both updated.
* This plugin was my first venture into Vimscript, so there are rough edges that I am actively working to improve as I learn more.