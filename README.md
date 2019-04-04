# GAN Inpainting Paper Study Project
This is a repository for training the model found [here](https://github.com/JiahuiYu/generative_inpainting) on [DTD](https://www.robots.ox.ac.uk/~vgg/data/dtd/)
 
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
│	│   └── <training and validation sets>
│	│   └── <flist files for the same>
```

To run this, modify _inpaint.yml_ to point to your data sets located above (see our _inpaint.yml_ file for an example with the ‘dtd’ data set). Details for creating an flist file can be found here.

Once the properties have been set, run the following command in the GenerativeInpainting directory:
```
python train.py
```
