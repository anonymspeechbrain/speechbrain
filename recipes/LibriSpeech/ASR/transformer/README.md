# LibriSpeech ASR with Transformers.
This folder contains the scripts to train a Transformer-based speech recognizer
using LibriSpeech.

You can download LibriSpeech at http://www.openslr.org/12


# How to run
python train.py train/train.yaml

# Results

| Release | hyperparams file | Test Clean WER | HuggingFace link | Model link | GPUs |
|:-------------:|:---------------------------:| :-----:| :-----:| :-----:| :--------:|
| 20-05-22 | transformer.yaml | 2.46 | Anonymous | Anonymous | 2xRTX8000 42GB |

# Training Time
It takes about 1 hour 35 minutes for each epoch on 4 NVDIA V100 (32GB).


# PreTrained Model + Easy-Inference
You can find the pre-trained model with an easy-inference function on HuggingFace:
- Anonymous
- Anonymous
- Anonymous

You can find the full experiment folder (i.e., checkpoints, logs, etc) here:
Anonymous

