node-0.4.2
update your node here follow the readme file 
############





wget https://github.com/gensyn-ai/rl-swarm/archive/refs/tags/v0.4.2.tar.gz
######

now extract the tar file of the node 





############




tar -xvzf v0.4.2.tar.gz



#####




then into the dir 




##############




cd rl-swarm-0.4.2




######
 
 
 
 
run the node 



python3 -m venv .venv && source .venv/bin/activate && ./run_rl_swarm.sh



#####


here starts the guide to twek the config for you cpu , this is for my specs 32 gb ram , and 16/8cpu

cd rl-swarm-0.4.2




nano cd hivemind_exp/configs/mac/grpo-qwen-2.5-0.5b-deepseek-r1.yaml 



changes the values to this 
model_revision: main
torch_dtype: float32
bf16: false
tf32: false


gradient_checkpointing: false




save_steps: 20


( if there are errrors of no input please change the max steps to 5 ) 



















############








