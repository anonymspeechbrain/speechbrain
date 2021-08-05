# MetricGAN+ Recipe for Enhancement

This recipe implements MetricGAN+ recipe for enhancement as described in the paper
Anonymous

Use the `download_vctk` function in `voicebank_prepare.py` to download the dataset
and resample it to 16000 Hz. To run an experiment, execute the following command in
the current folder:

```bash
python train.py hparams/train.yaml --data_folder /path/to/data_folder
```

## Results

Experiment Date | PESQ | CSIG | CBAK | COVL
-|-|-|-|-
2021-03-06 | 3.15 | 4.14 | 3.16 | 3.64


# PreTrained Model + Easy-Inference
You can find the pre-trained model with an easy-inference function on HuggingFace:
- Anonymous

You can find the full experiment folder (i.e., checkpoints, logs, etc) here:
Anonymous



