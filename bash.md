# Bash main commands and customizations

## Commands


## Customizations
Create alias to add keys into ssh agent

```sh
alias sshagit='eval $(ssh-agent) && ssh-add ~/.ssh/git'
```

Git branch in the terminal prompt
```sh
# Function to parse the git branch name
# How to use \[\e[0;35m\]($(parse_git_branch))\[\e[0m\]
# This line shows the git branch in cyan
parse_git_branch() {
    git branch --show-current 2>/dev/null
}

# The important code here is: \[\e[0;35m\]$(parse_git_branch)\[\e[0m\]
# 35m is the color and 0m backs to default color
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] \[\e[0;35m\]$(parse_git_branch)\[\e[0m\]\$ \n> '
```

