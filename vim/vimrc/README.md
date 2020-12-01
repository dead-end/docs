
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

" Tweaks for browsing
let g:netrw_banner=0        " disable annoying banner
let g:netrw_browse_split=4  " open in prior window
let g:netrw_altv=1          " open splits to the right
let g:netrw_liststyle=3     " tree view
let g:netrw_list_hide=netrw_gitignore#Hide()
let g:netrw_list_hide.=',\(^\|\s\s\)\zs\.\S\+'

" NOW WE CAN:
" - :edit a folder to open a file browser
" - <CR>/v/t to open in an h-split/v-split/tab
" - check |netrw-browse-maps| for more mappings
```

