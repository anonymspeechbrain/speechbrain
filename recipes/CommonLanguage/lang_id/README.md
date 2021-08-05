# Language Identification experiments with CommonLanguage.
This folder contains scripts for running language identificationexperiments with the [CommonLanguage](https://zenodo.org/record/5036977/files/CommonLanguage.tar.gz?download=1) dataset. These experiments were highly inspired by Speaker Identification tasks on VoxCeleb and follow a similar path.

# Training [ECAPA-TDNN](https://arxiv.org/abs/2005.07143)
Similar to the X-Vector a bigger and more powerful ECAPA-TDNN model can be used.

`python train.py hparams/train_ecapa_tdnn.yaml`

The experiment is also fine-tuning of the trained speaker embeddings done for Speaker Identification task on VoxCeleb, and can be accessed on https://huggingface.co/Anonymous/spkrec-ecapa-voxceleb. Therefore, most of the architecture choices come from that task.

Data augmentation and environmental corruption are done by concatenating waveforms, dropout, speed change, reverberation, noise, and noise+rev. The batch is double size of the original one. This may lead to
better performance, at the cost of longer training time and higher compute resourses.

# Performance
| Release | hyperparams file | Val. PER | Test PER | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:| :-----------:|
| 21-06-28 | train.yaml |  13. 5 | 15.1 | Anonymous | 1xV100 16GB |

Each epoch takes approximately 14 minutes on an NVIDIA V100.

# Inference
The pre-trained model + easy inference is available on HuggingFace:
- hAnonymous

Basically, you can run inference with only few lines of code:

```python
import torchaudio
from speechbrain.pretrained import EncoderClassifier
classifier = EncoderClassifier.from_hparams(source="speechbrain/lang-id-commonlanguage_ecapa", savedir="pretrained_models/lang-id-commonlanguage_ecapa")

# Italian Example
out_prob, score, index, text_lab = classifier.classify_file('speechbrain/lang-id-commonlanguage_ecapa/example-it.wav')
print(text_lab)

# French Example
out_prob, score, index, text_lab = classifier.classify_file('speechbrain/lang-id-commonlanguage_ecapa/example-fr.wav')
print(text_lab)
```




