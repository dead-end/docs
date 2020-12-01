
# Base

```
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" .vimrc
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

" Set the leader
let mapleader = ","

set fileencoding=utf-8

" enter the current millenium
set nocompatible

" show line numbers
set number

" Do not wrap lines
set nowrap

" Status line
set ruler

" expand tabs into spaces
set expandtab

" enable syntax and plugins (for netrw)
filetype plugin on

syntax on

"OK
" :colorscheme blue
" :colorscheme evening
:colorscheme desert

" show column 81 to see overflow
highlight ColorColumn guibg=Black
set colorcolumn=81
```


# Search

```
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Search options.
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

set hlsearch
set incsearch
set ignorecase

" Search a file in subfolders. Provides tab-completion
" Excample: :find hallo :find *src.sh
set path+=**

" Display all matching files when we tab complete
set wildmenu
set wildmode=full
```
