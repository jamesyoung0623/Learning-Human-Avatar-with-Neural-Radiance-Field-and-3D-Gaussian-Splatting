# Learning Human Avatar with Neural Radiance Field and 3D Gaussian Splatting

This repository is a term project for Interactive Computer Graphics 2024 Spring. 

# Getting Started

This repository is tested on Ubuntu 22.04.4 with CUDA 11.7. Run the following commands to create a conda environment and install the required packages.
```
conda create -n hugs python=3.8 -y

conda activate hugs

conda install -y pytorch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia

pip install fvcore iopath
pip install --no-index --no-cache-dir pytorch3d -f https://dl.fbaipublicfiles.com/pytorch3d/packaging/wheels/py38_cu117_pyt1131/download.html

pip install submodules/diff-gaussian-rasterization
pip install submodules/simple-knn

pip install -r requirements.txt
pip install git+https://github.com/mattloper/chumpy.git
pip install git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch
```

# Preparing the datasets and models
Please refer to the original repository [HUGS](https://github.com/apple/ml-hugs?tab=readme-ov-file#preparing-the-datasets-and-models) for datasets and models preparation.


# Training
    python main.py --cfg_file hugs_human_scene.yaml

# Evaluation and Animation
    python scripts/evaluate.py

# Acknowledgement
The implementation took reference from [HUGS](https://github.com/apple/ml-hugs?tab=readme-ov-file#preparing-the-datasets-and-models) and [HumanNeRF](https://github.com/chungyiweng/humannerf)
