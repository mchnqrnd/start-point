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
|p                  |pate                                                                       |
|5yy                |copy next 5 lines                                                          |
|5dd                |delete next 5 lines                                                        |
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

