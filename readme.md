# lf-net-tensorflow-2.6.0

修改了报错的代码，在te`nsorflow-2.6.0`上运行

`ubuntu20.04,GeForce RTX 3060,CUDA Version: 11.4, cudnn-11.4-linux-x64-v8.2.4.15.tgz`

新建`conda`环境

```bash
conda create -n LF-net python=3.6.5  
pip install -r requirements.txt 

```

requirements.txt修改如下：

```bash
imageio==2.1.2
numpy==1.14.5
opencv-contrib-python==3.4.1.15
opencv-python==3.4.1.15
pandas==0.20.1
scipy==1.0.0
six==1.11.0
tensorflow==2.6.0
tqdm==4.11.2
h5py
```

`tensorflow-2.6.0`对应的`keras`版本

```bash
conda install -c conda-forge keras==2.6.0 
```



```bash
╰─ conda list                                                             ─╯
# packages in environment at /home/cgm/anaconda3/envs/LF-net:
#
# Name                    Version                   Build  Channel
_libgcc_mutex             0.1                 conda_forge    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
_openmp_mutex             4.5                       2_gnu    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
absl-py                   0.15.0                   pypi_0    pypi
astor                     0.8.1                    pypi_0    pypi
astunparse                1.6.3                    pypi_0    pypi
backports                 1.0                pyhd8ed1ab_3    conda-forge
backports.functools_lru_cache 1.6.4              pyhd8ed1ab_0    conda-forge
bleach                    1.5.0                    pypi_0    pypi
ca-certificates           2023.5.7             hbcca054_0    conda-forge
cached-property           1.5.2                    pypi_0    pypi
cachetools                4.2.4                    pypi_0    pypi
certifi                   2023.5.7                 pypi_0    pypi
charset-normalizer        2.0.12                   pypi_0    pypi
clang                     5.0                      pypi_0    pypi
dataclasses               0.8                      pypi_0    pypi
decorator                 5.1.1              pyhd8ed1ab_0    conda-forge
entrypoints               0.4                pyhd8ed1ab_0    conda-forge
enum34                    1.1.10                   pypi_0    pypi
flatbuffers               1.12                     pypi_0    pypi
gast                      0.4.0                    pypi_0    pypi
google-auth               2.18.0                   pypi_0    pypi
google-auth-oauthlib      0.4.6                    pypi_0    pypi
google-pasta              0.2.0                    pypi_0    pypi
grpcio                    1.48.2                   pypi_0    pypi
h5py                      3.1.0                    pypi_0    pypi
html5lib                  0.9999999                pypi_0    pypi
idna                      3.4                      pypi_0    pypi
imageio                   2.1.2                    pypi_0    pypi
importlib-metadata        4.8.3                    pypi_0    pypi
ipykernel                 5.5.5            py36hcb3619a_0    conda-forge
ipython                   5.8.0                    py36_1    conda-forge
ipython_genutils          0.2.0                      py_1    conda-forge
jupyter_client            5.3.4                    py36_0    conda-forge
jupyter_core              4.5.0                      py_0    conda-forge
keras                     2.10.0                   pypi_0    pypi
keras-preprocessing       1.1.2                    pypi_0    pypi
libgcc-ng                 12.2.0              h65d4601_19    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
libgomp                   12.2.0              h65d4601_19    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
libsodium                 1.0.18               h36c2ea0_1    conda-forge
libstdcxx-ng              12.2.0              h46fd767_19    conda-forge
markdown                  3.3.7                    pypi_0    pypi
ncurses                   5.9                          10    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
numpy                     1.19.5                   pypi_0    pypi
oauthlib                  3.2.2                    pypi_0    pypi
opencv-contrib-python     3.4.1.15                 pypi_0    pypi
opencv-python             3.4.1.15                 pypi_0    pypi
openssl                   1.0.2u               h516909a_0    conda-forge
opt-einsum                3.3.0                    pypi_0    pypi
pandas                    0.20.1                   pypi_0    pypi
pexpect                   4.8.0              pyh1a96a4e_2    conda-forge
pickleshare               0.7.5                   py_1003    conda-forge
pillow                    8.4.0                    pypi_0    pypi
pip                       21.3.1             pyhd8ed1ab_0    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
prompt_toolkit            1.0.15                     py_1    conda-forge
protobuf                  3.19.6                   pypi_0    pypi
ptyprocess                0.7.0              pyhd3deb0d_0    conda-forge
pyasn1                    0.5.0                    pypi_0    pypi
pyasn1-modules            0.3.0                    pypi_0    pypi
pygments                  2.12.0             pyhd8ed1ab_0    conda-forge
python                    3.6.5                         1    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
python-dateutil           2.8.2              pyhd8ed1ab_0    conda-forge
python_abi                3.6                     2_cp36m    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
pytz                      2023.3                   pypi_0    pypi
pyzmq                     19.0.2           py36h9947dbf_2    conda-forge
readline                  7.0                           0    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
requests                  2.27.1                   pypi_0    pypi
requests-oauthlib         1.3.1                    pypi_0    pypi
rsa                       4.9                      pypi_0    pypi
scipy                     1.0.0                    pypi_0    pypi
setuptools                58.0.4           py36h5fab9bb_2    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
simplegeneric             0.8.1                      py_1    conda-forge
six                       1.11.0                   pypi_0    pypi
sqlite                    3.20.1                        2    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
tensorboard               2.10.1                   pypi_0    pypi
tensorboard-data-server   0.6.1                    pypi_0    pypi
tensorboard-plugin-wit    1.8.1                    pypi_0    pypi
tensorflow-estimator      2.8.0                    pypi_0    pypi
tensorflow-gpu            2.6.0                    pypi_0    pypi
tensorflow-tensorboard    0.4.0                    pypi_0    pypi
termcolor                 1.1.0                    pypi_0    pypi
tk                        8.6.11               h27826a3_1    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
tornado                   6.1              py36h8f6f2f9_1    conda-forge
tqdm                      4.11.2                   pypi_0    pypi
traitlets                 4.3.3              pyhd8ed1ab_2    conda-forge
typing-extensions         3.7.4.3                  pypi_0    pypi
urllib3                   1.26.15                  pypi_0    pypi
wcwidth                   0.2.6              pyhd8ed1ab_0    conda-forge
werkzeug                  2.0.3                    pypi_0    pypi
wheel                     0.37.1             pyhd8ed1ab_0    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
wrapt                     1.12.1                   pypi_0    pypi
xz                        5.2.6                h166bdaf_0    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
zeromq                    4.3.4                h9c3ff4c_1    conda-forge
zipp                      3.6.0                    pypi_0    pypi
zlib                      1.2.11            h36c2ea0_1011    http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
```



