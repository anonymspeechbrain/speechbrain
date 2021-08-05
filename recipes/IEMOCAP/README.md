# Emotion recognition experiments with IEMOCAP (speech only)
This folder contains scripts for running emotion recognition experiments with the IEMOCAP dataset (https://sail.usc.edu/iemocap/).
Get the IEMOCAP dataset from https://sail.usc.edu/iemocap/iemocap_release.htm and put it in the same folder as `iemocap_prepare.py` under the name `IEMOCAP_processed.tar.gz`.

# Training ECAPA-TDNN
Run the following command to train the model:
`python train.py hparams/train.yaml`

# Results
| Release | hyperparams file | Val. Acc. | Test Acc. | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:| :-----------:|
| 2021-07-04 | train.yaml |  65.3 | 65.7 | Anonymous | 1xV100 16GB |

# Training Time
About 40 sec for each epoch with a TESLA V100.

# Note on Data Preparation
We here use only the audio part of the dataset. The assumpion is that the data folder is structured as:

    ```<session_id>/<emotion>/<file:name>.wav```

e.g. ```session1/ang/psno1_ang_s084_orgn.wav```

Please, process the original IEMOCAP folder to match the expected folder structure.


# **About IEMOCAP**

```bibtex
@article{Busso2008IEMOCAPIE,
  title={IEMOCAP: interactive emotional dyadic motion capture database},
  author={C. Busso and M. Bulut and Chi-Chun Lee and Ebrahim Kazemzadeh and Emily Mower Provost and Samuel Kim and J. N. Chang and Sungbok Lee and Shrikanth S. Narayanan},
  journal={Language Resources and Evaluation},
  year={2008},
  volume={42},
  pages={335-359}
}
```


