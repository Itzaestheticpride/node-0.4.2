# node-0.4.3 Gensyn Setup Guide

## 1. Be ROOT user

```bash
sudo -i
```

IF you are running on a fresh VPS, follow 1.1 and 1.2:

## 1.1 DOWNLOAD DEPENDENCIES
```bash
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
```
## 1.2 INSTALL SYSTEM PACKAGES
```bash
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl screen git yarn
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install -y yarn


```
# 2. Fix for no participation/wins or node running errors:

## 2.1 DELETE OLD FILES
```bash
sudo rm -rf rl-swarm
sudo rm -f rl-swarm-0.4.2
sudo rm -rf rl-swarm-0.4.3
sudo rm -rf rl-swarm-0.4.4
```

## 2.2 DOWNLOAD THE FILES
```bash
git clone https://github.com/gensyn-ai/rl-swarm.git
```

## 2.4 GO TO FOLDER 
```bash
cd rl-swarm
```


## 2.6 CREATE A SCREEN 
```bash
screen -S swarm
```
IF YOU WANT TO EXIT PRESS CTRL + A +D 
IF WANT TO SEE THE PROCESS OF THE NODE/LOGS
```bash
sudo -i
screen -r swarm
```

# IF YOU ALREADY HAVE YOUR PEM FILE , USE TERMIUS STFP TO SHARE IT TO THE VPS /UBUNTU/


## 2.7 
TO SHARE THE FILE TO THE NODE DIRECTORY 
# (RUN THE BELOW COMMAND  ONLY AFTER YOU HAVE TRANSFERED YOUR PEM FILE TO THE VPS )

# REPLACE USERNAME WITH YOUR VPS USERNAME
```bash
sudo cp /home/(username)/swarm.pem /root/rl-swarm-0.5.1/

```

## 2.7 RUN THE NODE
```bash
python3 -m venv .venv && source .venv/bin/activate && ./run_rl_swarm.sh
```
📬 Need help?
Message on Telegram: @rahuljaat2502











