# Prefix-Tuning: (Customized) WebNLG
## Usage
### Setup
```bash
cd transformers
pip install -e .
```
### Train
```bash
cd gpt2
CUDA_VISIBLE_DEVICES=0 python train_e2e.py --optim_prefix yes --preseqlen 5 --epoch 5 --learning_rate 0.00005 --mode webnlg --bsz 5 --seed 101
```
### Generate
```bash
cd gpt2
python gen.py webnlg yes valid {checkpoint_path} no
```

