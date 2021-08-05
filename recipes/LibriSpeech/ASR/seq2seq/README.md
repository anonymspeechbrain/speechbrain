# LibriSpeech ASR with seq2seq models (CTC + attention).
This folder contains the scripts to train a seq2seq CNN-RNN-based system using LibriSpeech.
You can download LibriSpeech at http://www.openslr.org/12

# How to run
python train.py hparams/file.yaml

# Results

| Release | hyperparams file | Test Clean WER | HuggingFace link | Full model link | GPUs |
|:-------------:|:---------------------------:| :-----:| :-----:| :-----:| :--------:|
| 01-03-21 | train_BPE_1000.yaml | 3.08 | Anonymous| Not Available| 1xV100 32GB |
| 01-03-21 | train_BPE_5000.yaml | 2.89 | Anonymous | Not Available | 1xV100 32GB |

# Training Time
It takes about 5 hours for each epoch on a NVDIA V100 (32GB).

# PreTrained Model + Easy-Inference
You can find the pre-trained model with an easy-inference function on HuggingFace:
- Anonymous
- Anonymous
- Anonymous

You can find the full experiment folder (i.e., checkpoints, logs, etc) here:
Anonymous

