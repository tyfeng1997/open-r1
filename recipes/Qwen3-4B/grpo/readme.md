CUDA_VISIBLE_DEVICES=0 trl vllm-serve --model Qwen/Qwen3-4B

CUDA_VISIBLE_DEVICES=1,2,3,4 ACCELERATE_LOG_LEVEL=info accelerate launch --config_file recipes/accelerate_configs/zero2.yaml --num_processes 4 src/open_r1/grpo.py --config recipes/Qwen3-4B/grpo/config.yaml 
