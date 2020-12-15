# SETUP

## Clone repo

```sh
git clone https://github.com/ikota3/dotfiles.git
cd dotfiles
```

## Github ssh

```sh
ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa_github.pub
cp .ssh/config ~/.ssh/config
```

Go to https://github.com/settings/keys and add new SSH key.

```sh
# Copy public key
cat ~/.ssh/id_rsa_github.pub | clip
```

After adding ssh key, run the command below.

```sh
ssh -T github
```
