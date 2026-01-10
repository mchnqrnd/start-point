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

### Server best practices configuration
Disable password connection
```sh

```


