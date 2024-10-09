# Equivariant Masked Position Prediction for Efficient Molecular Representation


This repository contains the PyTorch implementation of the work "Equivariant Masked Position Prediction for Efficient Molecular Representation".


## Environment Setup ##
The implementation of this project is based on the Equiformer project. You can migrate the code in (nets) and (engine.py) to other equivariant GNNs.

### Environment 

See [here](docs/env_setup.md) for setting up the environment.


### QM9

The dataset of QM9 will be automatically downloaded when running training.


### MD17

The dataset of MD17 will be automatically downloaded when running training.


## Training ##


### QM9

1. We provide training scripts under [`scripts/train/qm9/equiformer`](scripts/train/qm9/equiformer).
For example, we can train Equiformer for the task of `alpha` by running:

    ```bash
        sh scripts/train/qm9/equiformer/target@1.sh
    ```

2. The QM9 dataset will be downloaded automatically as we run training for the first time.

3. The target number for different regression tasks can be found [here](https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.datasets.QM9.html#torch_geometric.datasets.QM9).



### MD17

1. We provide training scripts under [`scripts/train/md17/equiformer`](scripts/train/md17/equiformer).
For example, we can train Equiformer for the molecule of `aspirin` by running:

    ```bash
        sh scripts/train/md17/equiformer/se_l2/target@aspirin.sh    # L_max = 2
        sh scripts/train/md17/equiformer/se_l3/target@aspirin.sh    # L_max = 3
    ```

### General 

1. [`nets`](nets) includes code of position prediction modules.
2. [`engine`](engine.py) includes code of masking strategies.
3. [`scripts`](scripts) includes scripts for training models for QM9 and MD17.
 
