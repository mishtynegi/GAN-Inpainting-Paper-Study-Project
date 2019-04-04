# GAN Inpainting Paper Study Project
This is a repository for training the model found [here](https://github.com/JiahuiYu/generative_inpainting) on [DTD](https://www.robots.ox.ac.uk/~vgg/data/dtd/). All credits for the algorithm go the author of the same. These are just instructions and helper files to run the training yourself. These will be used for academic purposes only.

An interactive demo for this can be setup using code found [here](https://github.com/mishtynegi/Interactive-tool-for-GAN-Inpainting).
 
## Prerequisites:
- Bash Shell
- Anaconda

## Preparing the environment: 
Run the following commands in your shell:

```
conda config –add channels conda-forge
conda install tensorflow
conda install opencv
conda install pyyaml
pip install git+https://github.com/JiahuiYu/neuralgym
conda install pybottle
```

## Running the training:
For the training, the following directory structure is required: 

```
├── Interactive_tool-for-GAN-Inpainting
│   ├── train.py
│   └── test.py
│   └── inpaint.yml
│   └── inpaint_ops.py
│   └── inpaint_model.py
│   └── model_logs
│	│   └── <model directories go here>
│	└── neuralgym_logs
│	│   └── _<logs will go here>_
│	└── data
│	│   └── dtd
│	│   │   └── <training_data folder>
│	│   │   └── <flist files>

```

To run this, modify _inpaint.yml_ to point to your data sets located above (see our _inpaint.yml_ file for an example with the ‘dtd’ data set). A script to generate the required flist files is provided as well (see _training_flist_creation.py_), inspired by code found [here](https://github.com/JiahuiYu/generative_inpainting/issues/15).

Once the properties have been set, run the following command in the GenerativeInpainting directory:
```
python train.py
```
## WGAN-GP
Code for demo can be found in this repository as well (_Demo folders) with a detailed explanation [here](https://docs.google.com/document/d/1HaEFRi-zjvyZEo2KZy6jw5UiVPxN26aF0apbzp4WFSA/edit?usp=sharing).
