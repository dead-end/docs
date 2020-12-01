
# Base

```
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" .vimrc
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

" Set the leader for the mappings
let mapleader = ","

" Set the file encoding
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

" Switch on syntax highlight
syntax on

" Colors themes that are useful
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

```
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" Windows settings
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

if has("win32")

  " Use a default working directory.
  cd C:\Users\dead-end

  " Set the initial window size
  set lines=40 columns=160

  " Set the font
  set guifont=Courier_New:h10:cANSI:qDRAFT

  " Use only filename without path for tabs
  set guitablabel=%t
else

  " Unix file
  set fileformat=unix

endif
```


# Mappings

```
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" My mappings
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

" Copy the visual selection to the clipboard
" Use: "+y and: "+p
vnoremap <leader>c "+y
vnoremap <leader>p "*p

" Copy the whole file to the buffer and return to the current position
"   mq   - set mark q at the current line
"   qqVG - visual selection of the whole file
"   "+y  - copy selection to the clipboard
"   'q   - goto mark q
nnoremap <leader>a mqggVG"+y'q

" Paste clipboard in insert mode
inoremap <leader>p <C-R>*

" Create new tab
nnoremap <leader>nt :tabnew<CR>

" prev / next tab
nnoremap <F4> :tabnext<CR>
nnoremap <F3> :tabprevious<CR>
"
" Create new tab
nnoremap <leader>t :e<CR>G
nnoremap <leader>d :1,$d<CR>:w!<CR>

```

