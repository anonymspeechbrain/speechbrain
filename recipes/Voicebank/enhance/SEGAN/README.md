
# VoiceBank Speech Enhancement with SEGAN
This recipe implements a speech enhancement system based on the SEGAN architecture
with the VoiceBank dataset.
(based on the paper: Pascual et al. https://arxiv.org/pdf/1703.09452.pdf).

# How to run
python train.py hparams/train.yaml

# Results
| Release | hyperparams file | Test PESQ | Test STOI | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:| :-----------:|
| 2021-07-10 | train.yaml |  2.38 | 0.923 | Anonymous | 1xV100 16GB |

# Training Time
About 2 min and 30 sec for each epoch with a TESLA V100.


