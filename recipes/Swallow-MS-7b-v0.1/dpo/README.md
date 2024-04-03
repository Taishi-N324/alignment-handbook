
```shell
pip install wandb
pip install wheel
python -m pip install .
git clone https://github.com/Dao-AILab/flash-attention.git
cd flash-attention
python setup.py install
```

```shell
export CUDA_VISIBLE_DEVICES=2
export WANDB_PROJECT=Swallow-MS-7b-DPO
export WANDB_NAME=beta0.01_GBS64_lr_5e7.yaml
ACCELERATE_LOG_LEVEL=info accelerate launch --config_file recipes/accelerate_configs/deepspeed_zero3.yaml --main_process_port 32000 scripts/run_dpo.py recipes/Swallow-MS-7b-v0.1/dpo/beta0.01_GBS64_lr_5e7.yaml >> beta0.01_GBS64_lr_5e7.logs 2>&1 
```