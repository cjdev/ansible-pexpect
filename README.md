These are two simple scripts for wrapping ansible with pexpect allowing non-interactive ssh authentication.

If at all possible, you should use SSH keys for non interactive-auth instead.

The script simply reads the ssh username and password from ~/.ansible-ssh-auth and forwards them to the ansible process.

`~/.ansible-ssh-auth` format:

```
username
password
```

Third party requirements:

  - python
  - pexpect
  - ansible
