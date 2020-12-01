# Filtering

| Command                | Description |
|------------------------|-------------|
|:v/<PATTERN>/d          |Delete all lines, that do NOT match PATTERN |
|:v/foo/d                |Delete all lines that do NOT contain "foo" |
|:v/foo\|bar/d           |Delete all lines that do NOT contain "foo" or "bar" |
|u                       |Undo |
|:e!                     |Reload the file and discard all changes |

# Search and replace

| Command                | Description |
|------------------------|-------------|
| :<REGION>s//<br>- without REGION current line<br>- % the whole file ||
|:%s/ \*INFO.*Path://    |Deletes in every line in the whole file |
|:%s/foo/bar/g           |Change each 'foo' to 'bar' in all the lines. | 
|:%g/foo/d               |Delete all lines that do contain 'foo' |
|:%v/foo/d               |Delete all lines that do NOT contain 'foo' |
|:%v/\(foo\|bar\)/d      |Delete all lines that do NOT contain 'foo' or 'bar' |

# Registers

<CRL>-R*                In insert mode copy clipboard

"*y  "*p                In normal mode yank / paste to / from clipboard
"1y  "1p                In normal mode yank / paste to / from buffer "1"

# Buffer

:ls                     list all buffers
:b <tab>                tab through the buffers and select active


# Inner

ciw  diW                Change / delete inner word

ci(  ci)  ci[  ci]      Changes inner: (hallo)

# Spelling

Spelling requires spelling files from: http://ftp.vim.org/vim/runtime/spell/

  spell/de.utf-8.spl
  spell/en.utf-8.spl

The 'spell' directory is located under the 'runtimepath'. This is currently:

  U:\vimfiles\

and can be displayed with:

  echo &runtimepath

setlocal spelllang=de   Set the language for the spelling for the buffer

setlocal spell          Activate the spelling for the buffer

Select word and use 'z=' to get a recommandation.

# .vimrc

The current .vimrc can be reached by:

  $MYVIMRC 
  U:\.vimrc

# delete

  :1,.d     Delete to the beginning of the file (Current pos: .)
  :.,$d     Delete to the end of the file       (Current pos: .)

# visual select file

  ggVG      select complete file

# Diff two empty buffers
> Mark two files in the explorer and use "diff with vim"

---

> Create two empty buffers, fill in the content and start diff

  :tabnew <FILE1>
  :vnew <FILE2>
  :windo diffthis

> End diff

  :windo diffoff

> Move to the right/left window:

  <CTRL-w>RIGHT
  <CTRL-w>LEFT

---

