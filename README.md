node-0.4.4 gensyn 
1. Be ROOT user 

```sudo -i```

IF you are running on fresh vps follow 1.1 and 1.2 
1.1 DOWNLOAD DEPENDENCIES 
```curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash```
1.2 DOWNLOAD DEPENDENCIES 
```sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl screen git yarn && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list && sudo apt update && sudo apt install -y yarn```

For all who are facing no participation/wins or error while node running follow froom 2.1 
2.1 DELETE THE OLD DATA AND FILES 
```sudo rm -rf rl-swarm```
```sudo rm -f rl-swarm-0.4.2```
```sudo rm -rf rl-swarm-0.4.3```
```sudo rm -rf rl-swarm-0.4.4```

2.2 clone the files 
```wget https://github.com/gensyn-ai/rl-swarm/archive/refs/tags/v0.4.4.tar.gz```
2.3 extract the files 
```tar -xvzf v0.4.4.tar.gz```

2.4 go into the folder 
```cd rl-swarm-0.4.4```
2.5 edit your config files (for cpu only and google vps )
```nano hivemind_exp/configs/mac/grpo-qwen-2.5-0.5b-deepseek-r1.yaml```

# FOLLOW THESE EDITS AND BELOW 
scroll up and down with your arrow keys and go to the following for the edit 
1. torch_dtype: float32
2.gradeint_checkpointing: False
3.per_device_batch_size: 1
#CLOSE THIS NANO SCREEN WITH CTRL+X THEN PRESS 'Y' THEN 'ENTER'

2.6 run the node
```python3 -m venv .venv && source .venv/bin/activate && ./run_rl_swarm.sh```

MSG TELEGRAM ```rahuljaat2502``` for any issues 
