# Most used tmux features

## Shortcuts

|Command        	|description        			| 
|---            	|---                			|
|tmux a         	|create a new session			|
|tmux new -s name	|create a new named `name`		|
|ctrl+b $       	|rename the actual session		|
|ctrl+d		       	|detach from a session			|
|ctrl+b w       	|list open sessions and windows		|
|ctrl+b c       	|create window      			|
|ctrl+b ,       	|rename window      			|
|ctrl+b n       	|next window        			|
|ctrl+b p       	|previeous window   			|
|ctrl+b %       	|horizontal split   			|
|ctrl+b "       	|verticar split     			|
|ctrl+b arrows  	|splits navigation  			|
|ctrl+b ctrl+arrow  |resize pane        			|

## Config file
The config file for tmux is `~/.tmux.conf`

```sh
# Disable bell
setw -g monitor-bell off

# Mouse Mode
set -g mouse on
```
