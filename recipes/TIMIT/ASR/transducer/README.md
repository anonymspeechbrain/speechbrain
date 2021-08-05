# TIMIT ASR with Transducer models.
This folder contains the scripts to train an RNNT system using TIMIT.
TIMIT is a speech dataset available from LDC: https://catalog.ldc.upenn.edu/LDC93S1


# Extra-Dependencies
Before running this recipe, make sure numba is installed. Otherwise, run:
```
pip install numba
```

# How to run
Update the path to the dataset in the yaml config file and run the following.
```
python train.py hparams/train.yaml
```

# Results

| Release | hyperparams file | Val. PER | Test PER | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:| :-----------:|
| 2021-02-06 | train.yaml |  13.11 | 14.12 | Anonymous | 1xRTX6000 24GB |
| 21-04-16 | train_wav2vec2.yaml |  7.97 | 8.91 | Anonymous | 1xRTX6000 24Gb |

# Training Time
About 2 min and 40 sec for each epoch with a  RTX 6000.


