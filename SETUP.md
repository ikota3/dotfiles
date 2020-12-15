# SETUP

## Github ssh

```sh
ssh-keygen -t rsa -f ~/.ssh/id_rsa_github.pub
cp .ssh/config ~/.ssh/config
```

Go to https://github.com/settings/keys and add new SSH key.

After adding ssh key, run the command below.

```sh
ssh -T github
```