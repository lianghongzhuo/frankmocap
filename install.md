# Install Guid

## step1: Install packages in the environment
```bash
micromamba create -y -n frank python=3.11

micromamba activate frank

micromamba install pytorch3d pytorch fvcore matplotlib omegaconf cloudpickle pandas tqdm scipy \
ipython cuda-nvcc ninja libcusparse-dev opencv pycocotools gdown scikit-learn pyopengl easydict

micromamba install nvidia/label/cuda-12.0.0::cuda-toolkit

git clone PATH_TO_THIS_REPO
cd frankmocap
sh scripts/install_frankmocap.sh
cd ..
git clone https://github.com/vchoutas/smplx.git
cd smplx
pip install --no-deps -e .
cd ..
git clone https://github.com/facebookresearch/detectron2.git
cd detectron2
pip install --no-deps -e .
pip install git+https://github.com/uyoung-jeong/chumpy.git
```

# step2: Download data:
go to this website:
- smpl: https://smpl.is.tue.mpg.de/download.php
- smplx: https://smpl-x.is.tue.mpg.de/download.php

Put the file in: 
```bash
./extra_data/smpl/basicModel_neutral_lbs_10_207_0_v1.0.0.pkl
./extra_data/smpl/SMPLX_NEUTRAL.pkl
```