`下载预训练模型 pretrained models和`scare_coeur序列。例如，将它们解压缩到当前文件夹，以便它们低于 `release/models/outdoor` 。






==========================================================================================================================
# LF-Net: Learning Local Features from Images

This repository is a tensorflow implementation  for Y.  Ono, E. Trulls, P. Fua,
K.M. Yi, "LF-Net: Learning Local Features from Images". If you use this code in
your research, please cite [the paper](https://arxiv.org/abs/1805.09662). 


![comparison](/teasers/teasers.png)

## Important Note regarding the use of ratio tests

Do **NOT** use the ratio test for descriptor matching! The commonly-used ratio 
test depends on the distribution of descriptor distances, and the threshold 
differs from one descriptor to another. Commonly used thresholds (0.9 0.7) are
actually harmful for LF-Net. If you want to use the ratio test, you need to 
either tune this manually, or use statistical analysis as Lowe did for SIFT.

## Installation

This code is based on Python3.6.5 and tensorflow with CUDA-8.0. For more details on
the required  libraries, see  `requirements.txt`. You  can also  easily prepare
this by doing

```
pip install -r requirements.txt
```

## Docker image

We created a self-contained [Docker image](https://hub.docker.com/r/jiangweivcg/lf-net-release-env), for running the keypoint extraction demo easily. Make sure you have the nvidia docker runtime.

To launch a container:

`docker run --runtime=nvidia -e NVIDIA_VISIBLE_DEVICES=all -ti --name lf-net-container -v /path/to/code_repo:/home jiangweivcg/lf-net-release-env`

To run the ` run_lfnet.py` script inside the container:

`cd /home`

`python run_lfnet.py --in_dir=/path/to/images --out_dir=/path/to/outputs`


## Pretrained models and example dataset

Download                             the                            [pretrained
models](https://www.cs.ubc.ca/research/kmyi_data/files/2018/lf-net/pretrained.tar.gz) and
the                                                                [scare_coeur
sequence](https://www.cs.ubc.ca/research/kmyi_data/files/2018/lf-net/sacre_coeur.tar.gz). Extract
them to the current folder so that they fall under `release/models/outdoor` for
example.

For other datasets, we do not plan to release them at the moment. Please do not
contact us for  explanations on the training phase. We  are providing them **as
is** as a reference implementation.

## Updates new pretrained models
Download [pretrained model without rotation augmentation ](https://www.cs.ubc.ca/research/kmyi_data/files/2018/lf-net/lfnet-norotaug.tar.gz)

### Updates since the arXiv version

The provided pre-trained  models are trained with full  360 degree augmentation
for  orientation. Thus,  the results  you get  from these  models are  slightly
different  from  the  one  reported  in  arXiv.  We  have  further  included  a
consistency term on the orientation assignment.

## Running the keypoint extraction demo

To run LF-Net for all images in a given directory, simply type:

```
python run_lfnet.py --in_dir=images --out_dir=outputs
```

In addition, you can easily do the 2-view matching demo through
`notebooks/demo.ipynb` .

## Training

Training code can be found in `train_lfnet.py`. We will **not** provide any
support for the training process and datasets. All issues related to this topic
will be closed without answers.


## Some Examples

| Outdoor dataset</br> Top: LF-Net, Bottom: SIFT | Indoor dataset </br>Top: LF-Net, Bottom: SIFT | Webcam dataset</br>Top: LF-Net, Bottom: SIFT |
|:---------|:--------------------|:----------------|
| ![outdoor](/teasers/sfm_ours_sift.gif)     | ![indoor](/teasers/scannet_ours_sift.gif) | ![webcam](/teasers/webcam_ours_sift.gif) |
