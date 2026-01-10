# Main points of ssh

Open ssh is the standard of Linux administration application.

Folder with keys and with authorized keys
~/.ssh/

Authorized keys are the keys that are allowed to connect to the server. In my note this file is empty because no one can access.

## Commands
### Basic usage to connect
When no key is configured the password will be required. It is a best practice disable password connection after the key is configured.
```sh
ssh user@xxx.xxx.xxx.xxx
```

If a key is configured the key passphrase will prompt, assuming the key has a passphrase, otherwise the connection just happens automatically.
```sh
ssh -i ~/.ssh/key_name user@xxx.xxx.xxx.xxx
```

### Saving a passphrase
ssh agent must be running in background
```sh
eval $(ssh-agent)
ssh-add ~/.ssh/key_name
```

Creating an alias to this command in the .bashrc file
```sh
alias sshadd='eval $(ssh-agent) && ssh-add'
```

### Managing keys
Generate key
```sh
ssh-keygen -t ud25519 -C "key comment"
```

Copy a key for an server
```sh
ssh-copy-id -i ~/.ssh/key_name.pub xxx.xxx.xxx.xxx
```

Config file `~/.ssh/config`
```sh
Host server-nickname
     HostName xxx.xxx.xxx.xxx
     IdentityFile ~/.ssh/key-name
     User server-username
```

```sh
ssh server-nickname
```

### Server configuration
Ensuring that ssh is installed and running
The package to install if necessary is `openssh-server`
```sh
ssh -V
systemctl status sshd # and all variants: `reload`, `start` and `enable` to ensure it starts on boot.
```

Disable password connection editing the file `/etc/ssh/sshd_config`
```sh
PasswordAuthentication no
PubKeyAuthentication yes
PermitRootLogin no
```


