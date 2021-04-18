# Detection of Anomalous Communication in Fighter Jets

This repository is the official implementation of Detection of [Anomalous Communication in Fighter Jets](https://www.overleaf.com/read/gysdvyvhbhkr). 

The main contributions of this paper are as follows:

•Collect flight data using a novel approach that allows for much longer recordings to better reflect the real world.

•Design an IDS that considers all word types on MIL-STD-1553 to identify potential anomalies in every message.

•Identify whether a message is considered anomalous and specify the precise type of attack with greater performance compared to other methods.

## Requirements

- unpack `odf.zip` into `odf` folder in working directory
- upack `Small_Data.zip` or `Big_Data.zip` in `data` folder (or any folder specified by `folder='data'`).  It is reccommended to use `Big_Data.zip` as the small data files can be difficult to work with.
- Install dependencies with `requirements.txt` (Some additional dependencies may be required as specified in the first code block)

## Training

To train the model(s) in the paper, run the complete `Pipeline.ipynb` Script

## Evaluation

To compare the final model with other methods, replace the `build()` code block with one of the models specified in `TestedNetworks.ipynb`


## Results

Our model achieves the following performance on `Big_Data.zip`:

| Network   | GCNN   |
|-----------|--------|
| Precision | 0.9724 |
| Recall    | 0.8518 |
| F1        | 0.9081 |
| AUC       | 0.9801 |
| SCA       | 0.9542 |
| Runtime   | 22.9   |

## Bugfixes

Sometimes, the following error may appear when running the notebook for the first time:

```
Is a directory: 'data/.ipynb_checkpoints'
```

May be fixed by deleting the problematic folder, i.e.

```
rm -rf .~/data/.ipynb_checkpoints
```
