# Vim most used features

|Command            |Description                                                                |
|---                |---                                                                        |
|esc                |command mode                                                               |
|v                  |visual mode (select a text and yank or delete it)                          |
|i                  |insert                                                                     |
|a                  |append                                                                     |
|shift+i            |insert in the beginning                                                    |
|shift+a            |insert at the end                                                          |
|yy                 |copy (yank)                                                                |
|"0p                |copy (yank) after use dd command                                           |
|p                  |paste                                                                      |
|5yy                |copy next 5 lines                                                          |
|dd                 |delete (it actually cut a line)                                            |
|5dd                |delete next 5 lines (cut 5 lines)                                          |
|"_dd               |delete (cut but sendo to a black hole)                                     |
|/pattern           |find pattern, n or shitf+n to navigate to the next or previous occurences  |
|:%s/old/new/g      |replace                                                                    |
|:%s/old/new/gc     |replace confirmation required                                              |
|:%s/old/new/gi     |replace case insensitive                                                   |
|:%s/old/new/gI     |replace force case sensitive                                               |
|:e /home/txt       |open new buffer with txt file loaded                                       |
|:ls                |list of current open buffers                                               |
|:bn                |goes to next buffer                                                        |
|:bp                |goes to previous buffer                                                    |
|:bd                |delete --(closes)-- the current buffer or commonly used `bp|bd#`           |
|:!ls               |runs bash commands inside vi, this case `ls` command                       |

## Configuration file
The configuraton file for vim is `~/.vimrc`

Just type any valid vi command for vi in the file and all new instances of vim will take this configuration on startup

```sh
" Show line number
set number

" Use 4 spaces for indentation and tabs
set tabstop=4

" Tab is actually 4 spaces instead \t
set shiftwidth=4

" Tab key insert spaces defined in shiftwidth
set expandtab

" Enable filetype-specific indent settings (recommended)
filetype plugin indent on
" Optional: enable smart indentation for C-style languages
set smartindent
```
keep
keep
original
want keepkeep
