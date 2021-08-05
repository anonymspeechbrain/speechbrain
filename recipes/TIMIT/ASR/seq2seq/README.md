# TIMIT ASR with seq2seq models.
This folder contains the scripts to train a seq2seq RNNN-based system using TIMIT.
TIMIT is a speech dataset available from LDC: https://catalog.ldc.upenn.edu/LDC93S1

# How to run
python train.py hparams/train.yaml

# Results

| Release | hyperparams file | Val. PER | Test PER | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:| :-----------:|
| 20-05-22 | train.yaml |  12.50 | 14.07 | Anonymous | 1xV100 16GB |
| 21-04-08 | train_with_wav2vec2.yaml |  7.11 | 8.04 | Anonymous | 1xV100 32GB |


