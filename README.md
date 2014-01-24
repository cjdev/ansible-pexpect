These are two simple scripts for wrapping ansible with pexpect allowing non-interactive ssh authentication.

If at all possible, you should use SSH keys for non interactive-auth instead.

The script simply reads the ssh username and password from ~/.ansible-ssh-auth and forwards them to the ansible process.

This is insecure for obvious reasons. Use SSH Keys instead.

`~/.ansible-ssh-auth` format:

```
username
password
```

Third party requirements:

  - python
  - pexpect
  - ansible

You can also apply the patch file to your install of pexpect in order to silent expect input (like passwords)

The patchfile currently only works against pexpect 2.4 (3.x support pending)
