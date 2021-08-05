# AISHELL-1 ASR with Transformers.
This folder contains recipes for tokenization and speech recognition with [AISHELL-1](https://www.openslr.org/33/), a 150-hour Chinese ASR dataset.

### How to run
1- Train a tokenizer. The tokenizer takes in input the training transcripts and determines the subword units that will be used for both acoustic and language model training.

```
cd ../../Tokenizer
python train.py hparams/train_transformer_tokenizer_bpe5000.yaml --data_folder=/localscratch/aishell/
```
If not present in the specified data_folder, the dataset will be automatically downloaded there.
This step is not mandatory. We will use the official tokenizer downloaded from the web if you do not 
specify a different tokenizer in the speech recognition recipe. 

2- Train the speech recognizer
```
python train.py hparams/train_ASR_transformer.yaml --data_folder=/localscratch/aishell/
```

# Performance summary
Results are reported in terms of Character Error Rate (CER).

| hyperparams file | LM | Test CER | Dev CER | GPUs |
|:--------------------------:|:-----:| :-----:| :-----:| :-----: |
| train_ASR_transformer.yaml | No | 6.04 | 5.60 | 1xRTX 2080 Ti 11GB |
| train_ASR_transformer_with_wav2vect.yaml | No | 5.58 | 5.19 | 1xRTX 8000 Ti 48GB |

You can checkout our results (models, training logs, etc,) here:
Anonymous

# Training Time
It takes about 1h 10 minutes on a NVIDIA V100 (32GB) for train_ASR_transformer.yaml,
and about 5 hours minutes on a NVIDIA V100 (32GB) for rain_ASR_transformer_with_wav2vect.yaml.


# PreTrained Model + Easy-Inference
You can find the pre-trained model with an easy-inference function on HuggingFace
- Anonymous
- Anonymous
 
