## Generate SSH Keys

Generate a new ED25519 SSH key pair:

```
ssh-keygen -t ed25519 -C "email@example.com"
```

Or, if you want to use RSA:

```
ssh-keygen -t rsa -b 4096 -C "email@example.com"
```

Then:

```
  ssh-add ~/.ssh/<my-key>
```

Edit config file `~/.ssh/config`:

```
# GitLab.com
Host gitlab.com
  Preferredauthentications publickey
  IdentityFile ~/.ssh/<my-key>
```

Change url for remote to ssh if needed:

    git remote set-url origin git@github.com:biogluck/myrepo.git
