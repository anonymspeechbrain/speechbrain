# Google Speech Command v0.02 Dataset
This folder contains recipes for command recognition with [Google Speech Command Dataset](https://www.tensorflow.org/datasets/catalog/speech_commands).
The recipes supports 12 or 35 commands.  To run it, please type:

```
python train.py hparams/xvect.yaml --data_folder=/path_to_/GSC (V12 task)
python train.py hparams/xvect.yaml --data_folder=/path_to_/GSC --seed=1234  --number_of_commands=35 --percentage_unknown=0 --percentage_silence=0 (v35 task)
```

# Performance summary

[Command accuracy on Google Speech Commands]
| System | Accuracy |
|----------------- | ------------ |
| xvector + augment v12 | 98.14% |
| xvector + augment v35 | 97.43% |



# PreTrained Model + Easy-Inference
You can find the pre-trained model with an easy-inference function on HuggingFace:
- https://huggingface.co/Anonymous/google_speech_command_xvector

You can find the full experiment folder (i.e., checkpoints, logs, etc) here:
Anonymous


