# Mappings

```
" Set the leader for the mappings
let mapleader = ","

" Copy the visual selection to the clipboard
" Use: "+y and: "+p
vnoremap <leader>c "+y
vnoremap <leader>p "*p

```

# Auto Commands

The general form is:
```
autocmd <EVENT> <FILE-TYPE> <COMMAND

```

Examples:
```
autocmd BufWritePre *.py    %s/\s\+$//e

autocmd BufEnter    *.en.*  setlocal spelllang=en spell
```
