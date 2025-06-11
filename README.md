# node-0.4.4 Gensyn Setup Guide

## 1. Be ROOT user

```bash
sudo -i
```

IF you are running on a fresh VPS, follow 1.1 and 1.2:

1.1 DOWNLOAD DEPENDENCIES
```bash
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
```
1.2 INSTALL SYSTEM PACKAGES
```bash
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl screen git yarn
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install -y yarn
```
