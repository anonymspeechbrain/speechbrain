# CommonVoice ASR with CTC + Attention based Seq2Seq models.
This folder contains scripts necessary to run an ASR experiment with the CommonVoice dataset: [CommonVoice Homepage](https://commonvoice.mozilla.org/)

# How to run
python train.py hparams/{hparam_file}.py

# Data preparation
It is important to note that CommonVoice initially offers mp3 audio files at 42Hz. Hence, audio files are downsampled on the fly within the dataio function of the training script.

# Languages
Here is a list of the different languages that we tested within the CommonVoice dataset:
- French
- Kinyarwanda
- Italian
- English

# Results

| Language | CommonVoice Release | hyperparams file | LM | Val. CER | Val. WER | Test CER | Test WER | HuggingFace link | Model link | GPUs |
| ------------- |:-------------:|:---------------------------:| -----:| -----:| -----:| -----:| -----:| :-----------:| :-----------:| :-----------:|
| French | 2020-12-11 | train_fr.yaml | No | 5.36 | 15.87 | 6.54 | 17.70 | Anonymous | Anonymous | 2xV100 16GB |
| French | 2020-12-11 | train_fr_with_wav2vec.yaml | No | 6.13 | 11.82 | 9.78 | 13.34 | Anonymous | Anonymous | 2xV100 32GB |
| Kinyarwanda | 2020-12-11 | train_rw.yaml | No | 7.30 | 21.36 | 9.55 | 24.27 | Not Avail. | Anonymous | 2xV100 32GB |
| Kinyarwanda | 2020-12-11 | train_rw_with_wav2vec.yaml | No | 5.08 | 15.88 | 8.33 | 18.91 | Anonymous | Anonymous | 2xV100 16GB |
| English | 2020-12-11 | train_en.yaml | No | 8.66 | 20.16 | 12.93 | 24.89 | Not Avail. | Anonymous | 2xV100 16GB |
| English | 2020-12-11 | train_en_with_wav2vec.yaml | No | 14.50 | 13.21 | 24.65 | 15.69 | Anonymous | Anonymous | 2xV100 32GB |
| Italian | 2020-12-11 | train_it.yaml | No | 5.14 | 15.59 | 15.40 | 16.61 | Anonymous | Anonymous | 2xV100 16GB |
| Italian | 2020-12-11 | train_it_with_wav2vec.yaml | No | 3.11 | 8.30 | 5.75 | 9.86 | Anonymous | Anonymous) | 2xV100 16GB |

## How to simply use pretrained models to transcribe my audio file?

SpeechBrain provides a simple interface to transcribe audio files with pretrained models. All the necessary information can be found on the different HuggingFace repositories (see the results table above) corresponding to our different models for CommonVoice.
