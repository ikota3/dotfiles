# SETUP

## Clone repo

```bash
git clone https://github.com/ikota3/dotfiles.git
cd dotfiles
```

## Github ssh

```bash
ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa_github
cp .ssh/config ~/.ssh/config
```

Go to https://github.com/settings/keys and add new SSH key.

- Windows

    ```bash
    cat ~/.ssh/id_rsa_github.pub | clip
    ```

- Linux

    ```bash
    xclip -sel ~/.ssh/id_rsa_github.pub
    ```

    Or...

    ```bash
    cat ~/.ssh/id_rsa_github.pub
    ```

After adding ssh key, run the command below.

```bash
ssh -T github
```

If you push the repo to github, and get the message below

```bash
$ git ps
Warning: Permanently added the RSA host key for IP address 'xxx.xxx.xxx.xxx' to the list of known hosts.
```

Run this command
```bash
ssh-keygen -R github.com
```
