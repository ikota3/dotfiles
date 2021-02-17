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

- Windows

  ```sh
  # Copy public key
  cat ~/.ssh/id_rsa_github.pub.pub | clip
  ```

- Linux

  ```sh
  # Copy public key
  xclip -sel ~/.ssh/id_rsa_github.pub.pub
  ```

After adding ssh key, run the command below.

```sh
ssh -T github
```

If you push the repo to github, and get the message below

```sh
$ git ps
Warning: Permanently added the RSA host key for IP address 'xxx.xxx.xxx.xxx' to the list of known hosts.
```

Run this command
```sh
ssh-keygen -R github.com
```
